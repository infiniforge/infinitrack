# InfiniTrack application

## Purpose

InfiniTrack is the planned InfiniForge music tracker and digital audio workstation. It is intended to combine pattern-based tracker composition with piano-roll and timeline-based production. It is not intended to be only a tracker.

## Primary use cases

- Compose with tracker patterns, samples, instruments, note sequencing, and traditional tracker effects.
- Arrange patterns and audio on a multitrack timeline and edit notes through piano-roll and tracker views.
- Record, mix, automate, and export audio where the supported engine and platform allow.
- Import and export supported tracker, MIDI, instrument, and audio formats.
- Reuse instruments created in InfiniWave and export supported mixes for InfiniMedia.

## Current implementation status

This repository is a planned placeholder. It contains no Android application source, Gradle build, app build script, installable APK, project format, sequencer, or declared library dependency. All tracker and DAW functions above are intended direction rather than implemented behavior.

## Intended responsibilities and shared libraries

InfiniTrack should own composition sessions, sequencing, arrangement, tracker/piano-roll editing, DAW workflow, and app-owned project state. Reusable audio synthesis, decoding, timing, and PCM processing should come through libinfinisound; libinfinistream may provide resource/stream contracts, and libinfiniselect may provide Android selection and URI-grant handling. These are candidate libraries only; no dependency is declared here.

The app should not own remote storage backends or depend on InfiniFolder, InfiniWave, or InfiniMedia to build or launch. InfiniFolder may optionally provide resources through public Android/library contracts. Shared instruments and projects need documented data formats rather than access to another app's private files.

## Planned and exploratory functionality

A key design goal is displaying tracker patterns in a piano roll while retaining enough source structure for round-trip editing. The reverse mapping from unrestricted timeline events into traditional tracker patterns is not solved: event timing, pattern rows, channels, instrument constraints, and effects may not map one-to-one. Investigate a reindexing/translation strategy and define loss reporting before promising round-trip conversion.

Where practical, use an internal event representation that preserves pattern identity and timing alongside timeline edits. This is a design proposal, not an existing model. Additional planned areas include MIDI, multitrack arrangement, recording/editing, mixing, automation, and format import/export, subject to engine and platform capabilities.

## Interoperability

The [generated ecosystem map](ECOSYSTEM.md) provides the wider application/library map. InfiniWave may provide instruments/presets, and InfiniMedia may play supported exports. Their file or service contracts have not been defined. InfiniTrack must remain independently installable and should use explicit Android grants for imported or exported resources.

## Documentation audit

- Consistent: agent guidance already describes tracker and DAW responsibilities; this document clarifies that the product is not tracker-only.
- Incomplete: there is no app code, session model, timeline, or interoperability format.
- Unresolved: mapping free timeline events back into tracker patterns is explicitly an open design problem.

## Limitations and outstanding work

- No application code, sequencer, project/session format, audio engine, build, or release version exists in this placeholder.
- Tracker/piano-roll round-trip semantics and the proposed reindexing mechanism are unresolved.
- Recording, realtime mixing, automation, MIDI support, and format coverage are goals, not implemented features.
- Choose shared library APIs and interchange formats before adding app-local copies of sound engines or trackers.
- Document data-loss and conversion behavior before promising lossless editing across tracker and DAW representations.
