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

Starting with Manager 1.34, signed mods can also use older game revisions without
being registered in a compatibility pack. Each game update includes a complete clean
fingerprint catalog and compact differences from retained historical catalogs. The
Manager uses those fingerprints to verify the mod's original resources and companion
content, even for a package it has never seen. Releasing another compatible mod requires
no Manager update or compatibility-data publication. Only changes to actual game content
can require adaptation; a different build number alone does not reject a mod. Existing
migrations and reviewed exceptions still apply where game content really changed.

Manager 1.32 distinguishes Windows permission errors, missing files and real file locks.
Permission errors explain when to run the Manager as administrator. Lock errors name
the blocking application when Windows can identify it. Read-only resource files are
made writable for mod changes; folder permissions and security rules are kept.

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

Starting with Manager 1.28, game-changing actions also check both signed update
indexes before they begin. This catches updates published while the Manager stays
open, including replacements for the same game build. A detected application or
compatibility update blocks mod changes until it is installed. Dismissing the
notice or subsequently going offline does not clear a known pending update.
These parallel checks download only indexes, with no game scan or game-file copy.
When GitHub is unreachable and no newer update is known, matching cached support
remains usable. Local game-revision checks still run before and during file writes.

Full application self-updating is available beginning with Manager 1.24. Earlier
builds only support compatibility-data downloads and require this initial upgrade.

This is an unofficial community tool and is not affiliated with the game's developer
or publisher. Do not submit game archives or private keys in issues.
