steamUrlButton

One-click open a teammate's Steam profile from the ESC squad menu.

Press ESC, then press F7. A [Profile] button appears to the right of each squad member. Click it to open that player's Steam profile in the Steam overlay browser.

Dependency: Bingus Shared Loader v15 or newer

Usage

Opening the buttons
- Enter the game (main menu / ship / mission all work).
- Press ESC to open the squad menu.
- Press F7 -> a [Profile] button appears to the right of each squad member.
- The first time you press F7, it triggers a memory scan (about 6-15 seconds). During this, "Scanning players..." appears in the top right, and all 4 rows of buttons are gray.
- When the scan finishes, players with Steam data have their [Profile] button light up.

Clicking the buttons
- Lit [Profile] -> clicking it automatically opens the Steam overlay and jumps to that player's Steam profile.
- Gray [Profile] -> that player's Steam data hasn't been scanned yet; it can't be clicked.

Closing the buttons
- Press F7 again -> the buttons disappear.
- Or just close the ESC menu -> the buttons disappear automatically.

Hotkeys
F7: Toggle [Profile] buttons. Condition: ESC menu must be open.
F6: Rescan players in the current match. Condition: anytime; ESC not required.

When to press F6 to rescan
- A player joins mid-match: the new row's [Profile] is gray. Press F6 to rescan -> it lights up.
- A player leaves mid-match: the old row's [Profile] is lit but clicking it will fail. Press F6 to rescan -> it turns gray.
- Everything is fine: no need to press.

Warning: A scan takes about 15 seconds (depending on your machine). Don't spam F6. Pressing it during an active scan is ignored, but repeated presses put extra read load on the game.

FAQ
- No response to F7:
  Cause: (1) ESC menu isn't open; (2) loader version is too old.
  Fix: Open ESC first, then press; check the loader version.
- Keeps showing Scanning:
  Cause: It's scanning; normal.
  Fix: Wait 15 seconds.
- Someone's [Profile] is gray:
  Cause: They just joined, or the mapping hasn't been scanned yet.
  Fix: Press F6 to rescan.
- After clicking [Profile], browser doesn't open:
  Cause: Steam client isn't running / overlay is disabled.
  Fix: Check whether "In-Game Overlay" is enabled in Steam settings.
- No logs at all:
  Cause: Mod isn't loaded.
  Fix: Check in BingusSharedLoader.log whether mods/codex/stingray_probe is loaded.
- Installed but no effect:
  Cause: Deploy didn't take effect.
  Fix: Re-deploy once from the manager.

Behavior notes
- The mod only reads game memory.
- No memory modification, no external processes: pure lookup + open browser.
- Local: all data exists only in memory; no files written, no network upload.
- Cross-platform players have no Steam profile: PSN / Xbox players don't have Steam64 IDs, so their [Profile] row stays gray.
- One scan per match: if players change mid-match, you need to manually press F6; it won't auto-rescan.

steamUrlButton (untest) V1

Thanks to all the open-source work out there—the approaches and API calls gave me a lot of inspiration. Thanks to DS.
