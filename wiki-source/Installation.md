# Install on PS Vita

The repository documents a VitaShell folder-install route for this port. After installing the VPK, copy the original game's `game/` folder into the application's title-ID directory.

## Before you begin

- Download the port VPK.
- Obtain the original PC game from [Steam](https://store.steampowered.com/app/1406020/Sakura_Succubus_3/).
- Extract or otherwise access the original game's `game/` folder.
- Have VitaShell available on the Vita.

> [!IMPORTANT]
> **MUST KNOW!!** The port VPK and original game data are separate. The target folder is `ux0:/app/RNPYSSIII/`.

## Install with VitaShell

1. Download the VPK to your PC or device.
2. Extract the VPK like a ZIP/RAR archive into a new folder.
3. Transfer the extracted folder to the Vita.
4. Open **VitaShell**.
5. Highlight the folder without opening it.
6. Press **TRIANGLE**, open **More**, then select **Install folder**.
7. Confirm the two prompts.
8. Copy the original game's `game/` folder into:

```
ux0:/app/RNPYSSIII/
```

9. Launch the port from LiveArea.

## Verify

- Confirm the destination directory name matches the title ID above.
- Confirm the final path is `ux0:/app/RNPYSSIII/game/`.
- Keep the `game` directory name intact.
