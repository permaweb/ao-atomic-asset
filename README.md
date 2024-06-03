# AO Atomic Asset

[AO Atomic Assets](atomic-asset.lua) follow the token spec designed for exchangeable tokens which can be found [here](https://ao.arweave.dev/#/)

The creation of an atomic asset happens with these steps

1. The [asset process handlers](https://arweave.net/y9VgAlhHThl-ZiXvzkDzwC5DEjfPegD6VAotpP3WRbs) are fetched from Arweave
2. Asset fields are replaced with the values submitted by the user
3. A new process is spawned, with the tags and asset data included
4. A message is sent to the newly created process with an action of 'Eval', which includes the process handlers
5. A message is sent to the profile that created the asset in order to add the new asset to its Assets table