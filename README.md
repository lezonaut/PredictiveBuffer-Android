# Predictive Input Buffer — Android source port (experimental)

**Target:** Geode 5.11.2 / Geometry Dash Android 2.208.x, arm64 build intended.

## Changes in this revision
- Removed the Windows-only header and F6 polling.
- Removed Windows console initialization and replaced the remaining debug print with Geode logging.
- Uses an integer Geode setting (`buffer-preset`, 0–4), matching the Geode settings schema.
- Declares the Android game version as 2.208.1 in `mod.json`.

## Important limitations
- This ZIP contains **source code only**; it is not an installable `.geode` mod.
- It has **not been compiled or tested in Geometry Dash**. The original project uses game hooks and internal gameplay simulation, so compilation success alone would not prove it works safely in-game.
- A matching Geode SDK, Android NDK/toolchain, Geode CLI, and Android64 build are required to compile it.
- Test only with a backup and expect possible crashes or incorrect input behavior. This is an experimental port, not a verified working release.

## Build target
Use Geode's Android64 target (`arm64-v8a`) and a Geode SDK compatible with the installed Geode loader. Do not rename this source ZIP to `.geode`; the compiled package must contain the native Android64 binary.

## Optional cloud build (no PC needed, but a GitHub account is needed)
1. Create a new GitHub repository and upload the contents of this project (the files inside the `Predictive-Buffer-Android-Port` folder, not the parent folder itself).
2. Open the repository's **Actions** tab and run **Build Android64 Geode mod** (or push to `main`/`master`).
3. If the build succeeds, download the `PredictiveBuffer-Android64` artifact from that workflow run. It should contain the `.geode` package.
4. A successful compile is not proof that the mod works correctly in-game; test carefully and remove it if the game crashes or inputs behave incorrectly.
