# New Pidcat 
>Since [JakeWharton/pidcat][1] was little bit outdated.

## New Features
- Compatible with Windows ([Windows Terminal][2] Only).
- Support output original-form content to file.
- Support file based multi-tags filtering.
    >When `-y` (`--yes`) option is enabled, 
    `.pidcat_tags_ignore` in the current working directory is used for tag filtering.
    Same with  `.gitignore`, each line starting with `#` will be treated as comment 
    and prefix `!` means to discard the matched tag. 

## Pre-requests
- [Python**3**][3]
- [Android SDK][4]    
    
## Usage

### Windows Terminal
Step 0. Download NewPidcat  

Step 1. Create profile.ps1 in case you don't have it.   
>`if (!(Test-Path -Path $PROFILE )) { New-Item -Type File -Path $PROFILE -Force }`  

Step 2. Edit your profile.ps1 with any editor you like.  
>e.g. `notepad $PROFILE`  

Step 3. Add following two lines:   
>Function NEW_PIDCAT { python *your\path\to\pidcat.py* $args }  
Set-Alias -Name pidcat -Value NEW_PIDCAT`  

Step 4. Update profile and run with it:  
>`pidcat -h`


### *unix Terminal 

Step 0. Download NewPidcat   

Step 1. Copy somewhere in your `$path`   
>e.g. `cp ./pidcat.py ~/bin/pidcat`

Step 2. Run with it:  
`pidcat --current -c -o -y`


 [1]: https://github.com/JakeWharton/pidcat
 [2]: https://github.com/microsoft/terminal
 [3]: https://www.python.org/downloads/
 [4]: http://developer.android.com/sdk/

