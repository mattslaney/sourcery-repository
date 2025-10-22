# Sourcery Repository

## Packages

template.toml
template_{DISTROID}.toml
template_{DISTROID}_{RELEASEID}.toml
template_{DISTROID}_{ARCHITECTURE}.toml
template_{DISTROID}_{RELEASEID}_{ARCHITECTURE}.toml
```toml
name = "Name of Package"
desc = "Description of Package"
repo = [ "urls", "for", "source" ]

[build]
command = '''
# build commands, installing dependencies
# environment setup, etc
'''

[install]
prerequisites = [ "build" ]
command = '''
# installation steps
'''

[update]
prerequisites = [ "build" ]
command = '''
# update steps
'''

[uninstall]
command = '''
# uninstall steps
'''

[purge]
command = '''
# purge steps
'''
```

Variables:
 * ARCHITECTURE - Output of uname -m
 * DISTROID - ID from /etc/os-release
 * RELEASEID - VERSION_ID > VERSION_CODENAME

## Collections

template.toml
```
name = "Name of Collection"
desc = "Description of Collection"

[packages]
packagename1
packagename2
packagename3
```

