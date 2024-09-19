---
title: Tech:SSL certificates
---

`{{ {{Ombox|text=Note: For root/apex domains that use Miraheze DNS, you will need to use the second (legacy) method to set up the domain.}} }}`

## Current method (Cloudflare) 

Domain setup can be completed by anybody with access to the Cloudflare account. Initially the domain will show a Cloudflare error page if it hasn't been setup yet.

1. Login to Cloudflare and select the WikiTide Foundation account on the dashboard.

2. Navigate to Websites -> miraheze.org -> SSL/TLS -> Custom Hostnames

3. Click the "Add Custom Hostname" button.

4. Enter in the following values

* Custom Hostname: This this the domain that you are setting up
* Minimum TLS version: 1.2
* Certificate type: Leave this on the default (Provided by Cloudflare)
* Certificate validation method: HTTP Validation

5. Once again, click "Add Custom Hostname"

6. Within a few minutes an SSL certificate will be issued. The domain will show the Miraheze landing page.

7. You need to add the domain to certs.yaml in the SSL repo. For formatting and values, go off of the previous entries in that file.

8. Once the SSL change is deployed, the domain will show the Wiki not Found page. At this point, you can set the domain in ManageWiki, and you are done.

## Legacy method for root/apex domains using Miraheze DNS 

SSL certificates and CSRs can be generated on puppet181 using a shell script (ssl-certificate) to simplify and standardize the process. This can be done only by sre and ssl-admins.

### LetsEncrypt 

[Let's Encrypt](https://letsencrypt.org) is a Certificate Authority that issues free SSL certificates. We'll use the [certbot](https://github.com/certbot/certbot) client.

* Generating a CSR: `/root/ssl-certificate -d <domain> -c`
* Generating a CSR with extra domains: `/root/ssl-certificate -d <domain> -c -s <extra_domain>`
* Generating a LetsEncrypt SSL Certificate: `/root/ssl-certificate -d <domain> -g -p -o`
   * You can also do www. domains too by doing `/root/ssl-certificate -d <domain> -s www.<domain> -g -p -o`
* Generating a Wildcard LetsEncrypt SSL Certificate: `/root/ssl-certificate -d *.<domain> -g -w`
   * You can also do <domain> domains too by doing `/root/ssl-certificate -d <domain> -s *.<domain> -g -p -o -w`
* Renewing a LetsEncrypt SSL Certificate: `/root/ssl-certificate -d <domain> -r -p -o`
   * To renew a wildcard cert: `/root/ssl-certificate -d <domain> -r -w -p -o`

The domain is the fully qualified domain name that will be used as the common name in the certificate and will be the issued domain. The -g option generates a LetsEncrypt SSL certificate for the domain, and the -r option renews (regenerates) a LetsEncrypt certificate if the private key exists at the correct location.

For LetsEncrypt certificates, the public and private components are automatically added and pushed to their respective git repositories, both for new certificates and renewals. If you need to completely regenerate a certificate, use the renew option to avoid adding a duplicate entry to certs.yaml.

For CSR/Private key generations, these keys will be located at `/root/<domain.csr>` and `/root/<domain>.key`. Private key will need to be added as <domain.key> in `/home/ssl-admins/ssl-keys`, then committed and pushed.

For debugging purposes, public keys are handled in `/srv/ssl/ssl`.

To remove an LE certificate, run the following:
```
 sudo /root/ssl-certificate -d <domain> --revoke
```
Then answer yes to all the questions. This will revoke the cert and remove the private key from our system. Then you have to manually remove the public key by deleting the actual key from the certificate's directory, and removing the entry from certs.yaml.

For a non-LE cert, both the public and private keys would have to be removed manually.
 `{{ {{anchor|wildcard}} }}`As of November 24 2018. ACMEv2 (notably, Wild-card certificate) via Let's Encrypt is supported by our backend LE tool.

### Certificate Authority 

* Rule of thumb for acceptable CA on Miraheze is that it is trusted on the latest version of [Mozilla Firefox](https://meta.miraheze.org/wiki/:w:Mozilla_Firefox).
* StartSSL and WoSign are dead. Such is the fate when you make browsers angry.

## See also 

* [Custom domains](https://meta.miraheze.org/wiki/Custom_domains)

## Categories

* [Category:Guides for sysadmins](https://meta.miraheze.org/wiki/Category:Guides_for_sysadmins)



----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:SSL_certificates)**