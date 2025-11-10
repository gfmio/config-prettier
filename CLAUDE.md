# Prettier Configuration Project - Claude Expert Guide

## Project Overview

This is a shareable Prettier configuration package designed to enforce consistent code formatting across projects. It provides opinionated defaults and best practices for JavaScript, TypeScript, and related file types.

## Core Expertise Areas

### 1. Prettier Configuration Knowledge

- **Configuration Structure**: Understand all Prettier configuration options and their effects
- **Config Formats**: Support for `.prettierrc`, `.prettierrc.json`, `.prettierrc.js`, `prettier.config.js`, and `package.json` formats
- **Precedence Rules**: Know how Prettier resolves configuration from multiple sources
- **Shareable Configs**: Expertise in creating and maintaining shareable configs that can be extended
- **Version Compatibility**: Understand breaking changes and feature additions across Prettier versions

### 2. Key Configuration Options

When working with this project, be an expert on:

- **Print Width** (`printWidth`): Line wrapping behavior
- **Tab Width** (`tabWidth`): Indentation size
- **Tabs vs Spaces** (`useTabs`): Indentation character
- **Semicolons** (`semi`): Statement termination
- **Quotes** (`singleQuote`, `jsxSingleQuote`): String and JSX attribute quotes
- **Trailing Commas** (`trailingComma`): ES5, all, or none
- **Bracket Spacing** (`bracketSpacing`): Object literal spacing
- **Arrow Function Parens** (`arrowParens`): Always or avoid
- **End of Line** (`endOfLine`): lf, crlf, cr, or auto
- **Prose Wrap** (`proseWrap`): Markdown text wrapping
- **HTML Whitespace Sensitivity** (`htmlWhitespaceSensitivity`)
- **Embedded Language Formatting** (`embeddedLanguageFormatting`)

### 3. Plugin System

- **Official Plugins**: Be familiar with `@prettier/plugin-php`, `@prettier/plugin-ruby`, `@prettier/plugin-xml`
- **Community Plugins**: Know popular plugins like `prettier-plugin-organize-imports`, `prettier-plugin-tailwindcss`, `prettier-plugin-svelte`
- **Plugin Configuration**: Understand how to configure and integrate plugins
- **Plugin Order**: Handle plugin execution order and conflicts

### 4. File Type Support

- **JavaScript/TypeScript**: Core language support, JSX/TSX handling
- **JSON/JSONC**: JSON formatting with comment support
- **CSS/SCSS/Less**: Stylesheet formatting
- **HTML/Vue/Svelte**: Template and component files
- **Markdown/MDX**: Documentation and content files
- **YAML**: Configuration file formatting
- **GraphQL**: Query and schema formatting

### 5. Integration & Tooling

- **Package Structure**: Proper npm package setup for shareable configs
- **Peer Dependencies**: Correct Prettier version requirements
- **Editor Integration**: VSCode, WebStorm, Vim, etc.
- **CI/CD Integration**: GitHub Actions, GitLab CI, pre-commit hooks
- **Git Hooks**: Husky, lint-staged integration
- **Monorepo Support**: Handling multiple packages with shared configs

## Project-Specific Best Practices

### Package Development

1. **Versioning**: Follow semantic versioning strictly
   - Major: Breaking configuration changes
   - Minor: New options (backward compatible)
   - Patch: Bug fixes, documentation updates

2. **Testing**:
   - Test configuration with various file types
   - Verify config extends correctly
   - Test with different Prettier versions
   - Validate generated formatting output

3. **Documentation**:
   - Clear README with installation and usage
   - Document all configuration decisions and rationale
   - Provide migration guides for breaking changes
   - Include examples and common use cases

4. **Maintenance**:
   - Keep Prettier peer dependency up to date
   - Monitor Prettier releases for new options
   - Respond to community feedback and issues
   - Maintain backward compatibility when possible

### Code Quality Standards

- Use TypeScript for any scripts or utilities
- Maintain zero dependencies (except peer deps)
- Keep package size minimal
- Provide ESM and CommonJS exports if needed

### Configuration Philosophy

When making decisions about this config:

1. **Consistency Over Preference**: Choose options that minimize diffs and enhance readability
2. **Community Standards**: Align with popular conventions unless there's a strong reason not to
3. **Git Friendliness**: Prefer options that produce cleaner diffs (e.g., trailing commas)
4. **Editor Agnostic**: Configuration should work across all editors
5. **Performance**: Consider formatting speed for large codebases

## Common Tasks

### Adding New Configuration Options

1. Research the option in Prettier documentation
2. Consider the impact on existing formatted code
3. Evaluate community preferences and conventions
4. Document the decision rationale
5. Update version appropriately (major vs minor)
6. Test with representative code samples

### Handling Issues

1. Reproduce the formatting issue
2. Check Prettier version compatibility
3. Verify config is being loaded correctly
4. Test with minimal reproduction
5. Consider if issue is upstream in Prettier

### Publishing Updates

1. Update version in package.json
2. Update CHANGELOG.md with changes
3. Verify package contents (`npm pack`)
4. Test installation in a separate project
5. Publish to npm registry
6. Tag release in git

## Anti-Patterns to Avoid

1. **Over-configuration**: Don't expose every Prettier option unless necessary
2. **Breaking Changes**: Minimize breaking changes in minor versions
3. **Heavy Dependencies**: Avoid adding dependencies beyond Prettier
4. **Tight Coupling**: Don't couple to specific project structures
5. **Inconsistent Docs**: Keep README in sync with actual config
6. **Ignoring Peer Deps**: Always specify compatible Prettier versions

## Useful Commands Reference

```bash
# Test configuration locally
npm link
cd ../test-project && npm link @gfmio/config-prettier

# Format and check
prettier --config .prettierrc --check "**/*.{js,ts,json,md}"
prettier --config .prettierrc --write "**/*.{js,ts,json,md}"

# Package inspection
npm pack --dry-run
npm publish --dry-run

# Version management
npm version patch
npm version minor
npm version major
```

## Resources & Documentation

- [Prettier Official Docs](https://prettier.io/docs/en/)
- [Prettier Options](https://prettier.io/docs/en/options.html)
- [Prettier Configuration](https://prettier.io/docs/en/configuration.html)
- [Prettier Plugins](https://prettier.io/docs/en/plugins.html)
- [Shareable Configs](https://prettier.io/docs/en/configuration.html#sharing-configurations)

## Working with Claude

When requesting assistance:

- Specify the Prettier version you're targeting
- Mention any specific file types or languages
- Provide context about breaking vs non-breaking changes
- Include examples of desired formatting output
- Mention any integration requirements (CI, pre-commit, etc.)

I will prioritize:

- Configuration correctness and validity
- Clear documentation of choices
- Backward compatibility considerations
- Testing recommendations
- Community best practices
