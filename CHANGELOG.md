# Changelog

All notable changes to PRO REELS EDITOR are documented in this file.

This project follows [Semantic Versioning](https://semver.org/).

The changelog records changes that affect the skill's behavior, capabilities, structure, or use. Internal drafting changes and minor wording adjustments are only listed when they materially affect how the skill is interpreted or used.

---

## [1.0.0] - 2026-10-03

Initial public release of PRO REELS EDITOR.

Version 1.0 establishes the core editorial framework used by the skill. The release is focused on making editing decisions based on content, context, and viewer comprehension rather than relying on a fixed collection of effects or presets.

### Added

#### Editorial decision system

* Added a defined decision hierarchy for short-form editing.
* Established content and factual integrity as the first priority.
* Added story and comprehension checks before retention and visual polish.
* Added explicit support for choosing no effect when an effect is not necessary.
* Added a decision model based on the needs of the current moment rather than a fixed effect library.

#### Source and content analysis

* Added source-media inspection and triage.
* Added content understanding requirements before detailed editing.
* Added support for transcription-aware editing.
* Added semantic segmentation of spoken and visual content.
* Added speaker and dialogue analysis.
* Added identification of hooks, explanations, examples, punchlines, demonstrations, and calls to action.

#### Hook and retention

* Added dedicated opening and hook analysis.
* Added rules for removing unnecessary setup and dead time.
* Added retention-aware pacing decisions.
* Added attention-density considerations.
* Added attention reset logic for sections that become visually or structurally repetitive.

#### Semantic editing

* Added meaning-driven cut decisions.
* Added context-aware treatment of individual moments.
* Added rules for matching visual treatment to the role of a scene.
* Added separation between structural editing and decorative editing.

#### Attention management

* Added a primary attention-target model.
* Added explicit handling for speaker, product, screen, text, reaction, demonstration, environment, and graphic targets.
* Added rules to reduce competing visual priorities.

#### Effect management

* Added effect budgeting.
* Added effect cooldowns.
* Added treatment-frequency tracking.
* Added anti-repetition rules.
* Added controlled variation between similar moments.
* Added explicit support for `NO EFFECT` as an editorial outcome.

#### Face and speaker editing

* Added speaker-aware framing decisions.
* Added face-aware punch-in and reframing rules.
* Added reaction-aware editing.
* Added guidance for maintaining natural framing and avoiding unnecessary zoom cycles.

#### B-roll

* Added semantic B-roll selection rules.
* Added relevance checks for supporting footage.
* Added source-integrity requirements for B-roll.
* Added rules preventing unrelated footage from being presented as evidence.

#### Product and screen editing

* Added product-focused editing behavior.
* Added screen-recording and interface presentation rules.
* Added guidance for scale, crop, readability, highlighting, and interaction visibility.
* Added rules for prioritizing the relevant information within dense screens.

#### Captions and typography

* Added a dedicated caption system.
* Added reading-speed considerations.
* Added caption timing and segmentation rules.
* Added emphasis hierarchy.
* Added typography and safe-area requirements.
* Added multilingual text considerations.
* Added RTL and mixed RTL/LTR handling.

#### Audio

* Added dialogue-first audio treatment.
* Added speech cleanup considerations.
* Added level consistency requirements.
* Added music and SFX balancing rules.
* Added silence and pause handling.
* Added sound-design placement based on editorial events rather than empty space.

#### Music

* Added music-selection criteria based on content, tone, pacing, and speech density.
* Added music-level considerations for dialogue-heavy material.
* Added licensing awareness.

#### Color

* Added a structured color-correction workflow.
* Added exposure and white-balance checks.
* Added shot-consistency considerations.
* Added skin-tone protection.
* Added guidance against unnecessary heavy grading.

#### Brand consistency

* Added support for recurring project-level visual conventions.
* Added consistency rules for typography, captions, motion, SFX, framing, colors, and CTA treatment.
* Added separation between brand consistency and repetitive editing.

#### Accessibility

* Added muted-viewing considerations.
* Added small-screen readability checks.
* Added caption accessibility requirements.
* Added guidance for reducing reliance on audio-only information.

#### Source integrity

* Added explicit restrictions against fabricating speech, reactions, events, evidence, or product behavior.
* Added safeguards against misleading B-roll.
* Added requirements to preserve the meaning of source material.

#### Licensing and sensitive information

* Added checks for third-party media and music licensing.
* Added awareness of watermarks and protected material.
* Added sensitive-information checks.
* Added protection considerations for credentials, contact information, private UI data, and other information that should not appear in the final output.

#### Capability awareness

* Added capability-aware execution rules.
* Added explicit handling for environments without transcription, tracking, rendering, frame extraction, audio processing, or external-media capabilities.
* Added a requirement to distinguish between an action that was performed and an action that could not be performed.

#### Editing workflow

* Added a multi-pass editing architecture:

  1. Ingest
  2. Understand
  3. Structure
  4. Rhythm
  5. Visual
  6. Audio
  7. Color
  8. Polish
  9. QA

* Added separation between editorial structure and finishing work.

* Added final human-editor simulation before delivery.

#### Quality assurance

* Added final checks for:

  * Story clarity
  * Factual integrity
  * Caption accuracy
  * Caption timing
  * Audio clarity
  * Music balance
  * Visual consistency
  * Effect repetition
  * Cropping
  * Tracking
  * Graphics
  * Safe areas
  * Sensitive information
  * Export integrity

#### Platform delivery

* Added delivery considerations for:

  * Instagram Reels
  * YouTube Shorts
  * TikTok

* Added separation between platform formatting and core editorial decisions.

---

### Changed

* Consolidated repeated editing rules into a single decision hierarchy.
* Consolidated repeated attention-target guidance.
* Consolidated effect-priority and anti-repetition behavior.
* Consolidated overlapping rules for face editing, B-roll, product footage, and screen content.
* Moved the system away from effect-first decision making.
* Reframed visual effects as optional editorial tools rather than default treatments.
* Made source integrity a requirement across the entire workflow instead of a final-stage check.
* Made capability limitations part of the decision process instead of treating unavailable tools as implicit assumptions.
* Organized the workflow into explicit editing passes to reduce conflicts between structural and finishing decisions.
* Added stronger separation between editorial judgment, visual polish, and technical delivery.

---

### Fixed

* Removed overlapping rules that could result in contradictory editing decisions.
* Reduced repeated instructions concerning attention, effects, and visual variation.
* Clarified when B-roll should and should not be used.
* Clarified when visual emphasis is justified.
* Clarified that a lack of available tooling must not be represented as completed work.
* Clarified the relationship between retention optimization and content comprehension.
* Clarified that consistency does not mean repeating the same effect.
* Clarified that visual polish must not alter the meaning of the source material.

---

### Documentation

* Added the first public project README.
* Added repository structure documentation.
* Added semantic versioning guidance.
* Added contribution guidance.
* Added project roadmap.
* Added release documentation.

---

## [Unreleased]

Changes for the next release will be added here.

Potential development areas include:

* Persistent editorial memory
* Reuse of previous editing decisions
* Historical treatment tracking
* Project-specific editorial profiles
* Cross-video style consistency
* Editorial outcome tracking
* More advanced decision confidence
* Additional platform-specific delivery rules
* Extended QA coverage

Nothing listed under this section should be considered part of the current stable release until it is included in a versioned release.

---

## Versioning

Release numbers follow [Semantic Versioning](https://semver.org/):

* **MAJOR** — changes that significantly alter the skill's core behavior or require users to adjust how it is used.
* **MINOR** — new capabilities or editorial systems that remain compatible with the existing workflow.
* **PATCH** — corrections, clarifications, and smaller non-breaking improvements.

Release tags use the following format:

```text
vMAJOR.MINOR.PATCH
```

Example:

```text
v1.0.0
v1.1.0
v1.1.1
v2.0.0
```

---

## Release links

[Unreleased]: ../../compare/v1.0.0...HEAD
[1.0.0]: ../../releases/tag/v1.0.0
