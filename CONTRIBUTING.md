# Contributing to OpenHAB Configuration

Thank you for your interest in contributing to the **Smart Swimming Pool OpenHAB Configuration** project!
🏠

This document provides guidelines for contributing to the project. Please read it
carefully before submitting your first pull request.

## Code of Conduct

This project adheres to the
[Contributor Covenant](https://www.contributor-covenant.org/version/1/4/code-of-conduct.html).
By participating, you are expected to uphold this code. Please report unacceptable
behavior to
[project maintainers](https://github.com/smart-swimmingpool/openhab-config/graphs/contributors).

See also: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md)

## How to Contribute

### Reporting Issues

- **Check existing issues**: Search
  [GitHub Issues](https://github.com/smart-swimmingpool/openhab-config/issues)
  before creating a new one
- **Use the issue template**: Provide detailed information about the issue
- **Include**:
  - OpenHAB version
  - Configuration files you're using
  - Error messages from logs
  - Screenshots (if UI-related)

### Suggesting Enhancements

- **Check the roadmap**: See [README.md](README.md) for planned features
- **Discuss first**: Open a
  [GitHub Discussion](https://github.com/smart-swimmingpool/smart-swimmingpool.github.io/discussions)
  to discuss your idea
- **Check for duplicates**: Search existing issues and PRs

### Submitting Pull Requests

- **Fork the repository**: Create your own fork
- **Create a feature branch**: Use descriptive branch names
  (e.g., `feat/add-energy-monitoring`)
- **Test your changes**: Verify the configuration works in OpenHAB
- **Update documentation**: Keep docs in sync with changes

## Getting Started

### Prerequisites

- [OpenHAB](https://www.openhab.org/) (v3.x or later recommended)
- MQTT broker (e.g., Mosquitto)
- Smart Swimming Pool Pool Controller running
- Basic knowledge of OpenHAB configuration

### Setting Up

```bash
# Clone the repository
git clone https://github.com/smart-swimmingpool/openhab-config.git
cd openhab-config

# Copy configuration files to your OpenHAB conf directory
# Typically: /etc/openhab/conf (Linux) or C:\openHAB\conf (Windows)
```text

## Project Structure

```text
openhab-config/
├── items/               # Item definitions
│   ├── 1-groups.items  # Group items
│   └── 2-pool.items    # Pool-specific items
├── rules/               # Rule definitions
│   ├── pool.rules      # Main pool rules
│   └── pool-energy.rules # Energy monitoring rules
├── sitemaps/            # Sitemap definitions
│   └── pool.sitemap    # Main sitemap
├── persistence/         # Persistence configurations
│   └── pool.persist    # Persistence configuration
├── services/            # Service configurations
│   └── mqtt.cfg        # MQTT configuration
├── things/              # Thing definitions
│   └── pool.things     # Pool things
└── transform/           # Transformation scripts
    └── pool.transform  # Transformation rules
```text

## Configuration Guidelines

### Item Naming

- Use descriptive names: `Pool_Pump_State` instead of `Pump1`
- Group related items: `Pool_Temperature_Pool`, `Pool_Temperature_Solar`
- Use consistent naming conventions throughout

### Rule Development

- Add comments explaining complex logic
- Use meaningful variable names
- Handle errors gracefully
- Test rules thoroughly before committing

### Sitemap Design

- Group related items together
- Use consistent widget types
- Add labels for clarity
- Consider mobile usability

## Pull Request Process

1. **Fork the repository** and create your branch from `master`
2. **Make your changes** following the guidelines above
3. **Test in OpenHAB**: Verify your configuration works
4. **Update documentation** if applicable
5. **Commit your changes** with clear, descriptive messages
6. **Push to your fork** and submit a pull request

### Pull Request Requirements

- Configuration files are valid OpenHAB syntax
- All items, rules, and sitemaps are properly formatted
- Documentation is updated
- Clear commit messages

## Commit Message Guidelines

### Format

```text
type(scope): subject

body

footer
```text

### Types
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Formatting changes (no functional changes)
- `refactor`: Configuration restructuring
- `chore`: Maintenance tasks

### Example
```text
feat(energy): add energy monitoring for pool pump

- Add energy monitoring items
- Create energy calculation rules
- Add energy display to sitemap

Closes #123
```text

## Quality Gates

All contributions must pass the following quality checks:

1. **Super-Linter**: Code quality and style checks
2. **Manual Review**: Configuration review by maintainers

## Thank You!

Your contributions help make this configuration better for everyone. We appreciate your
time and effort in improving the Smart Swimming Pool OpenHAB Configuration!

## Additional Resources

- [OpenHAB Documentation](https://www.openhab.org/docs/)
- [Smart Swimming Pool Website](https://smart-swimmingpool.com)
- [GitHub Discussions](https://github.com/smart-swimmingpool/smart-swimmingpool.github.io/discussions)
- [Pool Controller MQTT Topics](https://github.com/smart-swimmingpool/pool-controller/blob/main/docs/mqtt-configuration.md)
