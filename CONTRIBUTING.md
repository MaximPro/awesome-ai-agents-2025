# Contributing to Awesome AI Agents 2025

Thank you for your interest in contributing to this project! This document provides guidelines for contributing.

## Table of Contents

- [Code of Conduct](#code-of-conduct)
- [How to Contribute](#how-to-contribute)
- [Adding a Platform](#adding-a-platform)
- [Style Guide](#style-guide)
- [Pull Request Process](#pull-request-process)
- [Issue Guidelines](#issue-guidelines)

---

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Provide constructive feedback
- Focus on the content, not the person
- Accept responsibility for mistakes

### Unacceptable Behavior

- Harassment or discrimination
- Trolling or personal attacks
- Spam or promotional content
- False information

---

## How to Contribute

### Types of Contributions

1. **Add new platforms/tools**
2. **Update existing information**
3. **Fix errors or outdated data**
4. **Improve documentation**
5. **Add resources**

### Quick Contribution

1. Fork the repository
2. Create a branch: `git checkout -b feature/add-platform-name`
3. Make your changes
4. Submit a pull request

---

## Adding a Platform

### Criteria for Inclusion

Platforms must be:

- **Publicly available** (not private beta or closed access)
- **AI agent focused** (not just LLM APIs or chatbots)
- **Actively maintained** (updated within last 6 months)
- **Documented** (has public documentation)

### Required Information

When adding a platform, include:

```markdown
### Platform Name

**Category**: [Enterprise/No-Code/Framework/Specialized]
**Website**: [URL]
**Company**: [Company name]

#### Overview
Brief description (2-3 sentences)

#### Key Features
- Feature 1
- Feature 2
- Feature 3

#### Pricing
| Plan | Price | Features |
|------|-------|----------|
| Free | $0 | ... |
| Pro | $X/mo | ... |

#### Best Use Cases
1. Use case 1
2. Use case 2

#### Pros
- Pro 1
- Pro 2

#### Cons
- Con 1
- Con 2
```

### File Placement

Add platforms to the appropriate file:

| Type | File |
|------|------|
| Enterprise (large companies) | ENTERPRISE-PLATFORMS.md |
| Cloud providers | CLOUD-PLATFORMS.md |
| No-code/low-code | NO-CODE-BUILDERS.md |
| Domain-specific | SPECIALIZED-AGENTS.md |
| Developer frameworks | AGENTIC-FRAMEWORKS.md |

Also add to:
- README.md (summary table)
- COMPARISON-MATRIX.md (if relevant)

---

## Style Guide

### Formatting

- Use Markdown formatting
- Keep line length under 120 characters
- Use consistent heading levels
- Include links to official sources

### Language

- Write in clear, concise English
- Use active voice
- Be objective and factual
- Avoid marketing language
- No emojis in main content

### Tables

Use this format:

```markdown
| Column 1 | Column 2 | Column 3 |
|----------|----------|----------|
| Data 1   | Data 2   | Data 3   |
```

### Links

- Use descriptive link text
- Verify all links work
- Prefer official documentation
- Format: `[Link text](URL)`

### Pricing

- Use USD for consistency
- Clearly state pricing model
- Note if pricing is approximate
- Include free tier information

---

## Pull Request Process

### Before Submitting

1. **Check existing content** - Avoid duplicates
2. **Verify information** - Use official sources
3. **Test all links** - Ensure they work
4. **Follow style guide** - Consistent formatting

### PR Title Format

```
Add: Platform Name
Update: Platform Name - pricing info
Fix: Broken link in RESOURCES.md
Improve: Cloud platforms comparison
```

### PR Description Template

```markdown
## Description
Brief description of changes

## Type of Change
- [ ] New platform
- [ ] Update existing content
- [ ] Bug fix
- [ ] Documentation improvement

## Checklist
- [ ] Information is accurate
- [ ] All links work
- [ ] Follows style guide
- [ ] Added to relevant files
```

### Review Process

1. Maintainer reviews within 7 days
2. Address any requested changes
3. Approval needed from 1 maintainer
4. Merge after approval

---

## Issue Guidelines

### Bug Reports

When reporting issues:

1. Check if issue already exists
2. Provide specific details
3. Include links to verify

Template:

```markdown
## Issue
What's wrong?

## Location
File and section

## Expected
What should it say?

## Source
Link to official source
```

### Feature Requests

For suggesting new platforms:

```markdown
## Platform
Name and URL

## Category
Enterprise/No-Code/Framework/etc.

## Why Include
Brief justification

## Information Available
Links to documentation, pricing, etc.
```

---

## Updating Information

### What to Update

- Pricing changes
- New features
- Company changes
- Statistics and metrics

### Update Frequency

- Pricing: When changed
- Features: Quarterly
- Statistics: Annually (or major changes)

### Marking Updates

When making updates, note in commit:
```
Update: Platform Name - November 2025 pricing
```

---

## Recognition

Contributors will be recognized in:

- GitHub contributors list
- Annual acknowledgments
- Major contribution highlights

---

## Questions?

- Open an issue for questions
- Tag with "question" label
- We'll respond within 7 days

---

## License

By contributing, you agree that your contributions will be licensed under the MIT License.

---

Thank you for helping make this resource better for everyone!
