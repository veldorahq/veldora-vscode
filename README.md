<div align="center">

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

</div>

---

## What is Veldora?

[Veldora](https://github.com/veldorahq/veldora-vscode) is a modern PHP framework built around a clean MVC architecture, a Blade-inspired template engine, guard-based authentication, a CLI scaffolding toolkit, and a 15-component UI system — fully owned by the developer.

This extension adds **first-class editor support** for `.veldora.php` and `.veldora` template files.

---

## Features

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

---

## Installation

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

---

## Version History

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

---

## License

MIT — see [LICENSE](LICENSE) for details.
