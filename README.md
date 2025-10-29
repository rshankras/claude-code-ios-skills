# Claude Code Skills for iOS/Swift Development

A collection of professional, well-structured Claude Code skills for iOS and Swift development. These skills help you maintain code quality, ensure HIG compliance, and create new skills with best practices.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

## 📦 Skills Included

### 🔍 coding-best-practices

Reviews Swift/iOS code for adherence to modern Swift idioms, Apple platform best practices, architecture patterns, and code quality standards.

**Features:**
- **Swift Language Patterns**: Optionals handling, type safety, collections, error handling, naming conventions
- **SwiftUI Best Practices**: State management, view composition, performance optimization
- **MVVM Architecture**: Separation of concerns, code organization, memory management
- **Core Data Patterns**: Context management, saving/fetching, relationships, CloudKit integration

**When to use:**
- Code reviews
- Refactoring sessions
- Architecture reviews
- Quality audits

**Modular Structure:**
- `SKILL.md` - Main review process
- `swift-patterns.md` - Swift language best practices
- `swiftui-patterns.md` - SwiftUI-specific patterns
- `architecture-patterns.md` - MVVM and organization
- `coredata-patterns.md` - Core Data best practices

### 🎨 ui-review

Comprehensive UI/UX review of SwiftUI code against Apple's Human Interface Guidelines, font best practices, and accessibility standards for iOS and watchOS.

**Features:**
- **HIG Compliance**: Layout, spacing, navigation, colors, tap targets
- **Font Usage**: Dynamic Type support, text styles, typography hierarchy
- **Accessibility**: VoiceOver, labels, hints, traits, testing guidelines
- **Platform-Specific**: iOS and watchOS requirements

**When to use:**
- UI/UX reviews
- Accessibility audits
- HIG compliance checks
- Design system validation

**Modular Structure:**
- `SKILL.md` - Main review process
- `hig-checklist.md` - Comprehensive HIG checklist
- `font-guidelines.md` - Typography and Dynamic Type
- `accessibility-quick-ref.md` - Accessibility quick reference

### 🛠️ skill-creator

Meta-skill that guides you through creating well-structured, modularized Claude Code skills with best practices.

**Features:**
- **Step-by-Step Guide**: Complete skill creation workflow
- **Templates**: Ready-to-use templates for simple and complex skills
- **Best Practices**: Naming, structure, modularization strategies
- **Examples**: Real-world skill examples

**When to use:**
- Creating new skills
- Refactoring existing skills
- Learning skill best practices
- Planning skill architecture

**Modular Structure:**
- `SKILL.md` - Main creation guide
- `skill-template.md` - Simple skill template
- `complex-skill-template.md` - Modularized skill template

## 🚀 Installation

### Option 1: Manual Installation

1. Clone this repository:
```bash
git clone https://github.com/rshankras/claude-code-ios-skills.git
```

2. Copy the skills to your project's `.claude/skills/` directory:
```bash
# From your project root
mkdir -p .claude/skills
cp -r /path/to/claude-code-ios-skills/skills/* .claude/skills/
```

3. The skills will be automatically available in Claude Code

### Option 2: Symlink (Advanced)

For active development or if you want automatic updates:

```bash
# From your project root
mkdir -p .claude/skills
cd .claude/skills

# Create symlinks
ln -s /path/to/claude-code-ios-skills/skills/coding-best-practices coding-best-practices
ln -s /path/to/claude-code-ios-skills/skills/ui-review ui-review
ln -s /path/to/claude-code-ios-skills/skills/skill-creator skill-creator
```

## 📖 Usage

### Using coding-best-practices

```
You: "Can you review my ExpenseViewModel for best practices?"

Claude: [Activates coding-best-practices skill]
- Reviews Swift idioms
- Checks MVVM architecture
- Validates Core Data usage
- Provides scored feedback
```

**Trigger phrases:**
- "review my code"
- "check for best practices"
- "audit code quality"
- "refactor this code"

### Using ui-review

```
You: "Review AddExpenseView for HIG compliance and accessibility"

Claude: [Activates ui-review skill]
- Checks HIG compliance
- Validates font usage
- Audits accessibility
- Tests Dynamic Type support
```

**Trigger phrases:**
- "review the UI"
- "check HIG compliance"
- "accessibility audit"
- "review fonts"

### Using skill-creator

```
You: "Help me create a new skill for API testing"

Claude: [Activates skill-creator skill]
- Guides through requirements
- Suggests structure
- Provides templates
- Helps with modularization
```

**Trigger phrases:**
- "create a new skill"
- "how do I make a skill"
- "skill best practices"

## 🏗️ Skill Architecture

### Modularization Strategy

These skills demonstrate best practices for skill organization:

**Simple Skills** (< 400 lines):
```
skill-name/
└── SKILL.md
```

**Complex Skills** (> 400 lines):
```
skill-name/
├── SKILL.md                # Main entry point (200-300 lines)
├── patterns.md            # Code patterns and anti-patterns
├── checklist.md           # Comprehensive checklists
├── examples.md            # Code examples
└── quick-ref.md           # Quick reference
```

### Benefits of Modularization

- **Maintainability**: Easy to update specific sections
- **Scalability**: Can add references without bloating main file
- **Usability**: Quick access to focused information
- **Clarity**: Main file stays concise and readable

## 🤝 Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Ways to Contribute

- Report bugs or issues
- Suggest new skills
- Improve existing skills
- Add more examples
- Improve documentation
- Share your use cases

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🎯 Roadmap

Future skills and improvements:

- [ ] **unit-testing** - Unit test generation and review
- [ ] **swiftui-preview** - SwiftUI preview generator
- [ ] **api-client** - REST API client generator
- [ ] **migration-helper** - Data model migration assistant
- [ ] **performance-analyzer** - Performance optimization suggestions
- [ ] **localization-checker** - Localization completeness checker

## 📚 Resources

### Apple Documentation
- [Swift API Design Guidelines](https://swift.org/documentation/api-design-guidelines/)
- [iOS Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/designing-for-ios)
- [SwiftUI Documentation](https://developer.apple.com/documentation/swiftui)
- [Core Data Programming Guide](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/CoreData/)

### Claude Code
- [Claude Code Documentation](https://docs.claude.com/claude-code)
- [Claude Code Skills Guide](https://docs.claude.com/claude-code/skills)

## ⭐ Show Your Support

If you find these skills useful, please consider:
- Starring this repository
- Sharing with other iOS developers
- Contributing improvements
- Creating issues for bugs or suggestions

## 👤 Author

**Ravishankar**

- GitHub: [@rshankras]

## 🙏 Acknowledgments

- Apple for comprehensive development guidelines
- Claude Code team for the skills framework
- iOS development community for best practices
- Contributors and users of these skills

## 📧 Contact

For questions, suggestions, or feedback:
- Open an issue on GitHub
- Start a discussion in the Discussions tab

---

**Note**: These skills are designed for iOS/Swift development but can be adapted for other Apple platforms (macOS, watchOS, tvOS).
