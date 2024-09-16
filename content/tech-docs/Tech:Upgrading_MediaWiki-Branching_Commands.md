---
title: Tech:Upgrading MediaWiki/Branching Commands
---

* Follow below to branch extensions/skins/core
```
<nowiki>
import os
from json import loads

file = open('users/me/mediawiki/.branches.json', 'r')

file = file.read()
file = loads(file)
extensions = os.popen('git -C /users/me/mediawiki config --file .gitmodules --get-regexp path | awk \'{ print $2 }\'').read().split('\n')
print(extensions)
for branch in file.keys():
    if branch != 'default':
        for ext in file[branch]:
            print(f'fixing {ext} for {branch}')
            os.system(f'cd /users/me/mediawiki && git submodule set-branch --branch {branch} -- {ext} && cd {ext} && git checkout {branch} && git pull')
            extensions.remove(ext)
for ext in extensions:
    branch = file['default']
    print(f'fixing {ext} for {branch}')
    os.system(f'cd /users/me/mediawiki && git submodule set-branch --branch {branch} -- {ext} && cd {ext} && git checkout {branch} && git pull')
</nowiki>
```

----
**Source**: [https://meta.miraheze.org/wiki/Tech:Upgrading_MediaWiki/Branching_Commands](https://meta.miraheze.org/wiki/Tech:Upgrading_MediaWiki/Branching_Commands)