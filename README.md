## pacaur_installed ##
to list out the common package for llaw daily use  

## operation ##
### to backup :###
```pacaur -Q |awk -e '{print }' > pacaur_installed```

### to restore : ###
```
pacaur -S --needed --noconfirm --noedit  $(curl  https://cdn.rawgit.com/louiscklaw/pacaur_installed/master/pacaur_installed |egrep -v "^[#| ]")
```
