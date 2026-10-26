# JT App Manager — Category Capability Standards

The catalogue should describe each JT app by its category and show implemented, in progress, and planned capabilities separately. Do not imply that an app has every feature of a category just because it appears in that category.

## Category standards for the JT ecosystem

| Category | JT product(s) | Capability targets |
|---|---|---|
| AI assistant / research | JT AI Agent, Jeff AI | Chat, project context, research workflows, documents, coding help, data analysis, specialist tools, model/provider selection and explicit tool permissions |
| Shared AI infrastructure | JT AI Core | Provider abstraction, local Ollama adapter, cloud-provider adapters when configured, structured tool calls, app-scoped permissions, audit events, timeouts and safe error handling |
| Desktop automation | JT Desktop Agent / Agent Jeff | Global launcher, app/file search, approved actions, browser/app automation, permission prompts, audit trail, task verification and emergency stop |
| Coding | JT Code | Editor, syntax highlighting, project/file tree, run/test tasks, diagnostics, Git workflows, isolated previews and AI coding assistance |
| Graphic design | JT Design | Canvas, layers, shapes, text, images, alignment, templates, SVG/PNG export, undo/redo and optional AI-assisted asset generation |
| Audio / music | JT Studio | Multitrack audio, recording, waveform editing, effects, mixing, export, MIDI/instrument workflows as feasible, project save/restore and optional AI assistance |
| Video / motion | JT Motion | Media library, multitrack timeline, trim/split, transitions, titles/captions, audio controls, preview and rendered export |
| File management / cloud | JT Cloud | File workspace, sync, versions, sharing, access control, offline queue, backup and restore; only call it cloud storage once a real backend exists |
| Streaming | JT Stream | Scene/source management, audio/video capture, transitions, overlays, recording, stream configuration, local recording and platform integrations with user-authorized credentials |
| App lifecycle | JT App Manager | Product catalogue, platform compatibility, build status, signed installer checks, version comparison, user-approved install/update, rollback and uninstall when implemented |

## Product integration rules
- Every app may request assistance from JT AI Core, but each app exposes only its own permitted tools.
- JT Desktop Agent alone may control the desktop or device, and only through explicit, revocable permissions.
- Prefer local processing when practical. Clearly disclose external providers and data sent to them.
- Do not invent CI status, platform support, release availability or installed-app state.
- Do not auto-install, delete user data, publish content or run arbitrary commands without clear user consent.
- Keep a feature-status field for each capability: implemented, in-progress, or planned; back implemented claims with tests or verifiable behavior.
- A category checklist is an acceptance standard, not evidence that the features already exist.