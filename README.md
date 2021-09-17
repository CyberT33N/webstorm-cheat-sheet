# webstorm-cheat-sheet
webstorm cheat sheet with the most needed stuff..



<br><br>

# Resolve merge conflicts
- Right click on project > Git > Resolve Conflicts 


<br><br>

# Resolve perfomance problems
- File > Invalidate Caches
































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

## global search does not show all results
- Click File -> Invalidate Caches / Restart..
  - Click the button "Invalidate and Restart"
    - After restart, try run the search again

