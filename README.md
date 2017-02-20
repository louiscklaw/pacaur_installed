## pacaur_installed ##
to list out the common package for daily use  

1. For Development : https://rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed
1. For Production  : https://cdn.rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed

## operation ##
### to backup :###
```
pacaur -Q |awk -e '{print $1}' > pacaur_installed
```

### to restore : ###

* configuration file location:  
`/etc/pacman.conf`

1. add repository   
```
[apricity-core]
SigLevel = TrustAll
Server = http://static.apricityos.com/apricity-core-signed/

[archlinuxfr]
SigLevel = Never
Server = http://repo.archlinux.fr/$arch

```

2. command line  
```
export MAKEPKG="makepkg --skipinteg --skipchecksums --skippgpcheck"
pacaur -S --needed --noconfirm --noedit  $(curl  https://cdn.rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed |egrep -v "^[#| ]")
```

BR,  
Louis  

https://portfolio.louislabs.com  
https://github.com/louiscklaw  

