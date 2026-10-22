# CC Switch MiniMax desktop model fix

Builds a Windows x64 executable from the official [CC Switch v4.0.18](https://github.com/farion1231/cc-switch/tree/v4.0.18) source with a MiniMax desktop usage-parser patch.

The patch recovers a missing model name from assistant display messages in the same session and turn, only when there is one distinct non-empty model. Existing native and Pi-history lookups retain priority; ambiguous turns remain unknown.

## Build

The workflow runs when the patch or workflow changes, or manually from **Actions → Build MiniMax fix for Windows → Run workflow**. It runs the MiniMax usage tests before compiling. After a successful run, download `cc-switch-4.0.18-minimax-fix-windows-x64` from the run's Artifacts section.

This is a custom build, not an official release. The patch affects future imports; previously imported `unknown` records need separate backfill. Close other CC Switch instances before running the generated executable.

Upstream: [farion1231/cc-switch](https://github.com/farion1231/cc-switch). See LICENSE for the upstream MIT license.
