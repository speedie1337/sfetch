# sfetch
#### speedie's fetch for macOS/Mac OS X and Linux

![image](https://user-images.githubusercontent.com/71722170/154552334-e50f6986-5222-4ecf-bf87-6c414632e498.png)


Was bored so I decided to write a fetch tool! 

## It currently fetches:
- Your distro
- Your kernel and version
- Your shell (zsh, bash, fish, etc.)
- Your package count (Linux)
- Your Mac (macOS/Mac OS X)

## And has ASCII art for:
- Gentoo Linux
- Funtoo Linux
- Arch Linux
- Fedora Linux
- Debian Linux
- Manjaro Linux
- Project 081 (Mac OS X distro)
- Mac OS X
- macOS
- PearOS (Garbage)
- Cutefish OS (Garbage)
- Linux/Other Distro (used if your OS is none of the above)

## Usage on most GNU/Linux distros

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch

## Usage on Mac OS X (Pre-10.11)

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch

## Usage on Mac OS X (10.11 and later)

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch

## Usage on Mac OS X (10.15 and later)

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch

## Usage on Project 081 (Pre-0.6)

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch

## Usage on Project 081 (0.6 and later)
Already built in, run sfetch in the Terminal to use.

## Usage on NixOS
NOTE: I'm a total fucking normie when it comes to NixOS, if there's a better way to do this, please let me know!

    echo "#!/run/current-system/sw/usr/bin/env $SHELL" > /run/current-system/sw/usr/local/bin/sfetch && \
    curl -o /run/current-system/sw/usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /run/current-system/sw/usr/local/bin/sfetch

## Usage on Alpine Linux (and other distros without GNU coreutils)
NOTE: I cannot provide any support for GNU-less systems!

    echo "#!/usr/bin/env $SHELL" > /usr/local/bin/sfetch && \ 
    curl -o /usr/local/bin/sfetch-base https://raw.githubusercontent.com/speediegamer/sfetch/main/sfetch && \
    cat /usr/local/bin/sfetch-base >> /usr/local/bin/sfetch && \
    chmod +x /usr/local/bin/sfetch && \
    sudo apk install ncurses

## Note
- Has been tested with both zsh and Bash but feel free to try other shells
- Should work on POSIX compliant shells though!

## Test Version

If you wish to use the 99.9% likely broken version of sfetch, you can get it by using:

    sudo curl -o /usr/bin/sfetch https://raw.githubusercontent.com/speediegamer/sfetch/sfetch-test/sfetch

## Contributing

If you like this project, please contribute with ASCII for more distros. Thank you!

## Having issues?

Issue: tput: command not found or similar
Solution: Install ncurses

Issue: [[ command not found or similar
Solution: Edit the sfetch script and add #!/bin/bash or #!/bin/zsh at the top
