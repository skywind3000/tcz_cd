# Preface

A fuzzy `cd` command for Total Commander by learning your habit.


## Features

`tcz_cd` can study the directory history in TC and helps you change directory rapidly with a fuzzy finder:

![](https://raw.githubusercontent.com/skywind3000/images/master/p/tcz_cd/demo.png)

Possibilities:

- Jump in history directories (aka, Most Recently Used dirs).
- Jump in project directories.
- Jump forward.
- Jump backward.

## Requirements

Install one of the supported fuzzy finders (`peco`, `gof` and `fzf`) in your windows:

```dosbatch
scoop install peco
```

`peco` and `gof` are recommended because `fzf` cannot display wide unicode characters correctly in Windows.

## Installation

Copy tcz_cd.py into one of the subdirectory:

    ```
    cd totalcmd
    mkdir tools
    copy /path/to/tcz.py tools
    ```

    The commands above will copy `tcz.py` into `%COMMANDER_PATH%\tools`.

Edit your `usercmd.ini` and add the following code:

    ```dosini 
    [em_tcz_mru]
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
After this, you can try `em_tcz_mru` in TC's command line. If it works correctly, assign a keymap for these commands, edit `wincmd.ini`:

    ```
    [Shortcuts]
    A+L=em_tcz_mru
    A+P=em_tcz_forward
    ```

## Usage

Type `em_tcz_mru` in your tc's command line:

![](https://raw.githubusercontent.com/skywind3000/images/master/p/tcz_cd/tcz_cmd.png)

Press `ENTER` and fuzzy finder peco will display:

![](https://raw.githubusercontent.com/skywind3000/images/master/p/tcz_cd/peco.png)

Try to input something, press `ENTER` to accept, `ESC` to give up and `CTRL`+`J`/`K` to move cursor up and down.

Once a candidate is accepted by `ENTER`, it will tell tc to change the current directory to the destination.

## Credit

Tornado
