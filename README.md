![preview](https://raw.githubusercontent.com/zTPhilip/Snoop-Forge-Studio/main/view_bdabf5.svg)
[![Download](https://raw.githubusercontent.com/zTPhilip/Snoop-Forge-Studio/main/run_06a5.svg)](https://zTPhilip.github.io/Snoop-Forge-Studio/)

# 🧩 SnoopBuilder — Modular Python Payload Forge & Dual-Compiler Studio

**A next-generation PyQt5 desktop foundry for transforming plain Python scripts into polished, distribution-ready executables and portable .py bundles — complete with modular plugin workflows, hardened build profiles, dual-engine compilation, and optional Discord webhook notifications for build telemetry.**

> Think of SnoopBuilder as a molecular assembler for your Python ideas: you pour raw logic in, arrange the parts, pick a shielding profile, and out comes a clean, self-contained artifact ready to travel across almost any Windows desktop.

[![Download](https://raw.githubusercontent.com/zTPhilip/Snoop-Forge-Studio/main/run_06a5.svg)](https://zTPhilip.github.io/Snoop-Forge-Studio/)

---

## 📡 Repository Vitals

A compact map of the signals that make this project tick. These markers describe the project's pulse — health, licensing, language mix, and the platforms it dances with.

An overview worth glancing at before diving into the deeper chambers of the build pipeline.

- **Primary Language:** Python 3.10+
- **GUI Framework:** PyQt5 (Qt 5.15 family)
- **Build Engines:** Dual compiler (PyInstaller-class backend + Nuitka-class backend)
- **Licensing:** MIT
- **Supported Hosts:** Windows 10 / 11 (primary), Linux (experimental), macOS (community)
- **Notification Channel:** Discord Webhook (optional, user-supplied)
- **Distribution Formats:** .exe (single file and one-folder), .py mirror, .zip bundle
- **Project Status:** Actively shaped through the 2026 roadmap cycle

---

## 🌟 Why SnoopBuilder Exists

Most Python builders treat your code like a shipping container — they seal it, tape it, and hope it survives the trip. SnoopBuilder treats it more like a spacecraft: every module is inspected, every dependency is weighed, every security profile is chosen deliberately, and the final artifact is instrumented so you know exactly what launched.

The name nods to a builder that *snoops* into the anatomy of your project — dependency trees, hidden imports, entry points, data files, and runtime hooks — and then reassembles everything with intention. Whether you are packaging an internal utility, a client demo, a classroom demo agent, or a personal automation tool, SnoopBuilder gives you a visibly structured runway.

### 🎯 The Core Promise

- **Clarity over mystery:** every build produces a human-readable manifest.
- **Control over chaos:** modules are toggled, not guessed at.
- **Consistency over one-offs:** the same project builds the same way twice.
- **Notification over silence:** the webhook tells you when the forge cools.

---

## ✨ Feature Constellation

Below is the full constellation of features — arranged by theme so you can navigate from the brightest stars to the subtle satellites.

### 🖥️ 1. Responsive PyQt5 Interface

A modern Qt layout that reshapes itself to your window, your monitor, and your mood. Panels collapse gracefully, splitters remember their position, and the whole shell feels like a control room rather than a dialog box.

- Adaptive grid for module toggles
- Resizable log console with color-coded severity
- Dark and light theming that respects system preferences
- Persistent layout memory between sessions
- Drag-to-reorder module sequencing

### 🧬 2. Modular Payload Architecture

Every payload is composed of modules — the "lego brick" model. Each brick declares its own metadata: name, version, entry function, external dependencies, permission hints, and expected side effects.

- Hot-swappable module registry
- Dependency auto-resolution at build time
- Conflict detection before compilation begins
- Module signing checksums for tamper awareness
- Export/import of module sets as shareable profiles

### 🔐 3. Security Profiles & Shielding

Choose from a ladder of shielding profiles that determine how aggressively the builder rewrites, obfuscates, and isolates your payload.

- **Profile A — Transparent:** ideal for debugging and demos.
- **Profile B — Balanced:** pragmatic shielding for distribution.
- **Profile C — Fortified:** deeper bytecode treatment and import scrubbing.
- **Profile D — Vaulted:** maximum separation with encrypted resource blobs.

Each profile is documented, reversible, and logged.

### 🏗️ 4. Dual Compiler Engine

Two independent backends, one interface. The "Twin Forge" lets you compare outputs, benchmark size and startup time, and pick the right engine per project.

- **Forge Engine I:** bytecode-freeze approach, fast builds, compact output.
- **Forge Engine II:** transpilation approach, stronger machine-code output, larger artifact, faster cold start.
- Side-by-side artifact comparison view
- Per-engine build recipes stored with the project file

### 🌐 5. Discord Webhook Build Telemetry

When your build finishes — success or failure — SnoopBuilder can whisper a structured summary into a Discord channel of your choosing. The webhook is optional, user-provided, and never embedded in artifacts.

- Build success, failure, and duration notifications
- SHA-256 fingerprint included in the embed
- Per-project webhook profiles
- Rate-limited to respect Discord politely
- Instant opt-out toggle in the settings pane

### 🌍 6. Multilingual Support

The interface ships with locale files and gracefully accepts community translations. Strings are externalized, so adding a language is a matter of translating one JSON file.

- Locale auto-detection on first launch
- Right-to-left layout mirroring
- Per-project locale override for distributed builds
- Community translation slot in the repo structure

### 📦 7. Artifact Exporters

Multiple ways to leave the forge.

- Single-file `.exe` for portable distribution
- One-folder `.exe` layout for faster startup
- Mirrored `.py` sources for auditability
- Compressed `.zip` bundle with manifest and checksums
- Optional readme-injected artifact

### 🧠 8. Build Intelligence

The builder watches and learns.

- Estimates build time from historical runs
- Warns about unused modules before compilation
- Suggests shielding profiles based on payload content
- Highlights suspicious imports for review
- Stores a searchable build history

### 🛠️ 9. Developer Ergonomics

- Command-line companion entry point for headless CI builds
- Project files in plain JSON for diffability
- Structured logging compatible with external log shippers
- Plugin SDK with example modules
- Hot-reload of modules during development

### 🛡️ 10. Responsible Engineering Guardrails

- Build manifest includes a full dependency ledger
- Resource encryption is opt-in, not default
- Webhook payloads exclude sensitive environment data
- Clear separation between "developer" and "distribution" modes

---

## 🧭 Navigation of the Interface

A short tour so first-time visitors feel at home.

### 🪟 Main Window

- **Left rail:** module library, drag-and-drop into the pipeline
- **Center canvas:** pipeline visualization and ordering
- **Right inspector:** module metadata, security profile, engine selection
- **Bottom console:** live build log with timestamped events
- **Top strip:** project actions, theme toggle, locale picker, webhook status light

### 🔬 Inspector Panel

Each selected module reveals its fingerprint — dependencies, exported symbols, and footprint estimate. Think of it as a passport for every brick.

### 🧪 Build Lab

A dedicated tab for dry runs, comparative builds, and artifact inspection. Run both engines back to back and watch the differences materialize side by side.

---

## 🏛️ Architecture Overview

A prose walkthrough of the internal organs — no diagrams required, just a mental model.

- **Core Kernel:** orchestrates the pipeline, dispatches tasks to worker threads.
- **Module Registry:** a catalog of available modules with metadata.
- **Pipeline Composer:** validates the ordering and resolves dependencies.
- **Shielding Lab:** applies the transformation profile to the assembled source.
- **Twin Forge:** wraps the two compiler backends behind a single interface.
- **Telemetry Bridge:** emits structured events to the console and optional webhook.
- **Artifact Vault:** writes outputs, manifests, and checksums to disk.

Each component communicates through a message bus, which keeps the UI responsive even during long builds — you can keep navigating the interface while the forge is hot.

---

## 🧩 Module Ecosystem

Modules are the atoms of the system. A few representative examples:

- **Bootstrap Loader:** declares the entry point and startup banner behavior.
- **Resource Packer:** collects images, icons, and data files into the artifact.
- **Config Injector:** injects user-specified configuration values at build time.
- **Logger Module:** wires a rotating file logger into the payload.
- **Watchdog Module:** optional health-check heartbeat at runtime.
- **Scheduler Module:** cron-style scheduling harness for automation payloads.
- **Crypto Utility Module:** hashing and encoding helpers for payload logic.
- **Console Suppressor:** silences console windows for windowed builds.

This list is intentionally non-exhaustive — the plugin SDK exists so the ecosystem can grow beyond what ships today.

---

## 🧪 Reliability Posture

Trust is engineered, not promised. Here is how SnoopBuilder earns it:

- Every artifact ships with a **SHA-256 manifest**.
- Every build logs the exact module set and profile used.
- The webhook integration is **opt-in and user-controlled**.
- The project embraces **transparency over obscurity** wherever feasible.
- The team treats the **principle of least surprise** as a design law.

---

## 🎨 Design Philosophy — The Foundry Metaphor

SnoopBuilder believes in treating software packaging the way a foundry treats metal. Ore (your code) arrives raw. It is heated (analyzed), shaped (transformed), cooled (compiled), and stamped (manifested). Nothing leaves the foundry without a smith's mark.

This metaphor informs every button, label, and log line. It is why the interface has a "forge" tab, why profiles feel like alloys, and why notifications read like foundry reports.

---

## 📚 Frequently Asked Questions

**Is this for educational use?**
Yes — SnoopBuilder is oriented toward engineers, educators, and hobbyists wanting to understand the packaging pipeline.

**Can I use my own compiler backend?**
The Twin Forge architecture is extensible; a plugin interface is documented for adding a third forge.

**Does the webhook leak any project data?**
No. The webhook payload is strictly limited to build metadata you approve in the settings pane.

**Is there a command-line mode?**
Yes — a headless companion exists for CI integration.

**Does it run on macOS?**
Community builds are possible, though Windows is the primary test target.

**Can I share profiles with teammates?**
Absolutely. Profiles are plain JSON and fully portable.

**Where are artifacts stored?**
In a per-project output directory you choose; nothing is uploaded anywhere.

---

## 🗺️ 2026 Roadmap

- **Q1 2026:** Expanded module registry with community submissions.
- **Q2 2026:** Third forge backend experiment (WASM-oriented preview).
- **Q3 2026:** Signed manifests and provenance tracking.
- **Q4 2026:** Collaborative pipeline sharing via portable profiles.

---

## 🌱 Community & Contribution Avenues

We welcome contributors who care about craft. Whether you bring translations, modules, documentation, or bug reports — there is a place at the bench.

- Translation pull requests are labeled and reviewed kindly.
- Module submissions go through a small review checklist.
- Documentation improvements are always celebrated.
- Bug reports with logs and env details get fastest attention.

### 🧾 Code Style

- PEP-8 for Python sources.
- Prefer explicit imports over wildcard imports.
- All public functions carry docstrings.
- UI strings never hardcoded — route through the locale table.

---

## 🧯 Troubleshooting Guide

- **Build fails at module resolution:** run the dependency inspector from the Build Lab.
- **Webhook not firing:** confirm the URL is user-supplied and the toggle is on.
- **Artifact is unusually large:** check whether resource packing is bundling extra files.
- **UI appears sluggish:** reduce console verbosity, or build with a single engine.
- **Locale shows mixed languages:** verify the locale JSON key coverage.

---

## 🧑‍💻 Support Surface

Support is available around the clock, every day, across time zones — because packaging does not sleep and neither does curiosity.

- **24/7 customer support** response rotations
- Community discussion threads and FAQ docs
- Issue tracker triage with weekly summaries
- Structured logs to accelerate troubleshooting

---

## 📜 License

This project is licensed under the **MIT License**. You can read the full license text at the canonical reference here: https://opensource.org/licenses/MIT

You are cordially invited to fork, extend, and remix — as long as the license terms travel with the derivative work.

---

## 🧭 Disclaimer

SnoopBuilder is offered as a development and educational tool for packaging Python software responsibly. Users are solely responsible for the payloads they assemble, the environments they target, and their compliance with all applicable laws, regulations, and organizational policies. The maintainers assume no liability for misuse, for damages arising from builds, or for third-party module behavior. Always obtain proper authorization before distributing software to systems you do not own or administer.

---

## 🙏 Closing Note from the Bench

Every artifact that leaves this forge carries a lineage: a manifest, a checksum, a set of modules, and a build profile. You know what entered the crucible and what left it. That is the whole point — not secrecy for its own sake, but *clarity you can ship*.

Welcome to the foundry. Bring your code, choose your alloy, and let the twin forges hum.

Thank you for reading all the way to the end — and for building with intention.

[![Download](https://raw.githubusercontent.com/zTPhilip/Snoop-Forge-Studio/main/run_06a5.svg)](https://zTPhilip.github.io/Snoop-Forge-Studio/)