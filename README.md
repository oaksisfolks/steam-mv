# steam-mv

Move Steam applications with large files to another install folder.

### Why?

[This bug.](https://github.com/ValveSoftware/steam-for-linux/issues/4851)

### Dependencies:

* Steam Client for Linux.

* Python 3.4 or newer.

* Python modules [vdf](https://github.com/ValvePython/vdf), [progress](https://github.com/verigak/progress/), and [psutil](https://github.com/giampaolo/psutil).

### Features: 

* Interactive. No command line options needed.

* Moves any Steam app with a Steam manifest/AppID from one Steam Library Folder to another. 

##### New:

* Should now work with Steam Library Folders created on Windows. (See this [PR](https://github.com/tinfoil-hacks/steam-mv/pull/2))

* Apps are alphabetically sorted.

* Terminates Steam Client processes before moving files to prevent client from freaking out. (The script asks for permission.)

* Checks available free space and total file size of move before moving. Exits gracefully if there isn't enough room.

* Progress bar based on file count.

* Refactored and readable. Obeys PEP8.

### Installation:

1. Make sure you have python 3.4 or greater. 

    ```
    python3 --version
    ```

2. Install python-vdf, python-psutil, & python-progress. Look in your repos, or use pip.

    ```
    pip3 install vdf psutil progress
    ```

3. Clone using git.

    ```
    cd ~
    git clone https://github.com/tinfoil-hacks/steam-mv.git
    ```

4. Mark the script executable. 

    ```
    chmod u+x ~/steam-mv/steam-mv
    ```

5. Create a symlink to `steam-mv` in `/usr/local/bin`.

    ```
    username=$(whoami)
    sudo ln -s /home/${username}/steam-mv/steam-mv /usr/local/bin/steam-mv
    ```

### Usage:

`$ steam-mv`
