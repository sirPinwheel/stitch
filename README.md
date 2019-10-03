# tccli
Twitch Chat Command Line Interface

## Description
tccli is a simple Python script that will connect to any Twitch channel, the idea behind it was to have an alternative to the in-browser chat. I admit it's a solution to the problem not many people have, but at the end of the day the more options the better.

## Installation
#### Requirements
``python3`` python interpreter<br>
``certifi`` python module<br>

#### On Windows
- Clone the repo or download and unpack the zip<br>
- Get Python 3 from official website ``python.org``<br>
- Install python and pip3<br>
- Open command line and run ``pip3 install certifi``<br>

#### On Linux
- Clone the repo or download and unpack the zip<br>
- Get Python 3:
- For Ubuntu:<br>
``sudo apt update: sudo apt install python3 pip3``<br>
- For Arch/Manjaro:<br>
``sudo pacman -Syu python3 pip3``<br>
- Run``sudo pip3 install certifi``<br>
- Done, remember to add -x flag to the script:<br>
``sudo chmod +x tccli.py``<br>

## Usage
Now you can launch the script, it's supposed to be run from the command line (duh).<br>
Run it with ``-h`` argument to get more info about the usage

```
tccli.py needs username, name of the channel and oauth token of that user
You can mix and match what's in the configuration file and what's
passed as the argument to the program, arguments will override data
from the configuration file.

usage:
    python3 tccli.py [option 1] <arg 1> [option 2] <arg 2>...
    ./tccli.py [option 1] <arg 1> [option 2] <arg 2>...

    To quit chat simply type in !exit or !quit

options:
    -n <name>        name of the account to use
    -c <channel>     name of the cahnnel to connect to (including "#" at the beginning)
    -o <oauth>       oauth string (including "oauth:" at the beginning)
    --config <path>  path to configuration file
    --spectate       disable sending messages to the server
    --timestamps     use [h:m:s] timestamps

examples:
    python3 tccli.py -n 'my_bot_account' -c 'my_epic_channel' -o 'oauth:abcdefghijkl...'
    python3 tccli.py --config './conf.cfg'
    python3 tccli.py --config './conf.cfg' -c 'my_epic_channel'
    python3 tccli.py --config './conf.cfg' --spectate

configuration file format:
    name=name_of_user
    channel=name_of_channel
    oauth=oauth:abcdefghijkl
```
