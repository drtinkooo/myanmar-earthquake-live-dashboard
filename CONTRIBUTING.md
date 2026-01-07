# Contributing to Myanmar Earthquake Dashboard

Thank you for your interest in contributing to the Myanmar Earthquake Dashboard! This document provides guidelines and instructions for contributing.

## Code of Conduct

By participating in this project, you agree to maintain a respectful and inclusive environment for everyone.

## How to Contribute

### Reporting Bugs

If you find a bug, please open an issue with:

1. **Clear title**: Summarize the issue
2. **Description**: Detailed explanation of the problem
3. **Steps to reproduce**: How to recreate the issue
4. **Expected behavior**: What should happen
5. **Actual behavior**: What actually happens
6. **Browser/OS**: Your environment details
7. **Screenshots**: If applicable

### Suggesting Features

We welcome feature suggestions! Please open an issue with:

1. **Feature description**: What you'd like to add
2. **Use case**: Why this feature would be useful
3. **Possible implementation**: Any ideas on how to implement it

### Pull Requests

#### Getting Started

1. **Fork the repository**
   ```bash
   # Click "Fork" on GitHub, then clone your fork
   git clone https://github.com/YOUR_USERNAME/myanmar-earthquake-dashboard.git
   cd myanmar-earthquake-dashboard
   ```

2. **Create a branch**
   ```bash
   git checkout -b feature/your-feature-name
   # or
   git checkout -b fix/your-bug-fix
   ```

3. **Make your changes**
   - Write clean, readable code
   - Follow existing code style
   - Test your changes in multiple browsers

4. **Commit your changes**
   ```bash
   git add .
   git commit -m "Add: brief description of your changes"
   ```

5. **Push to your fork**
   ```bash
   git push origin feature/your-feature-name
   ```

6. **Open a Pull Request**
   - Go to the original repository
   - Click "New Pull Request"
   - Select your branch
   - Fill in the PR template

#### Commit Message Guidelines

Use clear, descriptive commit messages:

- `Add: new feature description`
- `Fix: bug description`
- `Update: what was updated`
- `Remove: what was removed`
- `Refactor: what was refactored`
- `Docs: documentation changes`

#### Pull Request Guidelines

- **One feature/fix per PR**: Keep PRs focused
- **Update documentation**: If your change affects usage
- **Test thoroughly**: Check different browsers and scenarios
- **Describe your changes**: Explain what and why

## Development Guidelines

### Code Style

Since this is a single-file HTML application:

1. **HTML**
   - Use semantic elements where appropriate
   - Keep indentation consistent (4 spaces)
   - Add comments for complex sections

2. **CSS**
   - Use meaningful class names
   - Group related styles together
   - Use CSS variables for repeated values

3. **JavaScript**
   - Use `const` and `let` (no `var`)
   - Write descriptive function names
   - Add comments for complex logic
   - Handle errors gracefully

### Testing Checklist

Before submitting a PR, verify:

- [ ] Dashboard loads without errors
- [ ] Earthquake data fetches correctly
- [ ] Map displays and is interactive
- [ ] Filters work as expected
- [ ] Tectonic layer toggles properly
- [ ] Chart renders correctly
- [ ] Earthquake list is clickable
- [ ] Works in Chrome, Firefox, Safari, and Edge
- [ ] No console errors

## Areas for Contribution

### Beginner-Friendly

- Fix typos in documentation
- Improve code comments
- Add CSS improvements
- Enhance responsive design

### Intermediate

- Add new filters (depth, time of day)
- Implement earthquake notifications
- Add data export (CSV/JSON)
- Create keyboard shortcuts

### Advanced

- Add historical data comparison
- Implement offline caching (Service Worker)
- Add multiple region support
- Create unit tests

## Questions?

If you have questions about contributing:

1. Check existing issues for similar questions
2. Open a new issue with the "question" label
3. Be patient - maintainers are volunteers

## Recognition

Contributors will be recognized in:
- The repository's contributor list
- Release notes when applicable

Thank you for helping improve the Myanmar Earthquake Dashboard!
