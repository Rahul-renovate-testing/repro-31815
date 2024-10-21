# Test Details

Validate that `npmToken` when not present in the `encrypted` object (generally when Mend app use the portal to add such secrets) is passed into the config and replaced inside the `npmrc` string.

To do this add `npmToken` as secrets in the file config (this is how Mend app passes token from portal to renovate bot). Then confirm that the token is first decrypted (if needed) and then replaced with the in the `npmrc` string.
