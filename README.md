## pacaur_installed ##
to list out the common package for daily use  

1. For Development : https://rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed
1. For Production  : https://cdn.rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed

## operation ##
### to backup :###
```pacaur -Q |awk -e '{print }' > pacaur_installed```

### to restore : ###
```
export MAKEPKG="makepkg --skipinteg --skipchecksums --skippgpcheck"

pacaur -S --needed --noconfirm --noedit  $(curl  https://cdn.rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed |egrep -v "^[#| ]")
```

BR,
Louis
http://www.louislabs.com//
