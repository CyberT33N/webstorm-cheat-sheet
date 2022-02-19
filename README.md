# webstorm-cheat-sheet
webstorm cheat sheet with the most needed stuff..



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
