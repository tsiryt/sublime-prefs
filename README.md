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

# Manual actions

#
# Set unsaved view name

- Open Command Palette
- Type `PRV:` and select `PackageResourceViewer: Open Resource`
- Select `Default`
- Select `set_unsaved_view_name.py`
- Find `if syntax != 'Packages/Text/Plain text.tmLanguage'`:
- Select from there to the end of the `if` statement (the first return statement) (Python is indentation based) inclusive `return` to be commented out.
- Go to the Edit menu -> Comment -> Toggle Comment
- Save the file
- Ensure that, in your preferences (user, syntax specific etc.), `set_unsaved_view_name` is not set to `false`