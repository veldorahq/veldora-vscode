<div align="center">

<<<<<<< HEAD
<br/>

<img src="https://img.shields.io/badge/Veldora-Language%20Support-7c3aed?style=for-the-badge&labelColor=09090b" alt="Veldora Language Support"/>

<br/><br/>

**Syntax highlighting, IntelliSense snippets, and bracket matching for Veldora PHP template files.**

<br/>

[![Version](https://img.shields.io/badge/version-0.4.0-7c3aed?style=flat-square&labelColor=18181b)](https://github.com/veldorahq/veldora-vscode/releases/latest)
[![License](https://img.shields.io/badge/license-MIT-52525b?style=flat-square&labelColor=18181b)](LICENSE)
[![PHP](https://img.shields.io/badge/PHP-8.2+-7c3aed?style=flat-square&labelColor=18181b&logo=php&logoColor=white)](https://php.net)
[![VS Code](https://img.shields.io/badge/VS%20Code-1.60+-52525b?style=flat-square&labelColor=18181b&logo=visualstudiocode&logoColor=white)](https://code.visualstudio.com)
[![Downloads](https://img.shields.io/github/downloads/veldorahq/veldora-vscode/total?style=flat-square&labelColor=18181b&color=52525b)](https://github.com/veldorahq/veldora-vscode/releases)
[![Latest Release](https://img.shields.io/github/v/release/veldorahq/veldora-vscode?style=flat-square&labelColor=18181b&color=7c3aed)](https://github.com/veldorahq/veldora-vscode/releases/latest)
=======
<img src="images/v-icon.png" width="128" alt="Veldora Logo">

# Veldora Language Support

**Official Visual Studio Code extension for the Veldora PHP Framework.**

Syntax Highlighting • IntelliSense Snippets • File Icons • Language Configuration • Bracket Matching

<br>

[![Marketplace](https://img.shields.io/visual-studio-marketplace/v/veldora.veldora-vscode?style=flat-square&logo=visualstudiocode&color=7c3aed)](https://marketplace.visualstudio.com/items?itemName=veldora.veldora-vscode)
[![Downloads](https://img.shields.io/visual-studio-marketplace/d/veldora.veldora-vscode?style=flat-square&color=7c3aed)](https://marketplace.visualstudio.com/items?itemName=veldora.veldora-vscode)
[![Rating](https://img.shields.io/visual-studio-marketplace/r/veldora.veldora-vscode?style=flat-square&color=7c3aed)](https://marketplace.visualstudio.com/items?itemName=veldora.veldora-vscode)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=flat-square&logo=php&logoColor=white)](https://php.net)
[![License](https://img.shields.io/badge/license-MIT-gray?style=flat-square)](LICENSE)
>>>>>>> 8d1cda1090c2fb8b208c620be548519042d665cd

</div>

---

# What is Veldora?

<<<<<<< HEAD
[Veldora](https://github.com/veldorahq/veldora-vscode) is a modern PHP framework built around a clean MVC architecture, a Blade-inspired template engine, guard-based authentication, a CLI scaffolding toolkit, and a 15-component UI system — fully owned by the developer.

This extension adds **first-class editor support** for `.veldora.php` and `.veldora` template files.
=======
[Veldora](https://github.com/veldorahq/veldora) is a modern PHP framework focused on clean architecture, expressive syntax, built-in tooling, and an enjoyable developer experience.

The Veldora ecosystem includes:

- Framework Core
- UI Component Library
- CLI Tooling
- Documentation Website
- Visual Studio Code Extension

This extension provides first-class editor support for Veldora template files.
>>>>>>> 8d1cda1090c2fb8b208c620be548519042d665cd

---

# Features

<<<<<<< HEAD
### Syntax Highlighting

Full TextMate grammar covering all Veldora template syntax with proper PHP embedding:

| Syntax | Example | Description |
|---|---|---|
| Escaped output | `{{ $expression }}` | Highlighted as embedded PHP |
| Raw output | `{!! $html !!}` | Unescaped raw output |
| Template comments | `{{-- hidden --}}` | Grayed-out block comment |
| Control directives | `@if`, `@foreach`, `@auth` | Keyword highlighting |
| Closing directives | `@endif`, `@endforeach` | Separate scope coloring |
| PHP blocks | `<?php ?>`, `<?= ?>` | Full PHP syntax coloring |
| Component tags | `<x-button>`, `<x-slot>` | Custom element highlighting |

### File Icon Theme

Activate **Veldora Icons** via `File > Preferences > File Icon Theme > Veldora Icons`.

| Pattern | Icon |
|---|---|
| `*.veldora.php`, `*.veldora` | Violet lightning bolt file icon |
| `web.php`, `api.php`, `routes.php` | Blue arrows routes icon |
| `.env`, `.env.*` | Green lock secrets icon |
| `veldora-core/`, `veldora-ui/` folders | Violet Veldora folder icon |

### Code Snippets

**57 smart snippets** — all use tab stops and placeholders for fast editing.

#### Template Directives (`v-` prefix)

| Prefix | Expands To |
|---|---|
| `v-if` | `@if ... @endif` |
| `v-foreach` | `@foreach ... @endforeach` |
| `v-forelse` | `@forelse ... @empty ... @endforelse` |
| `v-unless` | `@unless ... @endunless` |
| `v-for` | `@for ... @endfor` |
| `v-while` | `@while ... @endwhile` |
| `v-php` | `@php ... @endphp` |
| `v-csrf` | `@csrf` hidden input |
| `v-auth` | `@auth ... @endauth` |
| `v-guest` | `@guest ... @endguest` |
| `v-admin` | `@admin ... @endadmin` |
| `v-dump` | `@dump($var)` |
| `v-extends` | `@extends('layout')` |
| `v-section` | `@section ... @endsection` |
| `v-yield` | `@yield('name')` |
| `v-comp` | `<x-component> ... </x-component>` |
| `v-esc` | `{{ $variable }}` |

#### UI Components (`vc-` prefix)

| Prefix | Expands To |
|---|---|
| `vc-button` | Button component |
| `vc-input` | Input field |
| `vc-textarea` | Textarea |
| `vc-select` | Select dropdown |
| `vc-checkbox` | Checkbox |
| `vc-radio` | Radio group |
| `vc-badge` | Badge |
| `vc-alert` | Alert box |
| `vc-card` | Card panel |
| `vc-modal` | Modal dialog |
| `vc-spinner` | Loading spinner |
| `vc-avatar` | Avatar image |
| `vc-dropdown` | Dropdown menu |
| `vc-navbar` | Navbar |
| `vc-toast` | Toast notification |

### Language Configuration

Correct bracket pairing, auto-close behavior, and comment toggling for Veldora template syntax.

---

## Supported File Extensions

| Pattern | Description |
|---|---|
| `*.veldora.php` | Primary template extension |
| `*.veldora` | Alternative short extension |

> VS Code multi-part extensions (like `.veldora.php`) are matched via `filenamePatterns`, not the `extensions` array — this is why v0.3.1 was required to fix highlighting.
=======
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
>>>>>>> 8d1cda1090c2fb8b208c620be548519042d665cd

---

## ✦ Language Configuration

<<<<<<< HEAD
### From VSIX (recommended)

Download the latest `.vsix` from [Releases](https://github.com/veldorahq/veldora-vscode/releases/latest), then:

```bash
code --install-extension veldora-vscode-0.3.1.vsix
```

Reload VS Code (`Ctrl+Shift+P` → **Reload Window**) after installing.

### From Source

```bash
git clone https://github.com/veldorahq/veldora-vscode
cd veldora-vscode
npx @vscode/vsce package --no-dependencies
code --install-extension veldora-vscode-0.3.1.vsix
```

### From VS Code Marketplace

> Coming soon — will be published when the framework reaches public release.
=======
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
>>>>>>> 8d1cda1090c2fb8b208c620be548519042d665cd

---

## Command Line

<<<<<<< HEAD
### `0.4.0` — File Icon Theme *(latest)*

- Added **Veldora Icons** file icon theme (`File > Preferences > File Icon Theme`)
- Custom SVG icon for `*.veldora.php` and `*.veldora` files (violet lightning bolt)
- Custom icon for `web.php` / `api.php` / `routes.php` (blue route arrows)
- Custom icon for `.env` files (green lock)
- Custom folder icons for Veldora project directories
- Bumped `categories` to include `Themes`

### `0.3.1` — Syntax Highlighting Fix

- Fixed `.veldora.php` files showing as plain text — VS Code multi-part extension limitation resolved via `filenamePatterns`
- Upgraded tmLanguage grammar: PHP blocks (`<?php ?>`, `<?= ?>`) now embed with full PHP syntax coloring
- Fixed `embeddedLanguages` scopes for PHP IntelliSense inside templates
- `@directives` split into control-flow and closing groups for more accurate coloring

### `0.3.0` — UI Component Snippets

- Added 15 `vc-` prefix snippets for all Veldora UI components (`vc-button`, `vc-modal`, `vc-toast`, etc.)
- Component snippets include all required props with tab-stop placeholders
- Snippet total: 17 directive + 15 UI = **32 total**

### `0.2.0` — Security & Auth Directives

- Added snippets: `v-csrf`, `v-auth`, `v-guest`, `v-admin`, `v-unless`, `v-forelse`, `v-for`, `v-while`, `v-php`, `v-dump`
- Updated syntax grammar to highlight all Phase 3 control keywords
- Added `README.md`

### `0.1.0` — Initial Release

- Syntax highlighting for `{{ }}`, `{!! !!}`, `{{-- --}}`, and core directives
- Basic snippets: `v-if`, `v-foreach`, `v-section`, `v-yield`, `v-extends`, `v-comp`, `v-esc`
- Language configuration with bracket matching

---

## Repository Structure

```
veldora-vscode/
├── syntaxes/
│   └── veldora.tmLanguage.json   # TextMate grammar
├── snippets/
│   └── snippets.json             # All 32 snippets
├── download/
│   ├── v0.1.0/                   # VSIX archive
│   ├── v0.2.0/
│   ├── v0.3.0/
│   └── v0.3.1/                   # Latest
├── language-configuration.json   # Bracket/comment config
└── package.json
```

---

## Contributing

This extension lives inside the [veldorahq/veldora-vscode](https://github.com/veldorahq/veldora-vscode) repository.

- Grammar file: `syntaxes/veldora.tmLanguage.json`
- Snippets: `snippets/snippets.json`
- Build: `npx @vscode/vsce package --no-dependencies`
=======
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
>>>>>>> 8d1cda1090c2fb8b208c620be548519042d665cd

---

# License

Released under the MIT License.

See [LICENSE](LICENSE) for more information.
