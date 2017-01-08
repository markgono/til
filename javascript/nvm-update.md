# Updating Node with NVM

When updating Node with NVM you can grab a list of the latest remotely available versions with `nvm ls-remote --lts`.

When updating to a new version - `v6.9.4`, for example - you can copy over your pre-existing packages during the install with `nvm install v6.9.4 --lts --reinstall-packages-from=v6.9.2`

Finally, preset your console default to the new node installation using `nvm alias default v6.9.4`.
