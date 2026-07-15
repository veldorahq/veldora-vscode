<div align="center">

# Veldora Language Support

**Syntax highlighting, snippets, and bracket matching for Veldora PHP template files.**

[![Version](https://img.shields.io/badge/version-0.2.0-7c3aed?style=flat-square)](https://github.com/veldora/veldora-vscode)
[![License](https://img.shields.io/badge/license-MIT-gray?style=flat-square)](LICENSE)
[![PHP](https://img.shields.io/badge/PHP-8.2+-7c3aed?style=flat-square&logo=php&logoColor=white)](https://php.net)

</div>

---

## What is Veldora?

[Veldora](https://github.com/veldora/veldora-core) is a modern PHP framework built around a clean MVC architecture, a Blade-inspired template engine, a guard-based authentication system, and a CLI scaffolding toolkit — designed to be fully owned by the developer.

This extension adds first-class editor support for `.veldora.php` and `.veldora` template files.

---

## Features

### ✦ Syntax Highlighting

Full TextMate grammar covering all Veldora template syntax:

- **Escaped output** — `{{ $expression }}` highlighted as embedded PHP
- **Raw output** — `{!! $raw !!}` highlighted separately
- **Template comments** — `{{-- hidden --}}` grayed out as block comments
- **Control directives** — `@if`, `@foreach`, `@auth`, `@csrf`, `@php`, and more highlighted as keywords
- **Component tags** — `<x-tag>`, `<x-slot>` highlighted as custom elements

### ✦ Snippets

17 smart snippets auto-complete the most common Veldora patterns. All snippets use tab stops and placeholders.

### ✦ Language Configuration

Correct bracket pairing, auto-close behavior, and comment toggling for Veldora template syntax.

---

## Snippet Reference

Type the prefix and press `Tab` to expand.

| Prefix | Expands To | Description |
|---|---|---|
| `v-if` | `@if ... @endif` | Conditional block |
| `v-foreach` | `@foreach ... @endforeach` | Foreach loop |
| `v-forelse` | `@forelse ... @empty ... @endforelse` | Loop with empty fallback |
| `v-unless` | `@unless ... @endunless` | Inverse conditional |
| `v-for` | `@for ... @endfor` | Classic for loop |
| `v-while` | `@while ... @endwhile` | While loop |
| `v-php` | `@php ... @endphp` | Inline PHP block |
| `v-csrf` | `@csrf` | Hidden CSRF input |
| `v-auth` | `@auth ... @endauth` | Show only to logged-in users |
| `v-guest` | `@guest ... @endguest` | Show only to guests |
| `v-admin` | `@admin ... @endadmin` | Show only to admins |
| `v-dump` | `@dump($var)` | Debug variable dump |
| `v-extends` | `@extends('layout')` | Extend a layout |
| `v-section` | `@section('name') ... @endsection` | Define a layout section |
| `v-yield` | `@yield('name')` | Output a layout section |
| `v-comp` | `<x-component> ... </x-component>` | Custom component block |
| `v-esc` | `{{ $variable }}` | Escaped output |

---

## Supported File Extensions

| Extension | Description |
|---|---|
| `.veldora.php` | Primary template extension |
| `.veldora` | Alternative short extension |

---

## Installation

### From VSIX (recommended for local development)

```bash
# Build from source
cd veldora-vscode
npx @vscode/vsce package --no-dependencies

# Install into VS Code
code --install-extension veldora-vscode-0.2.0.vsix
```

### From VS Code Marketplace
> Coming soon — will be published when the framework reaches public release.

---

## Version History

### `0.2.0` — Phase 3: Security & Auth Directives
- Added snippets: `v-csrf`, `v-auth`, `v-guest`, `v-admin`, `v-unless`, `v-forelse`, `v-for`, `v-while`, `v-php`, `v-dump`
- Updated syntax grammar to highlight all new Phase 3 control keywords
- Added this `README.md`

### `0.1.0` — Phase 2: Template Engine Launch
- Initial release
- Syntax highlighting for `{{ }}`, `{!! !!}`, `{{-- --}}`, and core directives
- Basic snippets: `v-if`, `v-foreach`, `v-section`, `v-yield`, `v-extends`, `v-comp`, `v-esc`
- Language configuration with bracket matching

---

## Contributing

This extension lives inside the main [veldora](https://github.com/veldora/veldora) monorepo under `/veldora-vscode`. The grammar file is `syntaxes/veldora.tmLanguage.json` and snippets live in `snippets/snippets.json`.

---

## License

MIT — see [LICENSE](LICENSE) for details.
