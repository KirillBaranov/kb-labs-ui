# KB Labs UI (@kb-labs/ui)

> **Shared UI component library for KB Labs ecosystem.** Framework-agnostic design system foundation with React component implementations.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Node.js](https://img.shields.io/badge/Node.js-18.18.0+-green.svg)](https://nodejs.org/)
[![pnpm](https://img.shields.io/badge/pnpm-9.0.0+-orange.svg)](https://pnpm.io/)

## 🎯 Vision

KB Labs UI provides a shared UI component library for the KB Labs ecosystem. It offers framework-agnostic design tokens and React component implementations, enabling consistent design and user experience across all KB Labs products.

The project solves the problem of inconsistent UI components and design systems across multiple KB Labs products by providing a unified component library with consistent design tokens, themes, and component implementations. Instead of each product maintaining its own UI components, developers can use KB Labs UI for consistent design and user experience.

This project is part of the **@kb-labs** ecosystem and integrates seamlessly with Studio, Core, DevKit, and all other KB Labs tools.

## 🚀 Quick Start

### Installation

```bash
# Clone repository
git clone https://github.com/kirill-baranov/kb-labs-ui.git
cd kb-labs-ui

# Install dependencies
pnpm install
```

### Development

```bash
# Start development mode for all packages
pnpm dev

# Build all packages
pnpm build

# Run tests
pnpm test

# Lint code
pnpm lint
```

### Creating a New Package

```bash
# Using the CLI tool (recommended)
pnpm dlx @kb-labs/create-pkg my-new-pkg

# Or manually copy and modify
cp -r packages/package-name packages/<new-package-name>
# Then update metadata and imports
```

## ✨ Features

- **Framework-agnostic Design Tokens**: CSS variables and design tokens that work with any framework
- **React Component Library**: Reusable React components with TypeScript support
- **Theme System**: Light/dark theme support with CSS variables
- **Consistent Design**: Unified design system across all KB Labs products
- **TypeScript Support**: Full TypeScript definitions for all components
- **DevKit Integration**: Shared configurations via `@kb-labs/devkit`

## 📁 Repository Structure

```
kb-labs-ui/
├── apps/                    # Demo applications
│   └── demo/                # Example app / playground
├── packages/                # Core packages
│   └── package-name/        # Example package (lib/cli/adapter)
├── fixtures/                # Fixtures for snapshot/integration testing
├── docs/                    # Documentation
│   └── adr/                 # Architecture Decision Records (ADRs)
└── scripts/                 # Utility scripts
```

### Directory Descriptions

- **`apps/`** - Demo applications demonstrating UI component usage
- **`packages/`** - Core UI packages (components, tokens, themes)
- **`fixtures/`** - Test fixtures for snapshot and integration testing
- **`docs/`** - Documentation including ADRs and guides

## 📦 Packages

| Package | Description |
|---------|-------------|
| [@kb-labs/ui-core](./packages/ui-core/) | Framework-agnostic design tokens and themes |
| [@kb-labs/ui-react](./packages/ui-react/) | React component library |

### Package Details

**@kb-labs/ui-core** provides the design system foundation:
- Design tokens (colors, spacing, typography, radius, shadows)
- Theme system (light/dark) with CSS variable generator
- Framework-agnostic design system

**@kb-labs/ui-react** provides React components:
- Reusable UI components with TypeScript support
- Theme integration via CSS variables
- Consistent design patterns across KB Labs products

## 🛠️ Available Scripts

| Script | Description |
|--------|-------------|
| `pnpm dev` | Start development mode for all packages |
| `pnpm build` | Build all packages |
| `pnpm build:clean` | Clean and build all packages |
| `pnpm test` | Run all tests |
| `pnpm test:watch` | Run tests in watch mode |
| `pnpm lint` | Lint all code |
| `pnpm lint:fix` | Fix linting issues |
| `pnpm type-check` | TypeScript type checking |
| `pnpm check` | Run lint, type-check, and tests |
| `pnpm ci` | Full CI pipeline (clean, build, check) |
| `pnpm clean` | Clean build artifacts |
| `pnpm clean:all` | Clean all node_modules and build artifacts |

### DevKit Commands

| Script | Description |
|--------|-------------|
| `pnpm devkit:sync` | Sync DevKit configurations to workspace |
| `pnpm devkit:check` | Check if DevKit sync is needed |
| `pnpm devkit:force` | Force DevKit sync (overwrite existing) |
| `pnpm devkit:help` | Show DevKit sync help |

## 🔧 DevKit Integration

This project uses `@kb-labs/devkit` for shared tooling and configurations. DevKit provides:

- **Unified Configurations**: ESLint, Prettier, TypeScript, Vitest, and TSUP configs
- **Automatic Sync**: Keeps workspace configs in sync with latest DevKit versions
- **Zero Maintenance**: No need to manually update config files

### DevKit Commands Usage

- **`pnpm devkit:sync`** - Syncs DevKit configurations to your workspace (runs automatically on `pnpm install`)
- **`pnpm devkit:check`** - Checks if your workspace configs are up-to-date with DevKit
- **`pnpm devkit:force`** - Forces sync even if local files exist (overwrites local changes)
- **`pnpm devkit:help`** - Shows detailed help and available options

For more details, see [ADR-0005: Use DevKit for Shared Tooling](docs/adr/0005-use-devkit-for-shared-tooling.md).

## 📋 Development Policies

- **Code Style**: ESLint + Prettier, TypeScript strict mode
- **Testing**: Vitest with fixtures for integration testing
- **Versioning**: SemVer with automated releases through Changesets
- **Architecture**: Document decisions in ADRs (see `docs/adr/`)
- **Tooling**: Shared configurations via `@kb-labs/devkit`

## 🔧 Requirements

- **Node.js**: >= 18.18.0
- **pnpm**: >= 9.0.0

## 📚 Documentation

- [Documentation Standard](./docs/DOCUMENTATION.md) - Full documentation guidelines
- [Contributing Guide](./CONTRIBUTING.md) - How to contribute
- [Architecture Decisions](./docs/adr/) - ADRs for this project

## 🔗 Related Packages

### Dependencies

- [@kb-labs/core](https://github.com/KirillBaranov/kb-labs-core) - Core utilities
- [@kb-labs/devkit](https://github.com/KirillBaranov/kb-labs-devkit) - DevKit presets

### Used By

- [kb-labs-studio](https://github.com/KirillBaranov/kb-labs-studio) - Web dashboard
- Other KB Labs projects requiring UI components

### Ecosystem

- [KB Labs](https://github.com/KirillBaranov/kb-labs) - Main ecosystem repository

## 🤝 Contributing

See [CONTRIBUTING.md](./CONTRIBUTING.md) for development guidelines and contribution process.

## 📄 License

MIT © KB Labs

---

**See [CONTRIBUTING.md](./CONTRIBUTING.md) for development guidelines and contribution process.**

## License

KB Public License v1.1 - see [LICENSE](LICENSE) for details.

This is open source software with some restrictions on:
- Offering as a hosted service (SaaS/PaaS)
- Creating competing platform products

For commercial licensing inquiries: contact@kblabs.dev

**User Guides:**
- [English Guide](../LICENSE-GUIDE.en.md)
- [Русское руководство](../LICENSE-GUIDE.ru.md)
