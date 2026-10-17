# Learn Tip · planned `block_coursectrllearntip`

[![Moodle Plugin CI](https://github.com/ralferlebach/moodle-block_coursectrllearntip/actions/workflows/moodle-ci.yml/badge.svg?branch=main)](https://github.com/ralferlebach/moodle-block_coursectrllearntip/actions/workflows/moodle-ci.yml?query=branch%3Amain) [![Status: scaffolding](https://img.shields.io/badge/Status-scaffolding-orange)](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/1)

[![CourseCtrl Hub](https://img.shields.io/badge/Plugin%20family-CourseCtrl%20Hub-3867d6)](https://github.com/ralferlebach/moodle-local_coursectrl) [![CourseCtrl Dates](https://img.shields.io/badge/Companion-CourseCtrl%20Dates-16a085)](https://github.com/ralferlebach/moodle-block_coursectrldates) [![Learn Tip](https://img.shields.io/badge/Companion-Learn%20Tip-8e44ad)](https://github.com/ralferlebach/moodle-block_coursectrllearntip)

**Development notice:** Learn Tip is a planned, small learner-facing Moodle course block. This repository currently contains a **copied `block_coursectrl` scaffold**: its `version.php`, namespaces and capabilities have **not yet been renamed to `block_coursectrllearntip`**. Do **not** treat this checkout as a safely installable Learn Tip block. Correct scaffolding is tracked in [#1](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/1).

## Requirements

- **Planned:** Moodle 4.5–5.3, subject to installation and compatibility tests; the current scaffold's `version.php` is **not authoritative** for the future Learn Tip component.
- **Planned dependency:** [`local_coursectrl`](https://github.com/ralferlebach/moodle-local_coursectrl) with the shared learner-state and evidence graph APIs ([Local #61](https://github.com/ralferlebach/moodle-local_coursectrl/issues/61), [#70](https://github.com/ralferlebach/moodle-local_coursectrl/issues/70)).
- **Target install path:** `blocks/coursectrllearntip` **only after** #1 has corrected the Frankenstyle component and plugin registration.

## Motivation

Students benefit from a manageable, explainable next learning action, a transparent map of reachable activities, and opt-in motivational cues rather than a long undifferentiated to-do list.

## Installation

**Not ready for installation as Learn Tip yet.** Complete [initialisation #1](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/1), fix the `block_coursectrl` copied identifiers, set dependency/compatibility metadata and pass Moodle CI. Then follow [standard Moodle plugin installation](https://docs.moodle.org/en/Installing_plugins).

## Usage & settings — planned features

- A single explainable **next learning step**, plus alternative and reason ([#2](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/2)).
- Compact activity matrix: **outline = configured completion**, **fill = configured grade**; green/grey for access, red for recoverable unsuccessful results, high-contrast checks and warnings, visible to authorised learners only ([#8](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/8)).
- Student preferences for weekends, institutionally free days and achievable study windows ([#9](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/9)).
- Optional Moodle/iCalendar/Google reminders with explicit consent; external assistants only through verified integrations ([#10](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/10)).
- Optional **per-activity expected/actually awarded XP** from Level Up XP; do not invent XP values or double-award points ([#4](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/4)).
- Optional badges, competencies and adaptive-learning signals ([#5](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/5)).

These are **issue-backed plans**, not completed functionality.

## Capabilities

Learners must see only their own accessible activities, grades and completion. The future `block/coursectrllearntip:*` capability set remains subject to [#1](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/1). Current `block/coursectrl:*` declarations belong to the obsolete copied scaffold.

## Scheduled tasks

Future reminder tasks, if implemented, require explicit opt-in, user-scoped data access, deduplication and quiet hours. No Learn Tip reminder task is currently provided.

## How this plugin works / pitfalls

Presentation in `block_coursectrllearntip` is deliberately small. A single, read-only, privacy-safe state/evidence service in `local_coursectrl` will answer access, future availability, completion/grade, unlocking impact and recoverability. Learn Tip ranks/visualises this state; **deep analysis uses the same rules but tests hypothetical course profiles**, not real students' private records. See [shared graph #70](https://github.com/ralferlebach/moodle-local_coursectrl/issues/70) and [deep-analysis simplification #71](https://github.com/ralferlebach/moodle-local_coursectrl/issues/71).

No external project homepage has been set up; GitHub is the only canonical project location.

## Theme support

Planned Boost/Classic support, keyboard and screenreader navigation, and colour-independent legends; not yet verified on this scaffold.

## Plugin repositories / related projects

- **Source:** https://github.com/ralferlebach/moodle-block_coursectrllearntip
- **Shared services:** https://github.com/ralferlebach/moodle-local_coursectrl
- **Course dates:** https://github.com/ralferlebach/moodle-block_coursectrldates
- **Template:** https://github.com/ralferlebach/moodle-plugintemplate

## Bug reports, support & feature proposals

Use [GitHub Issues](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues) and [Pull requests](https://github.com/ralferlebach/moodle-block_coursectrllearntip/pulls). Consult existing implementation issues before opening duplicates.

## Moodle release support

Moodle 4.5–5.3 is a **target**, not verified release support. Quality gates: [#6](https://github.com/ralferlebach/moodle-block_coursectrllearntip/issues/6).

## Translating this plugin

English/German localisation is planned; other languages via [AMOS](https://lang.moodle.org/).

## Right-to-left support

RTL not yet tested.

## Maintainer, copyright & licence

Maintainer: **Ralf Erlebach**. Copyright © 2026 contributors as credited in source files. Planned **GNU GPL v3 or later**, following the source scaffold.
