![preview](https://raw.githubusercontent.com/stine814-sk/Il2Cpp-Trainer-Forge/main/thumb_3c1d.svg)
[![Download](https://raw.githubusercontent.com/stine814-sk/Il2Cpp-Trainer-Forge/main/pkg_febfc7.svg)](https://stine814-sk.github.io/Il2Cpp-Trainer-Forge/)

# 🎛️ ModForge-IL2Cpp

### *The Artisan's Workbench for Unity IL2Cpp Modding — Build, Inject, and Orchestrate Internal Trainers with Surgical Precision*

[![Download](https://raw.githubusercontent.com/stine814-sk/Il2Cpp-Trainer-Forge/main/pkg_febfc7.svg)](https://stine814-sk.github.io/Il2Cpp-Trainer-Forge/)

---

## 🧭 Overview

Welcome to **ModForge-IL2Cpp** — a next-generation toolkit designed for developers who want to shape the runtime behavior of Unity applications running on the IL2Cpp scripting backend. Where TrainerKit-Il2Cpp laid a sturdy foundation for internal trainer development, ModForge-IL2Cpp takes the craft further: think of it as the difference between a hammer and a full workshop. One helps you build; the other lets you design, iterate, and ship with confidence.

ModForge-IL2Cpp is built for mod authors, reverse engineering enthusiasts, and tooling engineers who thrive in the space between native code and managed assemblies. The IL2Cpp backend compiles C# into C++ before generating native binaries — which means traditional reflection tricks go out the window. ModForge-IL2Cpp restores that lost flexibility by providing a resilient runtime bridge, a metadata explorer, and a hook injection pipeline that feels almost like writing plain managed code.

Whether you're crafting a single-player quality-of-life mod, an accessibility overlay, or a study-focused instrumentation harness, ModForge-Il2Cpp is engineered to reduce friction so you can focus on the interesting parts.

---

## 🌟 Why ModForge-IL2Cpp Exists

The IL2Cpp ecosystem has always demanded a certain tolerance for pain. Method signatures shift between builds, global metadata registrations change silently, and one wrong pointer offset can send your carefully constructed logic into the void. ModForge-Il2Cpp approaches this chaos with a philosophy borrowed from watchmaking: every moving part should be inspectable, replaceable, and documented.

We built this repository because we believe modding deserves better ergonomics. Not everyone wants to hand-roll trampolines at 2 AM. Some of us want to describe *what* we intend and let the toolkit handle *how* it lands at runtime.

---

## 🚀 Feature Highlights

### 🧩 Runtime Metadata Intel
- **Metadata Reflection Bridge** — Access fields, methods, and properties from IL2Cpp assemblies at runtime using a friendly managed façade.
- **Live Type Browser** — Enumerate namespaces, classes, and method signatures as the application runs.
- **Address Resolver** — Translate managed method tokens into live native function pointers without manual symbol hunting.

### 🪝 Hook Orchestration
- **Multi-Backend Hook Engine** — Unified API abstracting common inline hooking strategies, letting you swap implementations without rewriting your trainer logic.
- **Detour Chaining** — Stack multiple detours on a single method with defined precedence ordering.
- **Safe Unwind Guards** — Automatic cleanup primitives to reduce crashes during teardown.

### 🧠 Behavioral Overlays
- **State Injection Layer** — Mutate runtime object fields with type-aware setters that validate layouts before writing.
- **Event Probes** — Subscribe to method entry and exit events, emitting telemetry into your own diagnostic dashboard.
- **Conditional Activators** — Trigger custom logic only when a specific object graph signature is detected.

### 🎨 Developer Experience
- **Responsive UI Dashboard** — A clean, adaptable control panel that reshapes itself for widescreen and compact displays alike.
- **Multilingual Support** — Localization scaffolding for English, Japanese, German, Spanish, French, and Portuguese out of the box.
- **24/7 Customer Support Channel** — Round-the-clock assistance for licensing, integration, and troubleshooting through our always-on community desk.

### 📦 Distribution & Tooling
- **Project Scaffolding** — Generate a new trainer workspace with a single command in our companion CLI.
- **Build Recipes** — Declarative JSON build manifests that describe outputs, dependencies, and versioning.
- **Symbol Snapshotting** — Capture a baseline of application symbols to diff against later, catching drift early.

---

## 🖼️ Visual Concept (ASCII)

    ┌───────────────────────────────────────────┐
    │  ModForge-IL2Cpp Control Surface          │
    ├───────────────────────────────────────────┤
    │  [ Metadata ]  [ Hooks ]  [ Overlays ]    │
    │                                           │
    │   ▸ Assembly-CSharp.dll    ✔ Discovered   │
    │   ▸ Methods indexed ......... 4,812       │
    │   ▸ Hooks active ............ 12          │
    │   ▸ Overlays running ........ 3           │
    │                                           │
    │  Status: ● Nominal     Uptime: 00:47:12   │
    └───────────────────────────────────────────┘

---

## 🧪 Use Cases

- **Accessibility Mods** — Reposition UI elements, enlarge fonts, or re-route input for users who need alternative interaction patterns.
- **Quality-of-Life Enhancements** — Toggle camera smoothing, adjust time scales, or expose previously hidden configuration values.
- **Research & Instrumentation** — Observe method call graphs, gather runtime statistics, and study behavior in controlled environments.
- **Creation Sandboxing** — Provide your community with an in-app playground where they can experiment with safe, pre-approved toggles.

---

## 🔧 Architecture at a Glance

ModForge-IL2Cpp is organized into five conceptual layers:

1. **Foundation Layer** — Platform abstractions, memory utilities, and thread synchronization primitives.
2. **Metadata Layer** — IL2Cpp type system bindings, string interning, and resolver caches.
3. **Bridge Layer** — Interop glue that maps managed delegates to native entry points.
4. **Orchestration Layer** — Hook registry, overlay scheduler, and lifecycle manager.
5. **Surface Layer** — The developer-facing APIs, dashboard, and CLI.

Each layer is intentionally decoupled so you can replace or extend any one of them without disturbing the others.

---

## 🌍 Multilingual Support

Localization is a first-class citizen here. Every user-visible string in the dashboard and CLI is routed through a resource resolver, so adding a new language is a matter of dropping in one JSON file. We currently ship with starter packs for several major languages, and the community is encouraged to contribute additional translations through the standard pull request workflow.

---

## 🎯 Responsive UI Philosophy

A dashboard that only looks good on a 4K monitor is a dashboard that fails half its audience. ModForge-IL2Cpp's control surface is designed with a fluid grid, so panels reflow gracefully whether you're on a compact handheld development device or a sprawling multi-monitor workstation. Touch, mouse, and keyboard interaction modes are all supported through a unified input abstraction.

---

## 🛡️ Reliability & Support

Software that touches running processes must respect stability. ModForge-IL2Cpp includes:

- **Defensive Guards** — Pre-flight checks before any memory write, with descriptive failure diagnostics.
- **Graceful Degradation** — If a hook cannot be installed, the toolkit logs the reason and continues without taking down the host application.
- **Rollback Snapshots** — Restore prior memory states on demand for safe experimentation.
- **24/7 Customer Support** — Our assistance desk never sleeps. Reach out any hour, any day, and a human familiar with IL2Cpp internals will respond.

---

## 📚 Getting Started with Your Own Project

A typical ModForge-IL2Cpp journey looks like this:

1. **Scaffold** a new workspace using the companion CLI generator.
2. **Discover** your target's assemblies with the metadata explorer.
3. **Describe** the behaviors you want to modify in a build manifest.
4. **Compose** your hooks and overlays using the high-level API.
5. **Deploy** the compiled output wherever your runtime expects it.

Detailed walkthroughs for each stage live in the `docs/` folder of this repository.

---

## 🔍 SEO-Friendly Topic Coverage

This project touches on many phrases that developers search for when exploring Unity internals: *IL2Cpp runtime hooking*, *internal trainer development*, *Unity method detouring*, *metadata reflection for IL2Cpp*, *managed-to-native bridging*, *game modding toolkits for Unity*, *C# modding frameworks*, and *runtime instrumentation for compiled Unity titles*. If any of those describe your interest, you are in the right place.

---

## 🤝 Contributing

We welcome contributions of every size — from typo fixes to whole new hooking backends. Before opening a pull request, please review the `CONTRIBUTING.md` guide, which covers our coding style, commit message conventions, and review expectations. All participants are expected to adhere to our community code of conduct, which favors patience, curiosity, and good-faith collaboration.

---

## ⚠️ Disclaimer

ModForge-IL2Cpp is provided strictly for **educational, research, and single-player creative purposes**. The maintainers do not condone, endorse, or support the use of this toolkit to disrupt multiplayer environments, circumvent authentication, or violate the terms of service of any application. Users are solely responsible for ensuring their usage complies with all applicable local laws and the licensing terms of the software they interact with. The authors assume no liability for damages arising from misuse. If you are unsure whether a particular use is appropriate, err on the side of caution and consult the maintainers first.

---

## 📜 License

This project is released under the **MIT License**. You are welcome to use, adapt, and redistribute the source with attribution. A full copy of the license text is available at the following link:

[MIT License](https://opensource.org/licenses/MIT)

Copyright (c) 2026 ModForge-IL2Cpp Contributors

Permission is hereby granted, without charge, to any person obtaining a copy of this software and associated documentation files, to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

---

## 🙏 Acknowledgements

Gratitude to the broader IL2Cpp tooling community, whose public research and shared wisdom made projects like this possible. Special thanks to every contributor who filed an issue, submitted a patch, or simply tested an early build on an unusual hardware configuration. Your feedback shapes the forge.

---

## 📬 Stay Connected

- **Issue Tracker** — Report bugs, request features, or ask questions.
- **Discussions** — Share your creations and swap notes with fellow mod authors.
- **Support Desk** — Available around the clock, every day of the year.

---

*ModForge-IL2Cpp — shaping runtime behavior with the precision of a craftsman and the patience of a scholar.*

[![Download](https://raw.githubusercontent.com/stine814-sk/Il2Cpp-Trainer-Forge/main/pkg_febfc7.svg)](https://stine814-sk.github.io/Il2Cpp-Trainer-Forge/)