# tcz

Autojump for Total Commander.

## Installation

- Copy tcz_cd.py into one of the subdirectory:

    ```
    cd totalcmd
    mkdir tools
    copy /path/to/tcz.py tools
    ```

    The above commands will copy `tcz.py` into `%COMMANDER_PATH%\tools`.

- Setup user command for tcz:

    Edit your `usercmd.ini`, add following config:

    ```dosini 
    [em_tcz_mru]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-m
    
    [em_tcz_history]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-m
    
    [em_tcz_forward]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-f
    
    [em_tcz_backward]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-b
    
    [em_tcz_project]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-p
    
    [em_tcz_root]
    cmd=%COMMANDER_PATH%\tools\tcz_cd.py
    param=-r
    ```