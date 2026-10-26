# Umi‑Time Specification

**Umi-Time gives us one shared number for the exact same instant globally, while presenting it in a way that is locally meaningful.** 

Rather than creating a new time scale, Umi-Time acts as a presentation layer for UTC, treating the day as a continuous 0ᵘ–360ᵘ cycle. This repository contains the canonical, self-contained standard that defines how this single universal rhythm can be combined with local coordinates—allowing any digital, textual, or visual interface to ground the shared global number under an observer's local sky without altering the underlying value.

This repository is intentionally minimal and includes only the canonical assets required to render the specification correctly.

---

## Contents

```text
├── spec.html                 # The canonical Umi‑Time specification (self-contained HTML)
├── LICENSE                   # Repository license text (MIT)
├── CITATION.cff              # Repository citation metadata
├── .zenodo.json              # Zenodo archival configuration
├── css/
│   └── spec.css              # Stylesheet tailored for the specification layout
├── js/
│   └── spec.js               # Spec-specific interactive behavior
└── vendor/
    └── mathjax-full/         # MathJax core, loaders, and CHTML fonts (vendored for offline use)
```

The specification uses **MathJax** for rendering mathematical expressions. MathJax is vendored locally within this repository to ensure the text layout renders correctly:
- when opened directly from a local filesystem disk
- when archived permanently by Zenodo
- when embedded as a submodule in the Umi‑Time website
- when viewed completely offline

No external build tools or package managers are required.

---

## Viewing the Specification

### **Standalone**
Open `spec.html` directly from your file manager into any modern web browser. All required CSS, JavaScript, and fonts are loaded locally from the repository paths.

*Note: If your browser's local security policy restricts loading font files directly from disk (`file://`), you can serve the directory using a lightweight local server (e.g., `python -m http.server` or `npx serve`).*

### **On the Website**
The official, rendered version of this standard is viewable online at the [Umi-Time Specification Page](https://umitime.com). 

The website embeds this repository via a Git submodule. It does not modify or duplicate the spec; it simply displays this same canonical HTML asset.

---

## Purpose of This Repository

This repository exists to:
- provide a **single authoritative source** for the Umi‑Time standard
- maintain a **stable, citable artifact** for DOI publication
- keep the specification **independent** from the website and implementations
- ensure the spec can be viewed and archived **without build tooling**
- support embedding in other contexts (e.g., documentation, research, teaching)

Only the specification standard lives here. Implementation libraries belong in their own repositories (e.g., `umi-time-js`).

---

## Versioning

Each tagged release represents a stable, citable version of the standard using Semantic Versioning (e.g., `v1.0.0`).

---

## Contributing

Because this repository maintains the canonical standard, direct changes to the core specification follow a strict review protocol. 
* To report errata, ambiguities, or formatting typos, please open an Issue.
* For architectural modifications or changes to the time mapping formulas, please start a discussion topic before drafting a Pull Request.

---

## Citation

If you reference this specification in an academic paper, technical report, or software implementation, please cite it as follows:

> Brannon, D. & Umi-Time Contributors. (2026). *Umi-Time Specification: A Universal Time Representation with Local Presentation Mapping* (Version 1.0.0). DOI: [Insert DOI Here](https://doi.org)

---

## License

MIT License © 2026 Daniel Brannon and Umi-Time Contributors
