# webstorm-cheat-sheet
webstorm cheat sheet with the most needed stuff..







bstorm (https://www.jetbrains.com/de-de/webstorm/)

## Plugins
- Monokai Pro Theme(https://plugins.jetbrains.com/plugin/13643-monokai-pro-theme)
- Atom Material Icons
- Tabnine
- CodeGlance (Minimap)
- Pokemon Progress
- Activate-power-mode (https://plugins.jetbrains.com/plugin/14000-activate-power-mode-x)
- Power Mode II
- Rainbow Brackets
- Sexy Editor (https://plugins.jetbrains.com/plugin/1833-sexy-editor)
- Anime Memes (https://plugins.jetbrains.com/plugin/15865-anime-memes)
- Rainbow Fart (https://plugins.jetbrains.com/plugin/14543-rainbow-fart)
- Fancy music (https://plugins.jetbrains.com/plugin/13231-fancy-music)
- Key Promoter X (https://plugins.jetbrains.com/plugin/9792-key-promoter-x)

<br><br>

## Increae search limit results from 100 to xxxx
- In 2021.2 the limit is configurable in Settings | Advanced Settings | Maximum number of results to show in Find In Path/Show Usages preview.


<br><br>

## Enable Zoom with CTRL + Mouse Wheel
- In the Settings/Preferences dialog Ctrl+Alt+S, select Editor | General. Make sure that the setting Change font size (Zoom) with Ctrl+MouseWheel is enabled.

<br><br>

## Add Unit Tests Sidebar
- Edit Configuration (top right)
<br> -> Choose Mocha package
<br> -> User Interface: **bdd**
<br> -> Extra Mocha options: **--recursive --exit --timeout 30000**
<br> -> File Patterns: **./test/*.test.js**






<br><br> <br><br>

## Enable auto render of JSDoc
- open the Settings/Preferences dialog Ctrl+Alt+S, go to Editor | General | Appearance, and select the Render documentation comments checkbox.










<br><br><br><br>

## Fonts

<br><br>

#### Change Fonts
- File > Settings > Editor > Font

<br><br>

#### Bold Fonts
- File > Settings > Color Scheme > General > Text > Default Text > Bold
- You can to File > Settings > Color Scheme > Javascript to change as example function params to bold too




<br><br>

## disable auto indent
- In  File | Settings | Editor | General | Smart Keys you need to disable Smart indent (this should help for cases when "CLion still sometimes inserts tabs when i dont press TAB key") and set Reformat on paste to None (this should help for cases when "CLion deletes tabs from lines that i paste"):


<br><br>


## Create Desktop Shortcut
- Tools > Create Desktop Entry

<br><br>


## Import Color Scheme
- File > Settings > Editor > Color Scheme > Settings Wheel Icon > Import Scheme
- You can import .xml or .icls
- https://www.jetbrains.com/help/webstorm/settings-colors-and-fonts.html

<br><br>

## Sublime Syntax Color Scheme
- https://gist.github.com/CyberT33N/ef2ae6684f29734ba2263d07fe1548e7 **FINAL almost like atom v2**
- https://gist.github.com/CyberT33N/a3905f0b9da8cebb42d03998d79b6a5f **FINAL almost like atom**
- 
- https://plugins.jetbrains.com/plugin/12773-onedarkmonokai
- https://github.com/darekkay/config-files/blob/master/intellij-idea/config/colors/dk-monokai.icls


<br><br>
<br><br>

## Soft Wraps
- Preferences/Settings | Editor | General > Soft-wrap files (https://www.jetbrains.com/webstorm/guide/tips/soft-wraps/)


<br><br>

## Eslint
- File > Settings > Search: eslint

<br><br>

## Vertical Line Indentation
- Go to Settings/Editor/General/Appearance and select **Show indent guides** to enable this feature in IntelliJ. (https://i.stack.imgur.com/NsoJV.png)




































<br><br>
 _____________________________________________________
 _____________________________________________________

<br><br>

# Resolve merge conflicts
- Right click on project > Git > Resolve Conflicts 


<br><br>

# Resolve perfomance problems
- File > Invalidate Caches
- Delete .idea folder from project




























<br><br>
_________________________________________________
_________________________________________________
<br><br>


# Uninstall Webstorm

<br><br>


## Standalone

<br><br>

#### Linux
- You do not have to delete the standalone folder but you must remove the config files:
```bash
sudo rm -rf ~/.config/JetBrains
sudo rm -rf ~/.cache/JetBrains
sudo rm -rf ~/.local/share/JetBrains
```
























<br><br>
_________________________________________________
_________________________________________________
<br><br>



# Configurations
- You can create Configurations for a lot of stuff like Unit Testing, NPM Scripts and much more..
- If you create any Run Configurations for your Project then they will get saved to the *.idea* folder

<br><br>





























<br><br>
_________________________________________________
_________________________________________________
<br><br>

# Get relative path from current document
```javascript
// You can use Ctrl+Space to get the path auto-generated. Just enter
import {}  from "file"

// Then put the cursor on "file" and hit Ctrl+Space twice - you will get
import {}  from "../../directory2/file"
```




































<br><br>
_________________________________________________
_________________________________________________
<br><br>

# Debugging

## Guides 
- https://blog.jetbrains.com/webstorm/2018/01/how-to-debug-with-webstorm/?_ga=2.84889242.2022406785.1615292477-1756484165.1611909872



<br><br>


## Conditional Breakpoints
- Right-click on a breakpoint to configure its behavior: for instance, you can add a condition so that the execution will only be stopped when that condition is met.

<br>

![Conditional Breakpoints](https://www.jetbrains.com/webstorm/guide/static/263243bc708d14f99c09d16001069900/2a4de/tip.png)


































































<br><br>
_________________________________________________
_________________________________________________
<br><br>


# Known Problems

<br><br>

## National Keyboard Layout not working
- Settings > Keymap > Enable at bottom Box "Use national layout for shortcuts"

<br><br>

## global search does not show all results
- Click File -> Invalidate Caches / Restart..
  - Click the button "Invalidate and Restart"
    - After restart, try run the search again

<br><br>

## node not found (nvm)
- Now if IDE is launched from a terminal, environment variables are loaded correctly.
However, environment variables mismatch occurs if IDE is launched from Desktop or System menu. The problem is that IDE sees environment variables configured in ~/.profile (login shell), but not in interactive shell configuration files (like, ~/.bashrc).

The real problem is that some tools alter interactive shell configuration files only during their installation phase.
E.g. NVM https://github.com/creationix/nvm/blob/v0.28.0/install.sh#L126

Workaround 1: make required variables available in a login shell (i.e. for Bash, move them from .bashrc to .bash_profile or .profile), then restart X session (logout/login).
Workaround 2: run IDE from a terminal
Workaround 3: edit IDE desktop launcher and set command to /bin/bash -l -i -c  "/path/to/webstorm.sh"
