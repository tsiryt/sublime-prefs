This repository holds my Sublime Text settings.

# Requirements
Package Control has to be installed on every machine.

# Setup origin
Using `Preferences/Browse packages`, locate Packages/User directory.

```
cd <path>/Sublime\ Text\ 3/Packages/User
git init
git add Package\ Control.sublime-settings
git commit -am "settings from from <device name>"
git remote add origin https://github.com/<github name>/<repo name>.git
git push -u origin master
```

# Pulling settings to other machines

```
cd <path>/Sublime\ Text\ 3/Packages/User
git init
git remote add origin https://github.com/<github name>/<repo name>.git
rm Package\ Control.sublime-settings
git fetch
git checkout -t origin/master
```
