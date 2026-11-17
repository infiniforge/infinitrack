# InfiniTrack
InfiniTrack is a planned music tracker and digital audio workstation combining pattern-based and
timeline workflows. This repository is currently a placeholder; see the [application scope and
implementation status](docs/APPLICATION.md).

**Status: planned placeholder.** This checkout currently contains project guidance
only. It has no Android application source, Gradle build, app-level `build.sh`, or
APK, so it cannot be built or installed yet.

The planned app is a music tracker and digital audio workstation. It should own
its sequencing UI, session data, and export workflow in an independent Android
project. Android SAF is the baseline for assets and exports. Planned file access
should use `libinfiniselect`, with Infinifolder's provider optional. Reusable
audio processing may use `libinfinisound` through its public API.

No sequencing engine, project format, or DAW workflow is implemented in this
placeholder.
