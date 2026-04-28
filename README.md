<p align="center">
  <img width="300" src="https://github.com/taimleek-afk/send2ue/blob/main/docs/images/1.png?raw=true" alt="icon"/>
</p>
<h1 align="center">Send to Unreal</h1>
<br></br>

[![Docs](https://github.com/taimleek-afk/send2ue/actions/workflows/docs.yml/badge.svg)](https://github.com/taimleek-afk/send2ue/actions/workflows/docs.yml)
[![Tests](https://github.com/taimleek-afk/send2ue/actions/workflows/tests.yml/badge.svg)](https://github.com/taimleek-afk/send2ue/actions/workflows/tests.yml)

A Blender addon for sending assets directly from Blender to Unreal Engine with one click.

### NOTE: This is a fork of [poly-hammer/BlenderTools](https://github.com/poly-hammer/BlenderTools).


## Send to Unreal

![4](docs/images/send2ue/4.gif)

A one-click solution for sending assets from Blender to Unreal Engine.

<h2 align="center">
  <a href="https://github.com/taimleek-afk/send2ue/releases?q=Send+to+Unreal&expanded=true">⬇️ Download Addon</a>
</h2>


## ⚠️ Important: Enable Legacy FBX Importer in Unreal Engine

Starting from Unreal Engine 5.3+, the new **Interchange** import system is enabled by default, which may cause issues with the addon. You need to switch back to the **Legacy FBX importer**.

### Option 1 — Console (Temporary)

Open the console with `~` and type the command **without** the `=` sign:

- Disable Interchange (use Legacy FBX):
```
Interchange.FeatureFlags.Import.FBX False
```
- Re-enable Interchange:
```
Interchange.FeatureFlags.Import.FBX True
```

### Option 2 — Config File (Permanent)

To keep the setting after restarting the project, add the following to your `DefaultEngine.ini`:

**Path:** `YourProject/Config/DefaultEngine.ini`

```ini
[ConsoleVariables]
Interchange.FeatureFlags.Import.FBX=False
```
