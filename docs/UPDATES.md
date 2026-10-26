# Updates

The updater uses the independent robertmartic/polysheet public GitHub release channel.

Use About > Updates for manual checks, automatic startup checks, last-update details and update storage management. A newer version also shows an Update available button in the header. Manual checks remain available in Settings and View. Settings can disable automatic checks. Only the public release service is contacted; workbooks are never uploaded. No private credentials are in the application.

An installed copy checks newer numeric versions, downloads a full or matching file-level delta package and verifies SHA-256 hashes against release assets and the file manifest. Hashes check integrity; they are not a separately signed release trust chain. A portable copy directs users to the installer.

Before replacement, all PolySheet windows must close and unsaved work is checked. Cancelling the save prompt cancels the update. The helper stages and verifies files, preserves unrelated files and uses a maintenance installer to retain registration and shortcut choices. Failures report their actual state and retain rollback data; success is confirmed after restart and shows the offline changelog. About includes update storage management.

Version 0.1.4 includes a file-level delta from 0.1.3. If the installed files differ from the verified base, the updater uses the full package. Update success, failure, corruption, rollback and interruption are tested with synthetic fixtures. A real installed-app update requires the owner's confirmation after publication.

## Optional PolyHUB integration

This release supports the local PolyHUB protocol for coordinated updates. PolyHUB requests the existing application updater; download controls, save prompts, deltas/full fallback and rollback remain in this application. It also verifies the installed result. The app remains fully usable without PolyHUB. Setup, uninstall and update helpers coordinate maintenance to avoid concurrent changes.
