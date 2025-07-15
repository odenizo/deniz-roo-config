# 🔧 Configurations Directory

This directory contains all Roo Code configuration files, organized in a layered architecture for optimal management and LLM interaction.

## 📁 Directory Structure

```
configurations/
├── 📁 base/                    # Base configurations from upstream
│   ├── .clinerules            # Core rules (synced)
│   ├── .roomodes              # Mode definitions (synced)
│   └── .roorules              # Additional rules (synced)
├── 📁 custom/                 # Your personal customizations
│   ├── deniz-overrides.rules  # Personal rule overrides
│   ├── custom-modes.json      # Custom mode definitions
│   └── preferences.yaml       # Personal preferences
├── 📁 modes/                  # Custom mode definitions
│   ├── ai-automation/         # AI automation specialized mode
│   ├── zero-code/             # Zero-coding mode
│   ├── llm-optimized/         # LLM interaction optimized
│   └── full-stack-ai/         # Complete AI development
└── 📁 templates/              # Ready-to-use templates
    ├── project-init/          # Project initialization
    ├── memory-bank/           # Memory bank setups
    └── quick-start/           # Quick start configurations
```

## 🎯 Configuration Layers

### 1. Base Layer (`base/`)
- **Source**: Automatically synchronized from upstream repositories
- **Purpose**: Provides foundation configurations and latest features
- **Management**: Read-only, updated via automated workflows
- **Files**:
  - `.clinerules` - Core behavior rules
  - `.roomodes` - Mode definitions and settings
  - `.roorules` - Additional operational rules

### 2. Custom Layer (`custom/`)
- **Source**: Your personal modifications and preferences
- **Purpose**: Extends and overrides base configurations
- **Management**: Version controlled, manually edited
- **Files**:
  - `deniz-overrides.rules` - Personal rule modifications
  - `custom-modes.json` - Custom mode definitions
  - `preferences.yaml` - Personal preferences and settings

### 3. Mode Layer (`modes/`)
- **Source**: Custom mode implementations
- **Purpose**: Specialized behavior for different use cases
- **Management**: Template-based creation with customization
- **Directories**:
  - `ai-automation/` - Full AI reliance mode
  - `zero-code/` - Non-technical user mode
  - `llm-optimized/` - LLM interaction mode
  - `full-stack-ai/` - Complete AI development mode

### 4. Template Layer (`templates/`)
- **Source**: Ready-to-use configuration sets
- **Purpose**: Quick setup for common scenarios
- **Management**: Curated and maintained templates
- **Categories**:
  - `project-init/` - New project setup
  - `memory-bank/` - Memory bank configurations
  - `quick-start/` - Minimal setup templates

## 🔄 Configuration Merging

Configurations are applied in order of precedence:

1. **Base configurations** (lowest precedence)
2. **Template configurations** (if used)
3. **Custom configurations** (highest precedence)

### Merge Strategy
- **Rules**: Custom rules extend and override base rules
- **Modes**: Custom modes are added to available modes
- **Preferences**: Personal preferences take precedence

## 🛠️ Usage Examples

### Apply a Template
```bash
# Copy AI-focused template
cp templates/ai-focused/* ./

# Apply custom overrides
cp custom/deniz-overrides.rules ./.clinerules-custom
```

### Create Custom Mode
```bash
# Copy base mode template
cp modes/ai-automation/mode-template.json modes/my-custom-mode.json

# Edit with your preferences
# nano modes/my-custom-mode.json
```

### Backup Current Configuration
```bash
# Export current setup
mkdir ../exports/backup-$(date +%Y%m%d)
cp .clinerules .roomodes .roorules ../exports/backup-$(date +%Y%m%d)/
```

## 🔍 Configuration Validation

All configurations are automatically validated:
- **Syntax**: JSON/YAML syntax validation
- **Schema**: Structure validation against known patterns
- **Compatibility**: Cross-compatibility checks
- **Performance**: Impact analysis on performance

## 📝 Best Practices

1. **Always backup** before making significant changes
2. **Test configurations** in a separate environment first
3. **Use templates** as starting points for new configurations
4. **Document custom changes** in comments
5. **Version control** all personal modifications

## 🆘 Troubleshooting

### Common Issues

**Configuration not loading**:
- Check file syntax and structure
- Verify file permissions
- Review validation logs

**Conflicts during sync**:
- Review merge conflicts in custom files
- Use rollback if needed
- Check validation status

**Performance issues**:
- Review configuration complexity
- Check for recursive patterns
- Optimize rule definitions

### Getting Help

- Check [troubleshooting guide](../docs/troubleshooting.md)
- Review [configuration examples](../docs/configuration-examples.md)
- Open an issue for persistent problems

---

**💡 Remember**: This layered approach ensures your customizations are preserved while benefiting from upstream improvements!
