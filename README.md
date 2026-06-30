# CyberDeck

A fully custom, hand-built cyberdeck — a portable computer combining a single-board
computer, a custom 3D-printed enclosure, and integrated security/RF tooling — built
from scratch as a learning project covering Linux systems administration, CAD &
3D printing, electronics, and embedded firmware.

This repo is both the build log and the source of truth for the project: design
files, scripts, documentation, and notes, organised so the whole build is
reproducible and so it's legible to someone looking at it cold (recruiters
included).

> **Status:** 🚧 In progress — currently working through Module 1 (Linux &
> Command Line Foundations) of the build curriculum. See [`/docs/roadmap.md`](docs/roadmap.md).

---

## What is this?

Cyberdecks are DIY, fully custom portable computers — a term originating from
the cyberpunk novel *Neuromancer* — typically built around a single-board
computer (Raspberry Pi, Orange Pi, etc.) housed in a self-designed enclosure.
This build's goals:

- A **headless-capable, SSH-first Linux system** as the daily-driver compute base
- A **fully custom 3D-printed enclosure**, designed in CAD rather than reusing an
  off-the-shelf case
- Integrated **RF / security-research tooling** (e.g. ESP32-based wireless tools),
  built and used strictly for legal, ethical, and educational purposes —
  see [Ethical Use](#ethical-use--legal-notice) below
- A clean, documented build process other people could actually follow or learn from

## Repo structure

```
cyberdeck/
├── docs/                 # roadmap, learning modules, build logs, research notes
├── hardware/
│   ├── cad/              # FreeCAD / Fusion source files for the enclosure
│   ├── pcb/              # KiCad project files (schematics, PCB layout)
│   └── exports/          # generated STL / STEP / Gerber files for printing/fab
├── firmware/              # ESP32 / microcontroller firmware source
├── software/              # scripts, dashboard, automation, systemd services
├── bom.md                 # bill of materials, with costs and links
├── LICENSE
├── .gitignore
└── README.md
```

(Folders get created as each module of the build actually produces files —
no point scaffolding empty directories ahead of need.)

## Hardware overview

| Component | Choice | Status |
|---|---|---|
| Compute | Raspberry Pi (model TBD) | learning phase |
| Display | TBD | not started |
| Enclosure | Custom 3D-printed (FreeCAD) | not started |
| Power | TBD | not started |
| RF / security tooling | ESP32-based, TBD | not started |

Full bill of materials with sourcing and cost will live in `bom.md` once
hardware decisions are locked in.

## Build log / learning curriculum

This project is being built alongside a structured learning curriculum rather
than assembled in one go. Progress and module write-ups live in `/docs`:

1. Linux & Command Line Foundations
2. 3D Design & the Physical Build
3. Electronics & Power
4. RF, Wireless & Security Tooling
5. Integration & Software

## Ethical use & legal notice

This project includes wireless and security-research tooling (e.g. RF, NFC,
BadUSB-style capability). All such tooling here is built, tested, and used
**only** against hardware/networks I own or have explicit authorisation to
test. Nothing in this repo is intended to facilitate unauthorised access to
systems or networks. If you use anything from this repo, that responsibility
is yours — use it legally and ethically.

## License

See [`LICENSE`](LICENSE). Short version: MIT — do what you like with this,
just keep the attribution and don't hold me liable. See the license rationale
note in that file's accompanying section below if you're deciding what to
pick for your own repo.

## Author

Built by K — first-year Bachelor of Information Technology student,
Otago Polytechnic, Dunedin NZ.
