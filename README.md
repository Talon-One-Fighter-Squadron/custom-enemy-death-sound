# Nuclear Option – Kill Detect Mod (BepInEx)

Simple install + run instructions (no build/compile steps)

## You need
- Nuclear Option installed (Steam)
- **BepInEx 5 (x64)** installed for Nuclear Option
- Mod file: **`NO_KillDetect.dll`**

---

## 1) Install BepInEx (one-time)
1. Download **BepInEx 5 x64**.
2. Extract it into your **Nuclear Option game folder** (same folder as the game EXE).
3. Run the game once.
4. Close the game.

After the first run, you should see folders like:
- `BepInEx/`
- `BepInEx/plugins/`
- `BepInEx/config/`

---

## 2) Install the Mod
1. Open your game folder:
   - Steam → Nuclear Option → Manage → Browse local files
2. Go to:
   - `BepInEx/plugins/`
3. Copy NO_KillDetect mod folder into plugins

---

## 3) Custom Sound Install (where to place it)

### Step A: Run once to generate config
1. Start the game once with the mod installed.
2. Close the game.
3. Go to:
- `BepInEx/config/`
4. Open the mod’s config file (it will usually be something like):
- `BepInEx/config/<plugin-guid>.cfg`


### Step B: Place your sound file
If the config does **not** specify a path, use this standard BepInEx convention (recommended):

1. Create a folder:
- `BepInEx/plugins/NO_KillDetect/`
2. Put your sound file inside it, for example: Make sure to name it this same name!!
- `BepInEx/plugins/NO_KillDetect/kill.mp3`



### Step C: Point the config to the file (if needed)
If the config has a path setting, set it to the full/relative path, for example:
- `BepInEx/plugins/NO_KillDetect/kill.wav`

Then launch the game again to test.

---

## 4) Run + Verify It Loaded
1. Launch the game normally.
2. Open this log file:
- `<Game Folder>/BepInEx/LogOutput.log`
3. Search for `NO_KillDetect.dll` or your plugin name to confirm it loaded.

---

## 5) Uninstall
1. Close the game
2. Delete:
- `BepInEx/plugins/NO_KillDetect.dll`

(Optional) delete sounds/config you added:
- `BepInEx/plugins/NO_KillDetect/`
- `BepInEx/config/<plugin-guid>.cfg`

---

## Common Issues
**Mod not loading?**
- Make sure you installed **BepInEx x64**, not x86.
- Confirm the DLL is exactly here: `BepInEx/plugins/NO_KillDetect.dll`
- Run the game once after installing BepInEx so it generates folders/logs.
- Check `BepInEx/LogOutput.log` for errors.

**Custom sound not playing?**
- Double-check the config file under `BepInEx/config/` for the expected filename/path.
- Try a short **.wav** file (1–3 seconds) and avoid exotic codecs.
- Confirm the file path has no typos and the file actually exists.
