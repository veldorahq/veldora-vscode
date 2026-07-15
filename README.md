<div align="center">

<img src="images/v-icon.png" width="128" alt="Veldora Logo">

# Veldora Language Support

**Official Visual Studio Code extension for the Veldora PHP Framework.**

Syntax Highlighting • IntelliSense Snippets • File Icons • Language Configuration • Bracket Matching

<br>

[![Release](https://img.shields.io/github/v/release/veldorahq/veldora-vscode?style=flat-square)](https://github.com/veldorahq/veldora-vscode/releases)
[![Downloads](https://img.shields.io/github/downloads/veldorahq/veldora-vscode/total?style=flat-square)](https://github.com/veldorahq/veldora-vscode/releases)
[![Stars](https://img.shields.io/github/stars/veldorahq/veldora-vscode?style=flat-square)](https://github.com/veldorahq/veldora-vscode/stargazers)
[![Issues](https://img.shields.io/github/issues/veldorahq/veldora-vscode?style=flat-square)](https://github.com/veldorahq/veldora-vscode/issues)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=flat-square&logo=php&logoColor=white)](https://php.net)
[![License](https://img.shields.io/github/license/veldorahq/veldora-vscode?style=flat-square)](LICENSE)

</div>

---

# What is Veldora?

[Veldora](https://github.com/veldorahq/veldora) is a modern PHP framework focused on clean architecture, expressive syntax, built-in tooling, and an enjoyable developer experience.

The Veldora ecosystem includes:

- Framework Core
- UI Component Library
- CLI Tooling
- Documentation Website
- Visual Studio Code Extension

This extension provides first-class editor support for Veldora template files.

---

# Features

## ✦ Syntax Highlighting

Complete TextMate grammar with embedded PHP support.

Supports:

- Escaped output — `{{ }}`
- Raw output — `{!! !!}`
- Template comments — `{{-- --}}`
- Blade-inspired directives
- UI Components (`<x-button>`, `<x-card>`, etc.)
- Embedded PHP
- Control structures
- Authentication directives

---

## ✦ Smart IntelliSense Snippets

More than **30 snippets** are included to speed up development.

Categories include:

- Template directives
- Authentication
- CSRF
- Layouts
- Components
- UI Components

---

## ✦ File Icons

Recognizes Veldora projects with custom icons for:

- `.veldora`
- `.veldora.php`
- `.env`
- `web.php`
- `api.php`
- `routes.php`
- `veldora-core`
- `veldora-ui`
- `veldora-vscode`

---

## ✦ Language Configuration

Includes:

- Auto-closing brackets
- Auto indentation
- Comment toggling
- Bracket matching
- Embedded PHP parsing

---

# Snippet Reference

Type a prefix and press **Tab**.

| Prefix | Description |
|---------|-------------|
| `v-if` | Conditional block |
| `v-foreach` | Foreach loop |
| `v-forelse` | Foreach with empty state |
| `v-unless` | Inverse conditional |
| `v-for` | For loop |
| `v-while` | While loop |
| `v-php` | PHP block |
| `v-csrf` | CSRF directive |
| `v-auth` | Auth block |
| `v-guest` | Guest block |
| `v-admin` | Admin block |
| `v-dump` | Dump helper |
| `v-extends` | Extend layout |
| `v-section` | Section block |
| `v-yield` | Yield section |
| `v-comp` | Component block |
| `v-esc` | Escaped output |

---

# UI Component Snippets

| Prefix | Component |
|---------|-----------|
| `vc-button` | Button |
| `vc-input` | Input |
| `vc-textarea` | Textarea |
| `vc-select` | Select |
| `vc-checkbox` | Checkbox |
| `vc-radio` | Radio |
| `vc-badge` | Badge |
| `vc-alert` | Alert |
| `vc-card` | Card |
| `vc-modal` | Modal |
| `vc-spinner` | Spinner |
| `vc-avatar` | Avatar |
| `vc-dropdown` | Dropdown |
| `vc-navbar` | Navbar |
| `vc-toast` | Toast |

---

# Supported File Types

| File | Supported |
|------|-----------|
| `.veldora.php` | ✔ |
| `.veldora` | ✔ |

---

# Installation

## Visual Studio Code Marketplace (Recommended)

Search for:

```
Veldora Language Support
```

or install directly:

https://marketplace.visualstudio.com/items?itemName=veldora.veldora-vscode

---

## Command Line

```bash
code --install-extension veldora.veldora-vscode
```

---

## Manual (.vsix)

```bash
git clone https://github.com/veldorahq/veldora-vscode

cd veldora-vscode

npm install

npx @vscode/vsce package --no-dependencies

code --install-extension veldora-vscode-0.5.0.vsix
```

---

# Version History

## 0.5.0

- Published on Visual Studio Code Marketplace
- Added official Marketplace branding
- Added custom extension icon
- Added Marketplace banner
- Added file icons
- Improved extension metadata
- Updated documentation

## 0.4.1

- Added Veldora File Icon Theme
- Improved syntax grammar
- Updated extension packaging

## 0.3.0

- Added 15 UI Component snippets
- Improved registry support

## 0.2.0

- Added authentication snippets
- Added CSRF directive
- Added new template directives

## 0.1.0

- Initial release
- Syntax highlighting
- Blade-inspired directives
- Basic snippets
- Language configuration

---

# Contributing

Contributions are welcome.

Issues, pull requests, feature ideas, and bug reports can be submitted through GitHub.

Repository:

https://github.com/veldorahq/veldora-vscode

---

# License

Released under the MIT License.

See [LICENSE](LICENSE) for more information.
