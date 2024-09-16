---
title: Tech:Swift
---

Swift is a OpenStack run project that offers cloud storage software using a API.

**Remember to run `. /etc/swift-env.sh`, which will make sure you have the credentials for the `swift` command.**

## List containers / objects 

* To list all containers by doing `swift list`.
* To list all files within a container by doing `swift list <container>`.
* To list all files within a path by doing `swift list <container> --prefix <folder name or object name>`.
* To report the size, you can either add `-l` or in human format `--lh`.

## Transferring files (swift upload and swift download) 

The main reason for having to do this is if the files are too large to be downloaded with Special:DataDump. Use the following steps:

* Download the files from the wiki, using ` swift download miraheze-examplewiki-local-public -D examplewiki-images`.
* Zip the files that have been downloaded
* Upload the files to a container (for example if manually providing a dump) you can use ` swift upload miraheze-examplewiki-dumps-backup <filename>`.
* Access the files using `https://example.miraheze.org/wiki/Special:DataDump?action=download&dump=<name of dump>-images`

## Statistics 

You can run the following `swift stat <container>` to get the stats on the container.

You can run the following `swift stat <container> <file name>` to get stats for a file.

## Create an account file 

* Run `swift-ring-builder account.builder create 10 1 1`.
* `{{ {{note}} }}` The partition size must be nearest to the power of 2.
* Run `swift-ring-builder account.builder rebalance`.
* Run `swift-ring-builder account.builder` to see your changes.
* Once you are happy with the changes, deploy the account file by copying to `/root/private/files/swift`.

## Adding a new account server 

You can find this file at `/root/private/files/swift`. Copy it elsewhere so your changes aren't deployed unless you are happy with them. After you've run the following, copy the files back to `/root/private/files/swift`.

* Run the following, remember to replace where <REPLACE_HINT> are listed. `swift-ring-builder account.builder add --region 1 --zone 1 --ip <REPLACE_IP> --port 6000 --device <REPLACE_HARDDRIVE_NAME> --weight 100`.
* `{{ {{note}} }}``--device` is basically the folder it'll be stored under /srv/node on the swift account server you are adding.
* Run `swift-ring-builder account.builder rebalance`.
* You can see your changes with `swift-ring-builder account.builder`.
* Once you are happy with the changes, deploy the account file by copying back to `/root/private/files/swift`.

## Create a container file 

* Run `swift-ring-builder container.builder create 10 1 1`.
* `{{ {{note}} }}` The partition size must be nearest to the power of 2.
* Run `swift-ring-builder container.builder rebalance`.
* Run `swift-ring-builder container.builder` to see your changes.
* Once you are happy with the changes, deploy the container file by copying to `/root/private/files/swift`.

## Adding a new container server 

You can find this file at `/root/private/files/swift`. Copy it elsewhere so your changes aren't deployed unless you are happy with them. After you've run the following, copy the files back to `/root/private/files/swift`.

* Run the following, remember to replace where <REPLACE_HINT> are listed. `swift-ring-builder container.builder add --region 1 --zone 1 --ip <REPLACE_IP> --port 6000 --device <REPLACE_HARDDRIVE_NAME> --weight 100`.
* `{{ {{note}} }}``--device` is basically the folder it'll be stored under /srv/node on the swift account server you are adding.
* Run `swift-ring-builder container.builder rebalance`.
* You can see your changes with `swift-ring-builder container.builder`.
* Once you are happy with the changes, deploy the container files by copying back to `/root/private/files/swift`.

## Create an object file 

* Run `swift-ring-builder object.builder create 10 1 1`.
* `{{ {{note}} }}` The partition size must be nearest to the power of 2.
* Run `swift-ring-builder object.builder rebalance`.
* Run `swift-ring-builder container.builder` to see your changes.
* Once you are happy with the changes, deploy the object file by copying to `/root/private/files/swift`.

## Adding a new object server 

You can find this file at `/root/private/files/swift`. Copy it elsewhere, so your changes aren't deployed unless you are happy with them. After you've run the following, copy the files back to `/root/private/files/swift`.

* Run the following, remember to replace where <REPLACE_HINT> are listed. `swift-ring-builder object.builder add --region 1 --zone 1 --ip <REPLACE_IP> --port 6000 --device <REPLACE_HARDDRIVE_NAME> --weight 100`.
* `{{ {{note}} }}``--device` is basically the folder it'll be stored under /srv/node on the swift object server you are adding.
* Run `swift-ring-builder object.builder rebalance`.
* You can see your changes with `swift-ring-builder object.builder`.
* Once you are happy with the changes, deploy the object file by copying back to `/root/private/files/swift`.

## Help Resources 

* [Create Rings](https://docs.openstack.org/swift/queens/install/initial-rings.html)
* [Removing a object server](https://mindmajix.com/openstack/removing-nodes-from-a-cluster)

[Category:Services](https://meta.miraheze.org/wiki/Category:Services)

----
**Source**: https://meta.miraheze.org/wiki/Tech:Swift