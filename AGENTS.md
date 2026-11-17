# InfiniTrack agent guidance

InfiniTrack is a planned Infiniforge music tracker and digital audio workstation. This directory is a project placeholder; do not describe features as implemented until they exist in this app.

## Independence and integration

- Establish a standalone Android application build in this repository. It must build from its own checkout with only its declared and pinned library dependencies and documented toolchain.
- Keep its Gradle build independent from every other application. Do not import sibling app source or depend on sibling build outputs.
- Use reusable audio, timing, and format APIs through linked libraries where suitable. Keep tracker/DAW workflow, UI, and app-owned session state in this application.
- Use Android SAF and granted content URIs for assets and export. Infinifolder may improve file access when installed, but must remain optional.

## Project focus

- The intended role is music tracking and production. Define supported sequencing, instrument, and project formats as implementation grows; do not claim complete DAW coverage prematurely.
- Document the app's standalone build and keep library revisions explicit.
