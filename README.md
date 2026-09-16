# hostman

[English](README.md) · [한국어](README.ko.md)

**hostman** is a fast, account-free desktop client for HTTP, WebSocket, and
gRPC — no tracking, no cloud sync, just local execution. This repository is
the project's public front door: the introduction site and its downloadable
release, not the application source itself.

- 🔗 **Site:** [donghquinn.github.io/hostman](https://donghquinn.github.io/hostman/)


---

## What's in this repository

| File | Purpose |
|---|---|
| `index.html` / `index.ko.html` | The one-page introduction site, English and Korean. Deployed to GitHub Pages on every push to `main` (see `.github/workflows/release.yml`). |
| `hostman-logo.png` | The brand mark used in the site's header. |
| `hostman-1.0.0.dmg` | The current macOS release — linked from the site's Install section. |

The Electron shell, the Go backend, the frontend, and all the actual
development docs live in [hostman-desktop](https://github.com/donghquinn/hostman-desktop)
instead.

## Download

| Platform | |
|---|---|
| **macOS** | Universal binary (Apple Silicon + Intel), unsigned — [`hostman-1.0.0.dmg`](hostman-1.0.0.dmg), ~198 MB. macOS will warn on first launch since it isn't notarised; that's a paid Apple program, not a statement about the app. |
| **Windows / Linux** | Built from hostman-desktop's release pipeline — see that repo's [Releases](https://github.com/donghquinn/hostman-desktop/releases). |

A Homebrew tap (`brew install --cask hostman`) is planned but not published
yet — use the direct download above for now.

## What hostman does

Three protocols, one window:

| | |
|---|---|
| **HTTP & REST** | GET, POST, PUT, DELETE, and GraphQL, with JSON, form-data, and binary uploads. |
| **WebSocket** | Persistent connections for streaming messages, live feeds, and event sockets. |
| **gRPC** | Native `.proto` or server-reflection support, no code generation. |

No account, no telemetry, no paid tier. Collections save as plain, readable
JSON under `~/.hostman/collections/` — diff them, put them in Git, send one
as a file.

## What it deliberately leaves out

No test scripting, no collection runner, no mock servers or monitors, no
cloud team workspaces, no automated OAuth2 flow, no persistent cookie jar, no
automatic request chaining, no code generator. If your workflow needs any of
those, Postman or Bruno will serve you better — hostman stays narrow on
purpose.

## Developing the site

The site is plain HTML/CSS, no build step. Edit `index.html` /
`index.ko.html` directly and push to `main`; the Pages workflow picks it up
automatically.

## License

MIT © 2026 Dong H. Kim — see [hostman-desktop's LICENSE](https://github.com/donghquinn/hostman-desktop/blob/main/LICENSE).
