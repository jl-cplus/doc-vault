# Pacman Cheatsheet

Pacman is the package manager for Arch Linux. It handles installing, updating, removing, and querying software packages.  

### System Maintenance
```
pacman -Syu    update system (sync + refresh + upgrade)
pacman -Syy    force refresh all package databases
pacman -Scc    clear package cache
```

### Package Installation
```
pacman -S <pkg>     install a package
pacman -U <file>    install from local file (.pkg.tar.zst)
pacman -Sy <pkg>    refresh database + install package
```

### Searching
```
pacman -Ss <pkg>    search for a package in repos
pacman -Si <pkg>    show detailed info about a package in repos
```

### Package Removal
```
pacman -R <pkg>      remove package only
pacman -Rn <pkg>     remove package + config files
pacman -Rns <pkg>    remove package + config + unused deps
```

### Listing & Info
```
pacman -Ql <pkg>    list files installed by package
pacman -Qi <pkg>    show detailed info about installed package
pacman -Qs <pkg>    search installed packages
```

### Query
```
pacman -Q            list all installed packages
pacman -Q <pkg>      check if a package is installed
pacman -Qe           list explicitly installed packages
pacman -Qd           list dependencies
pacman -Qdt          list orphaned packages
pacman -Qm           list foreign packages (AUR/manual install)
pacman -Qo <file>    find which package owns a file
pacman -Qk <pkg>     verify package files
pacman -Qn           list native packages (official repos)
pacman -Qp <file>    query a package file (not installed)
```
