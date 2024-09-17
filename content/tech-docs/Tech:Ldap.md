---
title: Tech:Ldap
---

Miraheze uses ldap as an authentication system for some of our infrastructure, such as [Grafana](/tech-docs/techgrafana) and Icingaweb2.

You can use `ldapvi` to modify a user, add a user, or change the roles the user has. You can also use [https://ldapwiki.miraheze.org](https://ldapwiki.miraheze.org) to change your password.

You can find the ldap password in /etc/ldapvi.conf. All these steps have to be done using ldap171.wikitide.net.

Terminology:
* cn = Common Name

* sn = Surname

* UID = username you'll login with

* givenName = First Name

## Add New User 

1. Add the following to a file named user.ldif:
```
dn: uid=<uid>,ou=people,dc=miraheze,dc=org
changetype: add
objectClass: top
objectClass: person
objectClass: organizationalPerson
objectClass: inetOrgPerson
uid: <uid>
givenName: <firstName>
sn: <surname>
cn: <cn>
userPassword: <pass>
```

The 'uid' attribute is equal to the username you are using. It is recommended to set the 'cn' attribute equal to the contents of 'uid'. 'givenName' is usually your first name, while 'sn' is your surname.
You cannot directly put your password in this ldif file, instead you need to generate a hash through `sudo -i slappasswd`.

2. Run `ldapadd -x -D cn=write-user,dc=miraheze,dc=org -W -f user.ldif`.

## Add New Group 

1. Add the following to group.ldif

```
dn: cn=<name of group>,ou=groups,dc=miraheze,dc=org
objectClass: top
objectClass: groupOfNames
cn: <name of group>
member:
```

2. Run `ldapadd -x -W -D "cn=write-user,dc=miraheze,dc=org" -f group.ldif`

## Add User to existing group 

1. Create the following in add_member.ldif

```
dn: cn=<group name>,ou=groups,dc=miraheze,dc=org
changetype: modify
add: member
member: uid=<user_uid>,ou=people,dc=miraheze,dc=org
```

2. Run `ldapmodify -x -W -D "cn=write-user,dc=miraheze,dc=org" -f add_member.ldif`

**Alternatively** you can do:

1. Run `modify-ldap-group <group>`.

2. Add `member` with value `uid=<user_uid>,ou=people,dc=miraheze,dc=org`. Must be one per line.

## Modify user field 

1. Add the following to modify.ldif (note you can add and delete):

```
dn: uid=<user>,ou=people,dc=miraheze,dc=org
changetype: modify
delete: memberOf
memberOf: cn=sre,ou=groups,dc=miraheze,dc=org
```

2. Run `sudo ldapmodify -x -D cn=write-user,dc=miraheze,dc=org -W -f modify.ldif`

## Modify Existing User 

1. Run `modify-ldap-user <user>` on the ldap server (so ldap171.wikitide.net).

2. Change the bit you want and save.

## Modify Existing Group 

1. Run `modify-ldap-group <group>` on the ldap server (so ldap171.wikitide.net).

2. Change the bit you want and save.

## Change User Password 

1. Run `slappasswd`.

2. Run `ldapvi` on the ldap server (so ldap171.wikitide.net).

3. Locate the user you want to change and then locate the password field.

(Use the {SSHA} you got from the previous step).

4. Save.

## Change admin password 

To change the admin password do the following:

1. Run `slappasswd`

2. Run the following:

```
ldapmodify -Q -Y EXTERNAL -H ldapi:/// << E0F
dn: olcDatabase={1}mdb,cn=config
changetype: modify
replace: olcRootPW
olcRootPW: {SSHA got from first step}
E0F
```

3. Run `ldappasswd -x -D cn=admin,dc=miraheze,dc=org -W -S`

(Don't forget to change the password in the private puppet repo too)

## Adding base dn 

1. Add the following to a .ldif file

```
dn: ou=people,dc=miraheze,dc=org
objectClass: organizationalUnit
ou: people

dn: ou=groups,dc=miraheze,dc=org
objectClass: organizationalUnit
ou: groups
```

2. Run `sudo ldapadd -x -D cn=admin,dc=miraheze,dc=org -W -f basedn.ldif`

(The password can be found in the private puppet repo)

## Deleting user or group 

To delete a **user** do the following:

1. Run `ldapdelete -W -D "cn=write-user,dc=miraheze,dc=org" "uid=<user uid>,ou=people,dc=miraheze,dc=org"`.

To delete a **group** do the follow:

1. Run `ldapdelete -W -D "cn=write-user,dc=miraheze,dc=org" "cn=<group name>,ou=people,dc=miraheze,dc=org"`.

## LDAP Index 

1. Add the following to index.ldif:

```
dn: olcDatabase={1}mdb,cn=config
changetype: modify
add: olcDbIndex
olcDbIndex: cn pres,sub,eq
-
add: olcDbIndex
olcDbIndex: sn pres,sub,eq
-
add: olcDbIndex
olcDbIndex: uid pres,sub,eq
-
add: olcDbIndex
olcDbIndex: displayName pres,sub,eq
-
add: olcDbIndex
olcDbIndex: default sub
-
add: olcDbIndex
olcDbIndex: uidNumber eq
-
add: olcDbIndex
olcDbIndex: gidNumber eq
-
add: olcDbIndex
olcDbIndex: mail,givenName eq,subinitial
-
add: olcDbIndex
olcDbIndex: dc eq
```

2. Run `ldapmodify -Y EXTERNAL -H ldapi:/// -f ./index.ldif`

## Existing LDAP groups 

```
sre
sre-mediawiki
sre-infrastructure
sre-management
stewards
cvt
matomo-users
users
board
trustandsafety
```
*Note: Non-exhaustive list*

## Monitoring 

LDAP can be monitored via Grafana by accessing [this link](https://grafana.wikitide.net/d/uOLD33lMz/ldap?orgId=1).

## Categories

* [Category:Technology guidelines and guides](https://meta.miraheze.org/wiki/Category:Technology_guidelines_and_guides)

----
**[Go to Source &rarr;](https://meta.miraheze.org/wiki/Tech:Ldap)**