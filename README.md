# Bedrock Module Template Web _(bedrock-module-template-web)_

A template repository for creating new @bedrock/web-* packages with standardized structure, testing setup, and CI/CD configuration.

## Table of Contents

- [Background](#background)
- [Security](#security)
- [Usage](#usage)
  - [1. Create New Repository](#1-create-new-repository)
  - [2. Configure Repository Settings](#2-configure-repository-settings)
  - [3. Customize Package Files](#3-customize-package-files)
  - [4. Development Workflow](#4-development-workflow)
- [Package Structure](#package-structure)
- [Key Features Included](#key-features-included)
  - [ESLint Configuration](#eslint-configuration)
  - [Testing Setup](#testing-setup)
  - [CI/CD Pipeline](#cicd-pipeline)
- [Requirements for New Packages](#requirements-for-new-packages)
  - [Naming Convention](#naming-convention)
  - [Code Standards](#code-standards)
  - [Documentation](#documentation)
- [Contribute](#contribute)
- [Commercial Support](#commercial-support)
- [License](#license)

## Background

This template provides the foundation for creating browser-compatible Bedrock modules with:

- ✅ Standard Bedrock web package structure
- ✅ ESLint configuration with Digital Bazaar standards
- ✅ GitHub Actions CI/CD pipeline
- ✅ Proper licensing and documentation templates
- ✅ ESM module configuration

## Security

TBD

## Usage

### 1. Create New Repository

1. Click the **"Use this template"** button above
2. Choose repository name following pattern: `bedrock-web-{module-name}`
3. Make it **public**
4. Create the repository

### 2. Configure Repository Settings

After creation, configure these settings in your new repo:

**Settings → General:**

- Disable "Allow merge commits"
- Disable "Allow squash merging" 
- Keep only "Allow rebase merging"

**Settings → Branches:**

- Add protection rule for `main` branch
- Enable "Require linear history"
- Enable "Restrict pushes that create files"

### 3. Customize Package Files

**Update `package.json`:**

```json
{
  "name": "@bedrock/web-{your-module-name}",
  "version": "1.0.0-0",
  "description": "Your module description",
  "exports": "./lib/index.js"
}
```

**Update `README.md`:**

- Replace with your module's documentation
- Include installation and usage examples
- Document API and features

**Update `lib/index.js`:**

- Implement your module's main exports
- Follow ESM module patterns

**Update test files:**

- Replace placeholder tests with your module's tests
- Update `test/package.json` with correct package reference

### 4. Development Workflow

1. **Install dependencies:**

   ```bash
   npm install
   ```

2. **Run linting:**

   ```bash
   npm run lint
   ```

3. **Run tests:**

   ```bash
   cd test
   npm install
   npm test
   ```

## Package Structure

```
your-new-package/
├── .github/
│   └── workflows/
│       └── main.yml              # CI/CD pipeline
├── lib/
│   ├── index.js                  # Main export file
│   └── ...                       # Your module files
├── test/
│   ├── web/                      # Browser tests
│   │   └── *.js
│   ├── package.json              # Test dependencies
│   ├── test.js                   # Test runner
│   └── test.config.js            # Test configuration
├── .eslintrc.cjs                 # ESLint configuration
├── .gitignore
├── CHANGELOG.md                  # Version history
├── LICENSE.md                    # Bedrock Non-Commercial License
├── README.md                     # Package documentation
└── package.json                  # Package metadata
```

## Key Features Included

### ESLint Configuration

- Uses `eslint-config-digitalbazaar`
- Configured for browser and Node.js environments (TBD for Node.js)
- Includes JSDoc and unicorn plugins

### Testing Setup

- Bedrock test framework integration
- GitHub Actions for automated testing

### CI/CD Pipeline

- Automated linting and testing
- Node.js 22.x support

## Requirements for New Packages

### Naming Convention

- Package name: `@bedrock/web-{module-name}`
- Repository name: `bedrock-web-{module-name}`
- Use kebab-case for module names

### Code Standards

- Use ES modules (ESM) only
- Follow Digital Bazaar ESLint configuration
- Write comprehensive JSDoc comments
- Include unit and integration tests

### Documentation

- Clear README with usage examples
- API documentation for all public methods
- Update CHANGELOG.md for each release

## Contribute

See [the contribute file](https://github.com/digitalbazaar/bedrock/blob/master/CONTRIBUTING.md)!

PRs accepted.

If editing the Readme, please conform to the
[standard-readme](https://github.com/RichardLitt/standard-readme) specification.

## Commercial Support

Commercial support for this library is available upon request from
Digital Bazaar: support@digitalbazaar.com

## License

[Bedrock Non-Commercial License v1.0](LICENSE.md) © Digital Bazaar