# Quick Start Guide

Get up and running with Claude Code iOS Skills in under 5 minutes!

## Prerequisites

- Claude Code installed
- iOS/Swift project with `.claude/` directory

## Installation (1 minute)

### Option 1: Quick Copy

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/claude-code-ios-skills.git

# Navigate to your project
cd /path/to/your/ios-project

# Create skills directory if it doesn't exist
mkdir -p .claude/skills

# Copy all skills
cp -r /path/to/claude-code-ios-skills/skills/* .claude/skills/
```

### Option 2: Individual Skills

Copy only the skills you need:

```bash
# Just coding-best-practices
cp -r /path/to/claude-code-ios-skills/skills/coding-best-practices .claude/skills/

# Just ui-review
cp -r /path/to/claude-code-ios-skills/skills/ui-review .claude/skills/

# Just skill-creator
cp -r /path/to/claude-code-ios-skills/skills/skill-creator .claude/skills/
```

## Verification (30 seconds)

Check that skills are installed:

```bash
ls .claude/skills/
# Should show: coding-best-practices  ui-review  skill-creator
```

## First Use (2 minutes)

### Test coding-best-practices

1. Open Claude Code in your project
2. Type: **"Review my [ViewModelName] for best practices"**
3. Claude will activate the skill and provide a detailed review

### Test ui-review

1. Open Claude Code in your project
2. Type: **"Review [ViewName] for HIG compliance and accessibility"**
3. Claude will audit your UI against Apple guidelines

### Test skill-creator

1. Open Claude Code
2. Type: **"Help me create a new skill for API testing"**
3. Claude will guide you through the creation process

## Common Use Cases

### Code Review Before PR

```
You: "Review all my ViewModels for best practices"
```

Claude will:
- Check Swift idioms
- Validate MVVM architecture
- Review Core Data usage
- Provide scored feedback

### Accessibility Audit

```
You: "Audit my views for accessibility issues"
```

Claude will:
- Check VoiceOver support
- Verify Dynamic Type
- Test color contrast
- Provide recommendations

### Creating Custom Skills

```
You: "I want to create a skill for reviewing API clients"
```

Claude will:
- Ask about requirements
- Suggest structure
- Provide templates
- Guide implementation

## Tips for Best Results

### Be Specific

```
✅ Good: "Review ExpenseViewModel.swift for best practices"
❌ Vague: "Check my code"
```

### Provide Context

```
✅ Good: "Review AddExpenseView for iOS HIG compliance, especially accessibility"
❌ Vague: "Look at this view"
```

### Request Prioritization

```
✅ Good: "Review for critical issues only"
✅ Good: "Focus on accessibility and Dynamic Type"
```

## Expected Output

### coding-best-practices Output

```
Reviewing: ExpenseViewModel.swift

✅ Strengths Found
- Excellent use of @Published properties
- Clean MVVM separation
- Good error handling

⚠️ Issues Found

**Category: Optionals Handling**
**High Priority: ExpenseViewModel.swift:45** - Force unwrapping
// Current: let payer = expense.payer!
// Suggested: guard let payer = expense.payer else { return }
// Reason: Force unwrapping crashes if nil

📊 Code Quality Score: 7/10

📋 Recommendations
1. High Priority: Remove force unwrapping
2. Medium Priority: Improve error handling
3. Low Priority: Use first(where:) instead of filter().first
```

### ui-review Output

```
Reviewing: AddExpenseView.swift

✅ HIG Compliance
- Good use of semantic colors
- Proper NavigationStack implementation
- Safe area handling correct

⚠️ Font Issues Found
1. AddExpenseView.swift:178 - Hardcoded font size
   Current: .font(.system(size: 14))
   Suggested: .font(.subheadline)

⚠️ Accessibility Issues Found
1. AddExpenseView.swift:92 - Icon button missing label
   Suggested: Add .accessibilityLabel("Select date")

📋 Testing Recommendations
1. Test with VoiceOver enabled
2. Test at largest Dynamic Type size
3. Verify in Dark Mode
```

## Troubleshooting

### Skill Not Activating

**Problem**: Claude doesn't use the skill when expected

**Solutions**:
1. Check skill is in `.claude/skills/` directory
2. Verify YAML front matter is valid
3. Use explicit trigger phrases from README
4. Try: "Use the [skill-name] skill to review this"

### Missing Reference Files

**Problem**: Skill references files that don't exist

**Solution**:
```bash
# Ensure all files copied
ls .claude/skills/coding-best-practices/
# Should show: SKILL.md, swift-patterns.md, swiftui-patterns.md, etc.
```

### Wrong Skill Activates

**Problem**: Different skill than expected activates

**Solution**:
- Be more specific in your request
- Use explicit skill names
- Check skill descriptions in README

## Next Steps

### Customize Skills

Edit skill files to match your project's standards:

```bash
# Edit coding standards
vim .claude/skills/coding-best-practices/swift-patterns.md

# Edit UI guidelines
vim .claude/skills/ui-review/hig-checklist.md
```

### Create Your Own Skill

Use the skill-creator to build custom skills:

```
You: "Help me create a skill for reviewing API error handling"
```

### Share Improvements

Found a bug or improvement?
1. Fork the repository
2. Make your changes
3. Submit a pull request

See [CONTRIBUTING.md](../CONTRIBUTING.md) for details.

## Resources

- [Full README](../README.md)
- [Contributing Guidelines](../CONTRIBUTING.md)
- [Skill Templates](../skills/skill-creator/)
- [Example Output](examples/)

## Getting Help

- Open an issue on GitHub
- Check existing issues for solutions
- Ask in Discussions tab
- Review skill documentation in SKILL.md files

## What's Next?

After getting comfortable with the basics:

1. **Explore All Features**
   - Read through reference files
   - Try different review scenarios
   - Experiment with skill customization

2. **Integrate into Workflow**
   - Add to pre-commit hooks
   - Use in PR reviews
   - Regular accessibility audits

3. **Contribute Back**
   - Report bugs
   - Suggest improvements
   - Create new skills
   - Help others in Discussions

---

**Questions?** Open an issue or start a discussion!

**Found this helpful?** Star the repository and share with other iOS developers!
