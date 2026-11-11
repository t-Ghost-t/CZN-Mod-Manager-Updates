# CZN Mod Manager compatibility updates

Signed compatibility data for CZN Mod Manager. This repository distributes data only.
It does not contain CZN game code, clean game resources, private migration records,
mod artwork packages, or signing secrets.

The manager selects support for the exact installed resource revision and verifies it
against a public signing key embedded in the application. Downloading a key from this
repository does not establish trust. Changed game formats require an application update.

Release assets include a signed stable index and a separate signed preview index.
Preview support is for owner testing and is rejected by stable application builds.
A published preview does not mean gameplay or native Windows testing has passed.

If support for a new game revision is unavailable, the manager keeps the library and
selected load order and blocks changes to game resources until matching support exists.
Close both the game and launcher before applying mods. Missing clean data may require
Verify/Repair in the official launcher. The manager does not delete game resources.

This is an unofficial community tool and is not affiliated with the game's developer
or publisher. Do not submit game archives or private keys in issues.
