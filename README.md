# CZN Mod Manager updates

This repository distributes signed game-compatibility data and complete CZN Mod
Manager application releases. It does not contain CZN game code, clean game
resources, private migration records, original mod packages, or signing secrets.

The Manager verifies downloads against a public key built into the application.
Downloading a key from this repository does not establish trust.

Compatibility updates match the exact installed game revision. Missing support blocks game-file
changes and preserves the mod library and selected load order. A game update can
replace only some files; clean recovery data may still require the official
launcher's Verify/Repair. The Manager does not delete game resources.

Complete application updates use a separate, fixed `application-updates` release.
Its signed indexes point to complete app releases. Game compatibility updates and
application updates are distributed independently.

The Manager checks for application updates and game compatibility updates each time
it starts, even if no game is detected. New compatibility data downloads automatically.
An available app update prompts you to update and restart. Unchanged installations stay
quiet. You can also choose **Tools > Check for updates** at any time. An available application
update offers **Update and restart**. It can replace the outer launcher, packaged
runtime, native components and legal files, and add or retire application files.
Libraries, settings, selections, backups and Qt overrides are preserved. Downloads
are verified before replacement. A retained helper waits for the Manager to exit,
keeps a durable rollback journal, and checks that the new app starts. Interrupted
updates recover on the next launch.

Full application self-updating is available beginning with Manager 1.24. Earlier
builds only support compatibility-data downloads and require this initial upgrade.

This is an unofficial community tool and is not affiliated with the game's developer
or publisher. Do not submit game archives or private keys in issues.
