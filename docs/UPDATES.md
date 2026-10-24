# Updates

The updater uses the independent robertmartic/polysheet public GitHub release channel.

Settings can disable automatic checks. Only the public release service is contacted; workbooks are never uploaded. No private credentials are in the application.

An installed copy checks newer numeric versions, downloads a full or matching file-level delta package and verifies SHA-256 hashes against release assets and the file manifest. Hashes check integrity; they are not a separately signed release trust chain. A portable copy directs users to the installer.

Before replacement, all PolySheet windows must close and unsaved work is checked. Cancelling the save prompt cancels the update. The helper stages and verifies files, preserves unrelated files and uses a maintenance installer to retain registration and shortcut choices. Failures report their actual state and retain rollback data; success is confirmed after restart and shows the offline changelog. About includes update storage management.

This first release has no earlier PolySheet binary base, so a real delta is not applicable. The packaging script accepts a verified earlier manifest for later versions. Update success, failure, corruption, rollback and interruption are tested with synthetic fixtures. A real installed-app update requires the owner's confirmation after publication.
