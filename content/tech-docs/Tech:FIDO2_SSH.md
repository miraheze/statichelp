---
title: Tech:FIDO2 SSH
---

If you have access to a FIDO2 key, you can use it to add 2FA to your SSH login.

 `{{ {{hatnote|This was only tested on Linux with OpenSSH, other operating systems may require additional steps, and other client software may not support FIDO2. You also need up-to-date versions of OpenSSH, which you should use anyway.}} }}`

## Generating the key

There are two options when creating FIDO2-backed keys: sk-ssh-ed25519 and sk-ssh-ecdsa. Due to [policy](https://meta.miraheze.org/wiki/Tech:Appointment_and_revocation_policy#New_Access), only Ed25519 keys are allowed.

Generate your key via `ssh-keygen -t ed25519-sk -C "comment"`. This will create a non-discoverable key. Some additional considerations.

* **Stay clear of no-name FIDO2 keys!** Avoid knock-offs of dubious security, as they undermine the security of FIDO2 SSH, get a Yubikey if you're going to do this.
* no-touch-required keys are not allowed.
* For added security, do not use resident/discoverable keys.

This will create your standard public key, and a key handle/identification. This identification is not the private key itself. It is only useful to the specific hardware key you used to create the SSH key, so don't lose it and **don't let anyone other than you use it!** However, **treat the identification as if it was the private key anyway**, so make sure to choose a good passphrase (what it is exactly depends on how your key handles these types of keys, see [https://www.yubico.com/blog/yubicos-u2f-key-wrapping/](https://www.yubico.com/blog/yubicos-u2f-key-wrapping/) for how this works on Yubikeys).

## Getting the key on Miraheze

Fork [miraheze/puppet](https://github.com/miraheze/puppet) on GitHub, go to `modules/users/data/data.yaml` and look for your shell account. Replace your SSH public key with your newly generated public key. Get a hold of someone from Infrastructure if you yourself do not have write access to Puppet.

If you use signed commits or OpenPGP, now would be a good time to use them for extra assurance. Example: [https://github.com/miraheze/puppet/pull/3203](https://github.com/miraheze/puppet/pull/3203).

## Account recovery

If your key is broken, you will be locked out from login in. To prevent this, you can create multiple SSH keys using various **different** FIDO2 keys. Just repeat the above process with different keys, and assign their public keys to your shell account. That way, if your main key stops working, you'll not be locked out completely.

Ignore this warning at your own peril: If your key stops working, it could become impossible for SRE to verify that any requests to change your keys on Puppet comes from you. Better to have multiple keys from the get-go.

## See also

* Your GitHub and Miraheze accounts also have privileged access. Consider using WebAuthn with your FIDO2 key there as well
   * GitHub: You can use WebAuthn as your second factor, and you can also use a sk-ssh-ed25519 as your login SSH key for Git there.
      * Per the policy, do not just reuse the SSH key you use to login to Miraheze servers, generate a new one for GitHub.
   * Miraheze: WebAuthn is available as one of the two possible second factors.
* [Pisces's guide to get it working on Windows](https://meta.miraheze.org/wiki/User:Pisces/FIDO2_SSH_on_Windows)

----
**Source**: [https://meta.miraheze.org/wiki/Tech:FIDO2_SSH](https://meta.miraheze.org/wiki/Tech:FIDO2_SSH)