# iBrew: The Dream Tea!

iKettle, [iKettle 2.0](http://smarter.am/ikettle) and [Smarter Coffee](http://smarter.am/coffee) Interface

## Needed remote access to iKettle 1, to test new code!

To test and finish: 
  * iKettle Emulation (emulates an iKettle with an iKettle 2.0)
  * iKettle Brigde (connect to an iKettle and use it if it was an iKettle 2.0)
  * Figure out to correct responses
  
Such that all features of iBrew are available (if supported) for the original iKettle!

So if you have an original iKettle filled up with water! And some time to spare!

Contact <tristan@monkeycat.nl>!


## Downloads
  * [Windows](https://dl.dropboxusercontent.com/u/12474226/iBrew.exe)
  * [MacOS]  (https://dl.dropboxusercontent.com/u/12474226/iBrew.dmg)
  * [Source] (https://github.com/Tristan79/iBrew/archive/master.zip)

## Hot! News

Now! macOS & windows apps! With nice icon in the taskbar! :-)

__Trigger! You can now push your data or run commands!__
It is now possible to push sensor values and states of the appliances to other smarthome controllers using HTTP or run commands!

__Please post links, information or help on interfacing with smarthome controllers software in the issues! There are too many out there for me to test and write guides for them all!__.
If you are a plugin coder or scripter and you do not have an iKettle or Smarter Coffee, __just simulate one!__

* Simulates iKettle 2.0 ```ibrew simulate```
* Simulates Smarter Coffee machine ```ibrew simulate```


## Introduction
iBrew is an interface to the iKettle 2.0 and Smarter Coffee devices (and has legacy support for the original iKettle, see below). 

_Stand alone, no internet or Smarter app needed!_

It features! 

__For smarthome fans!__
 * Support unlimited iKettle 2.0 or Smarter Coffee appliances! As many as you like!
 * Usage statistics!
 * No tracking!
 * Stand alone or bridge mode!
 * HomeKit Support
 * HTTP push!
 
__iBrew Interfaces & Bridges__
 * Command Line (now with iKettle Legacy support) 
 * Web (almost finished, help appreciated!)
 * JSON REST 
 * [Javascript](https://github.com/Tristan79/iBrew/blob/master/source/resources/ibrew.js) (almost finished :-)
 * [Python 2.7] (https://github.com/Tristan79/iBrew/tree/master/source/smarter) 
 * Message relay (works with Smarter app!)
 
__Connection Guides__
 * __HomeKit__ (using HomeBridge)  
 * [Domoticz](http://www.domoticz.com/) 
 * [Home Assistant](https://home-assistant.io)
 * [OpenHAB](http://www.openhab.org) 
 * [Smartthings](https://www.smartthings.com)
 * Improve your connection with a relay server 
 * Please share your favorite smarthome controller setup!

_No tracking of you or your appliances usage!_
 
__For the Smarthome and Domotics Interface experts!__
 * Kettle and coffee machine simulation (works with Smarter app!)
 * Console for Smarter protocol debugging
 * Monitor
 * Message blocking and patching
 * Smarter protocol description (start web interface for a clickable web version :-)

Tested on iKettle 2.0 v19 and SmarterCoffee v20 & v22. 

<tristan@monkeycat.nl>

Please share any bugs, jokes, problems, discoveries you made! 

### Legacy support of the original iKettle 

It features! 

__For smarthome fans!__
 * Command Line
 * HomeKit support 
 * Relay
 * Simulator

#### Usefull links
Check out [ikettle-brute-forcer](https://github.com/C0smos/ikettle-brute-forcer)
        
### iBrew in the Media
[The iKettle, the Eleven-Hour Struggle to Make a Cup of Tea, and Why It Was All About Data, Analytics and Connecting Things Together](https://medium.com/mark-rittman/the-story-behind-the-ikettle-the-eleven-hour-struggle-to-make-a-cup-of-tea-and-why-it-was-all-769144d12d7#.h62foolse) 


### Old :-) News
I would like to thank Ju4ia for letting me access his coffee machine remotely, and get more Smarter Coffee missing protocol bits, and... that I could test the client code. And all the other people helping track down bugs and supplying new features, whether by e-mail or in the issues, Thanks!

Since the console it nearly done, protocol almost fully mapped out. It is time to focus on the webpage... the framework is working, it auto reconnect, keeps some stats and you can even preform some actions with it.


## Contact
[Bugs or issues](https://github.com/Tristan79/iBrew/issues). 

<tristan@monkeycat.nl>

If you have jokes on coffee, tea, hot chocolade, coffee machines or kettles, please post in the issues!

### Other stuff 

[iSamsungTV](https://github.com/Tristan79/iSamsungTV) the command line interface to Samsung TV series C, D, E, F and Blue Ray Disc Players with Smart Hub feature.

 
## Installing

Other systems than Windows, MacOS or Pi that are running python see download from source section.

### Windows 

  * [Windows]  (https://dl.dropboxusercontent.com/u/12474226/iBrew.exe)

#### From source
First no python is installed by default so head up over to [python](https://www.python.org/downloads/) and install v2.7 (NOT 3)
Secondly you need [make](http://gnuwin32.sourceforge.net/packages/make.htm) and the python [win32 package](https://sourceforge.net/projects/pywin32/files/pywin32/), the [PythonVC] (https://www.microsoft.com/en-us/download/details.aspx?id=44266) and [git](https://git-scm.com/download/win) and your machine should be minial XP SP3.

Go into the source folder and use `make setupwin` to setup, use `make win` to create a package and use `make cleanwin` to clean up

### MacOS
  * [MacOS]  (https://dl.dropboxusercontent.com/u/12474226/iBrew.dmg)

Once you start the app from the MacOS package (drag it to your application folder first) it will auto link iBrew in your terminal.
Open a terminal and run ```ibrew``` and you're all set, good to go!

_it creates a soft symlink to /usr/local/bin/ibrew,... :-)_

#### From source
Make sure either the command line or xcode is installed, just run `make` in the source folder and it will prompt for a download!
Go into the source folder and, use `make setupmac` to setup, use `make mac` to create a package and use `make cleanmac` to clean up

### Linux

See Pi section.

Go into the source folder and, use `make setuplin` to setup, use `make lin` to create a package and use `make cleanlin` to clean up


### Source

You can run iBrew on systems that run python 2.7. Download and unpack the [source](https://github.com/Tristan79/iBrew/archive/master.zip), download it from github using [Github Desktop](https://desktop.github.com) or manually `git clone https://github.com/Tristan79/iBrew.git`. Finish the setup with running `make setup` in the iBrew folder to configure the python packages for bare bones operation. Update to the latest version of iBrew with `git pull`. Run `make` to see all other options possible.

#### Bonjour

Bonjour is not enabled by default, to install it use `make bonjour` or for windows `make bonjourwin`. But you have to have bonjour installed on your system, macOS its out of the box, on most linux system you can install it with (or try equivalent packages for your *nix distro) `apt-get install avahi-daemon avahi-discover libnss-mdns` and on Windows you either install iTunes or download it from [apple](http://developer.apple.com/networking/bonjour/download/)
Also check out [pybonjour](https://code.google.com/archive/p/pybonjour/)

### Raspberry Pi Jessy (light)

Tested on a clean Jessy light image (september 2016). 

#### Install 

SSH to the Pi! And use:

```
cd ~
sudo apt-get install git
sudo apt-get install python-setuptools
sudo easy_install pip
git clone https://github.com/Tristan79/iBrew.git
cd ~/iBrew/source
sudo make setuplin
sudo ln -s ~/iBrew/ibrew /usr/local/bin/ibrew
```

Now you can start ibrew from anywhere :-) Type in your terminal

```
ibrew
```

Or if you want to start the web interface with event triggers type 

```
ibrew events web
```

And surf to your pi on port 2080!

#### Update 

You can update to the latest version of iBrew with

```
cd ~/iBrew
git pull
```

#### Start web server on pi boot

To add the webserver on boot run

```
sudo nano /lib/systemd/system/iBrew.service
```

Copy and paste this text and save with ctrl-x

```
[Unit]
Description=iBrew
After=multi-user.target

[Service]
Type=simple
ExecStart=/usr/bin/python /home/pi/iBrew/ibrew events web
Restart=on-abort

[Install]
WantedBy=multi-user.target
```

Then run the additional commands
```
sudo chmod 644 /lib/systemd/system/iBrew.service
sudo systemctl daemon-reload
sudo systemctl enable iBrew.service
sudo systemctl start iBrew.service
sudo systemctl status iBrew.service
```

#### Troubleshooting

Please post any bug or [issues](https://github.com/Tristan79/iBrew/issues) here on github!
The error handling is still kinda broken... :-) now use dump to see more. Will revert to debug, info, logging (wip)

### Log & config location

#### Log 
 * macOS ```~/Library/Application Support/iBrew/logs```
 * unix  ```~/.iBrew/logs```
 * unix (root) ```/var/log/iBrew/```
 * windows ```~%APPDATA%\iBrew\logs```
 
#### Config
 * macOS ```~/Library/Application Support/iBrew/```
 * unix  ```~/.iBrew/```
 * unix (root) ```/etc/iBrew/```
 * windows ```~%APPDATA%\iBrew\logs```
 

### Unable to connect to iKettle 2.0 or Smarter Coffee appliance

```
MoonTwo:iBrew Tristan$ ./ibrew list
[10.0.0.3:2016-11-13 12:38:24] Found iKettle 2.0 (iBrew certified firmware v19)
[10.0.0.98:2016-11-13 12:38:24] Found Smarter Coffee (iBrew certified firmware v20)
[10.0.0.99:2016-11-13 12:38:24] Found iKettle 2.0 (iBrew certified firmware v19)
```
Some hints
* Did you download, clone or pull iBrew from git to get the latest version with all the bug fixes?

Network trouble
 * Does the Smarter app autodetects it?
 * Is a firewall blocking port 2081 on your computer (or on your router)?
 * Does ```./ibrew list``` work?
 * Make sure that your kettle/coffee machine is on the same network and subnet as your pc and your phone.
 * It could be that your router is blocking utp broadcast messages (some do, so it never auto detects). 
 * Running it on a computer with only a loopback device will result in auto detection be disabled (when using the simulator)

Static IP address
 * Look up the IP address of the appliance in your router (dhpc server)
 * Set up a static IP address in your router (dhpc server) for your appliance

Reset wireless network
 * Reset appliance (iKettle is longer then 10 seconds button hold on base, coffee machine, eeuh I forgot which button but you can use the smarter app to reset your appliance wireless network to direct mode [FIX])
 * If the appliance is reset. Try connect with your wifi of your pc (if it has wifi) to the appliance its wireless network access point iKettle:?? or SmarterCoffee:?? try if iBrew works.
 * Reconnect to your wifi network (and if you are lucky and could connect with iBrew in direct mode, the command is ./ibrew join namewireless password) else use your phone app.



## Usage

### Command Line

See the console section for the commands.
 
```

  iBrew Server
  ________________

  Usage: ibrew (dump) (events) (fahrenheid) server (host:(port) (host:(port))

    dump                   dump message enabled
    events                 enable trigger events (monitor, relay, console)
    fahrenheid             use fahrenheid
    web                    start web interface & rest api
    port                   optional port number, default 2082
    rules                  blocking & patching rules
    host                   host address of the appliance (format: ip4, ip6, fqdn)
    port                   port of appliance, optional, only use if alternative port


  iBrew iKettle Legacy Command Line
  _________________________________

  Usage: ibrew (dump) legacy command (host(:port))

    command                iKettle command, action to take!
    host                   host address of the appliance (format: ip4, ip6, fqdn)
    port                   port of appliance, optional, only use if alternative port


  iBrew iKettle 2.0 & Smater Coffee Command Line
  ______________________________________________

  Usage: ibrew (dump) (events) (legacy [bridge|emulate] (host:(port))) (shout|slow) (coffee|kettle) (fahrenheid) [command] (host(:port))

    bridge                 emulate iKettle 2.0 using legacy iKettle (NOT IMPlEMENTED)
    emulate (host:(port)   emulates legacy iKettle
    coffee                 assumes coffee machine
    command                action to take!
    dump                   dump message enabled
    events                 enable trigger events (monitor, relay, console)
    fahrenheid             PARTLY WORKING use fahrenheid
    host                   host address of the appliance (format: ip4, ip6, fqdn), only use if detection fails
    kettle                 assumes kettle
    port                   port of appliance, optional, only use if detection fails
    shout                  sends commands and quits not waiting for a reply
    slow                   fully inits everything before action

  If you do not supply a host, it will try to connect to the first detected appliance
  Thus if you have more then one appliance supply a host (if its not in direct mode)


```

The following commands are available, note that [] are manditory arguments and () are optional arguments.

```

  Commands
  ________

  iKettle Commands
    heat                   start heating water
    stop                   stop heating water
    65                     select 65°c
    80                     select 80°c
    95                     select 95°c
    100                    select 100°c
    warm                   start keep water warm
    5                      select keep water warm timer is set to 5 minutes
    10                     select keep water warm timer is set to 10 minutes
    20                     select keep water warm timer is set to 20 minutes
    status                 Get status

    protocol               protocol information
    simulate               start kettle simulation
    relay ((ip:)port)      start relay

  iKettle 2.0 & Smarter Coffee Commands
    default                set default settings
    info                   appliance info
    list                   list detected appliances
    reset                  reset appliance to default
    start                  start the appliance
    status (full)          show status
    settings               show user settings
    stop                   stop the appliance

  iKettle 2.0 Commands
    base                   show watersensor base value
    base [base]            store watersensor base value
    boil                   heat till 100°C
    calibrate              calibrates watersensor
    celsius                use celsius °C [console only]
    fahrenheid             use fahrenheid °F [console only]
    formula (temperature (keepwarm))] heat kettle in formula mode
    heat (temperature)(keepwarm))    heat kettle
    kettlecoffee           warms water for coffee 95°C
    milk                   warm  65°C
    settings [temperature] [keepwarm] [formula] [formulatemperature] store kettle user settings
    tea [green,white,oelong,black] warms water for tea 65°C,80°C,90°C,100°C

  Smarter Coffee Commands
    beans                  use beans for coffee
    brew (cups (hotplate (grind (strength)))) brew coffee
    brew default           brew coffee with stored user default settings
    carafe                 returns if carafe is required
    carafe [state]         set carafe is required [true or false]
    cups [number]          set number of cups [1..12]
    descale                descale coffee machine
    filter                 use pregrind beans in filter for coffee
    hotplate off           turn hotplate off
    hotplate on (minutes)  turn hotplate on (time in minutes)
    mode                   return which mode: cup or carafe mode
    mode [mode]            set mode: [cup] or [carafe] mode
    pregrind               use pregrind beans in filter for coffee
    (strength) [strength]  set strength coffee [weak, medium or strong]
    settings [cups] [hotplate] [grind] [strength] store user settings

  Wireless Network Commands
    direct                 enable direct mode access
    join [net] (pass)      connect to wireless network
    rejoin                 rejoins current wireless network [not in direct mode]
    scan                   scan wireless networks

  Smarter Network Commands
    connect (host) (rules&modifiers) connect to appliance
    block [rules]          block messages with groups or ids
    disconnect             disconnect connected appliance
    events                 start trigger events only
    patch [rules]          patch messages
    relay ((ip:)port)      start relay
    relay stop             stop relay
    remote info            info on remote relay
    remote block [rules]   remote block messages with groups or ids
    remote patch [rules]   remote patch
    remote rules (full)    show remote blocking and patching rules
    remote unblock [rules] remote unblock messages groups or ids
    rules (full)           show blocking & patching rules
    stats                  show traffic statistics
    unblock [rules]        unblock messages groups or ids

  Block Rules
    Consists of rules, in: is for outgoing connection to the appliance, out: is for incomming connection from relay client.

    [in:|out:]rule(,[in:|out:]RULE)*

    RULE
      message id
      group name

  Patch Rules
    Patches additional functionality

    [mod:]VAR=VALUE(,[mod:]VAR=VALUE)*

    VAR                VALUE
    temperaturelimit   STATE or [0..100]  kettle can not heat above VALUE degrees
    childprotection    STATE              kettle can not heat above 45 degrees

  Triggers
    trigger add [group] [trigger] [action] add trigger to a group
    trigger delete [group] (trigger) delete trigger or group triggers
    trigger groups         show list of groups
    trigger [group]        show triggers of group
    trigger                show all triggers
    trigger [group] [bool] enabled/disable trigger group
    trigger [group] switch [bool] set group switch type

  Actions can either be a path to a command or url

  Trigger actions examples:
    C:\SCRIPTS\SENSOR.BAT §O §N
    /home/pi/iBrew/scripts/smarthome.sh Temperature §O §N
    http://smarthome.local/?idx=34&value=§N

  Debug Commands
    time [time]            set the appliance time
    firmware               show firmware Wifi
    history                action history
    [hexdata]              send raw data to appliance (e.g. '64 7e')
    dump                   toggle 'dump raw messages'
    monitor                monitor incomming traffic
    simulate               start kettle (or coffee simulation)
    sweep (id)             [developer only] try (all or start with id) unknown command codes

  Help Commands
    examples               show examples of commands
    groups                 show all message groups
    group                  show messages in group
    messages               show all known protocol messages
    message [id]           show protocol message detail of message [id]
    notes                  show developer notes on the appliances
    protocol               show all protocol information available
    switches               show various forms of trigger switch types
    structure              show protocol structure information
    triggers               show triggers

  iBrew Commands
    console (rules) (modifiers) start console [command line only]
    joke                   show joke
    license                show license
    quit                   quit console [console only]


```

Alternativly you can run a console to test out the commands. Start the console with the command `ibrew console 10.0.0.99`. 

#### Examples

```

  Example command line:
    ibrew shout 21 30 05 7e  Send kettle raw heat without waiting for reply
    ibrew weak 10.0.0.1      Set coffee strength to weak
    ibrew strength weak      Set coffee strength to weak but do not toggle filter/beans
    ibrew dump coffee relay out:GOD,in:32 Simulates Smarter Coffee machine
    ibrew dump kettle relay out:GOD,in:14 Simulates iKettle 2.0

  Example console:
    off                      Stop heating/brewing
    messages                 Show all protocol messages
    message 3e               Show protocol message 3a, turn hotplate on
    167E                     Send kettle raw stop
    21 30 05 7e              Send kettle raw heat
    weak                     Set coffee strength to weak
    strength weak            Set coffee strength to weak but do not toggle filter/beans
    cups 3                   Set number of cups to brew
    mode cup                 Set cup mode
    block in:wifi,in:02          Block wifi and [Set appliance time] command to appliance
    brew 4 10 beans strong   Brew 4 cups of strong coffee using the beans keeping the hotplate on for 10 minutes
    join MyWifi p@ssw0rd     Joins MyWifi wireless network using p@ssw0rd as credential
    settings 100 20 On 75    Set default user settings for the kettle to...


```

### Relay

Start a relay server on port 2081, it acts as an man in the middle passing messages between the appliance and
the clients like the Smarter app or another iBrew instances. It can be configured to block and/or modify/patch certain messages. And as there is only one connection needed to the appliances. Good riddense of the annoying beep when the wireless network disconnects due to overload of connections. Also statistics are now possible.


__Advantages__
 * No annoying beep. Only one connection to the appliance needed
 * A lot faster!
 * History and statistics possible!
 * Works with Smarter app!
 * Works with iBrew as client!?
 * Message blocking
 * Message patching

```ibrew relay 10.0.0.99```

#### Advance relay options

```ibrew dump relay in:DEBUG,out:DEBUG 10.0.0.99 127.0.0.1:3081```

Bind relay server to localhost on a different port and uses the firewall to block all debug messages

To change the firewall rules of a relay server already running, use

```ibrew remote unblock in:ADMIN,out:ADMIN 127.0.0.1:3081```

```ibrew remote block in:DEBUG,out:DEBUG 127.0.0.1:3081```

To see the rules use

```ibrew remote rules 127.0.0.1:3081```


### Firewall 

You can block messages either in (from the appliance) or out (from the relay), this can be usefull to disable calibration or other options like wifi and is internally used to speed things up :-)

```ibrew rules 10.0.0.99```

```ibrew unblock in:ADMIN,out:ADMIN 10.0.0.99```

```ibrew block in:DEBUG,out:DEBUG 10.0.0.99```


### Simulation

* Simulates iKettle 2.0 ```ibrew coffee simulate```
* Simulates Smarter Coffee machine ```ibrew kettle simulate```

You can use to dump action to see more info what is going on.

_Note that message blocking is disabled!_



You can add triggers by replacing the host (ip) with the word simulation and start it with the evens system enabled, if you want to try out triggers...

```
ibrew trigger add Domoticz Temperature "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=155&nvalue=0&svalue=§N" simulation
ibrew events kettle simulate
```

### Web (WIP)

This is a build in progress, please contribute!

Start the web interface 

```
ibrew web
```

and surf to:

```
http://ip:port/
```

#### Replacement for the Smarter app

Yeah I know the start and stop icons look terrible... and it is partly functional but you get no visual indicator it worked. Work in progress!

![devices](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/devices.png)

#### Build in JSON Rest API

For bridging smarthome controllers or use it to integrate your appliance in your own website!

![rest](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/api.png)

#### Setup

You can setup your appliance without the Smarter app. Default settings, calibration, descaling or wifi setup... it does it all! No internet required. This means you can use and setup the kettle and the smarter coffee even if smarters servers disappears (chance of no smarter servers in 5 years 97%, I seen it before :-/)

![settings](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/settings.png)

#### Statistics

It keeps stats for you, and you only! It does NOT send them (or anything else) to Smarter like the Smarter app does and definitly not to me...
Keep your appliance usage to yourself, will you!

![stats](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/stats.png)

#### Protocol description is fully interactive!

Cuz my code... :-) 

![protocol](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/protocol.png)


### JSON REST API

You can find information on the iBrew JSON REST API in the Web Interface under:

```
http://ip:port/info/api
```

The default port is 2080

#### Example JSON return

http://localhost:2080/api/10.0.0.99/status

```
{"status": "ready", "sensors": {"base": "On", "temperature": {"raw": {"fahrenheid": 75, "celsius": 24}, "stable": {"fahrenheid": 75, "celsius": 24}}, "waterlevel": {"raw": 2174, "base": 1110, "stable": 2173}}, "appliance": {"model": "iKettle 2.0", "firmware": {"version": 19, "certified": "iBrew certified firmware"}, "mode": "normal", "network": {"connection": {"directmode": false, "host": "10.0.0.99", "connected": true, "port": 2081, "relay": false}, "relay": {"active": false, "bind": "", "port": 2081}}}, "settings": {"default": {"formula": {"use": false, "temperature": {"fahrenheid": 33, "celsius": 1}}, "keepwarm": 5, "temperature": {"fahrenheid": 212, "celsius": 100, "prefered": "celsius"}}}}
```

### JavaScript (WIP)

Work in progress! Help would be nice!

JavaScript for use with iBrew JSON REST API [Javascript iBrew interface](https://github.com/Tristan79/iBrew/blob/master/source/resources/ibrew.js) 
 
### Python

Python 2.7 only!

The [Python Smarter Interface](https://github.com/Tristan79/iBrew/blob/master/source/smarter/) to the iKettle 2.0 and the Smarter Coffee is located in the Smarter folder. Use __pydoc__ or any other python doc app to see the help on [SmarterInterface.py](https://github.com/Tristan79/iBrew/blob/master/source/smarter/SmarterInterface.py) and [SmarterProtocol.py](https://github.com/Tristan79/iBrew/blob/master/smarter/source/SmarterProtocol.py). There are a lot of options and functions you can use!

Yes, code could be a lot better, you rewrite it,... I suggest making classes of blocking, triggers and patches. Classes of the protocol arguments and messages. Arrghh. This is just one big prototype hack! For me it was about testing IT stuff, not the appliance. The appliances made testing stuff more fun! I mean, events trigger system, emulation, simulation of a _Kettle_?! Wiresharking protocols and figure out what it all does. Well for me this is great fun while I am sick.

#### Basic example

```
from smarter.SmarterInterface import *
from smarter.SmarterProtocol import *

appliance = SmarterClient()
appliance.setHost("10.0.0.99")
appliance.connect()
if appliance.isKettle() and not appliance.heaterOn:
    appliance.kettle_heat_default()
appliance.disconnect()

```

### Smarthome controller push

You can pull values and states with the JSON REST api with it also possible to push values and state with the trigger events system.

To add

```
ibrew trigger add Domoticz Temperature "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=155&nvalue=0&svalue=§N" 10.0.0.99

ibrew trigger add Scripts KettleBusy "C:\SCRIPTS\SENSOR.BAT §N" 10.0.0.99

ibrew trigger add Scripts KettleBusy "/home/pi/iBrew/scripts/sensor.sh §O §N" 10.0.0.99
```

where Domoticz is the group (one action per trigger per group) and §N is the new value and §O is the old value.

To see all triggers 

`ibrew triggers`

To see all active triggers

`ibrew trigger`

monitor the trigger event system
 
`ibrew dump events 10.0.0.99`

or use the web server with auto re-connect :-)

`ibrew dump events web`

If you run the webserver as daemon/service add sudo to all your ibrew commands such that the right config file gets updated!

So instead of `ibrew trigger Domoticz state On 10.0.0.99` run `sudo ibrew trigger Domoticz state On 10.0.0.99`


It is possible to set boolean type to various formats (on/off, 1/0, enabled/disabled,...)


`ibrew trigger Domoticz state on`

See  `ibrew states` for an overview


And enable disable entire groups

`ibrew trigger Domoticz off`

See for group overview

`ibrew trigger groups`

Alpha!

## Guides

### [Domoticz](http://www.domoticz.com/)
[iBrew Forum Thread](http://domoticz.com/forum/viewtopic.php?f=56&t=12985)

Lets set up a kettle temperature sensor and a on base sensor!

For this example the base url of domoticz is 

`http://127.0.0.1:8080/`

The IP of the kettle is `10.0.0.99`

Lets start!

Go to `Setup -> Hardware` and create a new dummy hardware called `Smarter`

![hardware](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/hardware.png)

Click on _Create Virtual Sensors_

![sensor](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/sensor.png)

Create a temperature sensor

![temperature](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/temperature.png)

Go to `Setup -> Devices` and look up your new sensor.

![devices](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/devices.png)

Use the _idx_ of the sensor to add a trigger

```
ibrew trigger add Domoticz Temperature "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=149&nvalue=0&svalue=§N" 10.0.0.99
```

Now we also add an on base motion sensor 

![switch](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/switch.png)

Go to `Switches` and look up your new sensor.

![switches](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/switches.png)

Edit it!

![motion](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/motion.png)

Select motion 

![edit](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/edit.png)

Look up the idx in `Setup -> Devices`

Use the _idx_ of the sensor to add a trigger

```
ibrew trigger add Domoticz OnBase "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=99&switchcmd=§N" 10.0.0.99
```

We need to set up the right boolean state, domoticz uses the format _On_ or _Off_

`ibrew trigger Domoticz state On 10.0.0.99`

start any server with the events enables like

`ibrew dump events web`

If you run the webserver as daemon/service add sudo to all your ibrew commands such that the right config file gets updated!

So instead of `ibrew trigger Domoticz state On 10.0.0.99` run `sudo ibrew trigger Domoticz state On 10.0.0.99`

To see it in action!

For more information on [JSON used by domoticz!](https://www.domoticz.com/wiki/Domoticz_API/JSON_URL's)

Next step is creating and filling in buttons actions using either script:// or iBrew JSON Rest API!...

#### User Variables

Adding user variables

![menu](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/menuvariables.png)

![edit](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/editvariable.png)

![vars](https://raw.githubusercontent.com/Tristan79/iBrew/master/source/distro/images/domoticz/variables.png)

####  Domoticz Technical Stuff

[Domoticz JSON API](https://www.domoticz.com/wiki/Domoticz_API/JSON_URL's)

__State based triggers__
 * uservariable _string_ ("On",Off")
 * virtual sensor _switch_ (set to motion)

__Watersensor based triggers__
 * virtual sensor _custom sensor_
 * uservariable _integer_

__Temperature based triggers__
 * virtual sensor _temperature_
 * uservariable _integer_

__Text based triggers__
 * virtual sensor _text_
 * uservariable _string_


#### iKettle 2.0 example 

These are the example commands to add triggers which update Domoticz. Assuming linux and running as a service (else drop the sudo): Use your own sensors idx's & iKettle 2.0 host, Domoticz host, login & password :-)

__Sensors__
```
sudo ibrew trigger add Domoticz TEMPERATURE "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=149&nvalue=0&svalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz WATERSENSOR "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=198&nvalue=0&svalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz KETTLEBUSY "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=199&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz KEEPWARM "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=202&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz KETTLEHEATER "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=201&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz FORMULACOOLING "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=200&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz ONBASE "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=150&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz KETTLESTATUS "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=205&nvalue=0&svalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz KETTLEDEFAULTCHANGED "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=222&switchcmd=§N" 10.0.0.99
sudo ibrew trigger add Domoticz BASECHANGED "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=225&nvalue=0&svalue=§N" 10.0.0.99
```

__User Variables__
```
sudo ibrew trigger add Domoticz BASE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Kettle Base&vtype=0&vvalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz DEFAULTTEMPERATURE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Kettle Default Temperature&vtype=0&vvalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz DEFAULTFORMULATEMPERATURE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Kettle Default Formula Temperature&vtype=0&vvalue=§N" 10.0.0.99
sudo ibrew trigger add Domoticz DEFAULTKEEPWARM "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Kettle Default Keepwarm&vtype=0&vvalue=§N" 10.0.0.99
```

__Boolean State__

Very important step, do not forget!

```
sudo ibrew trigger Domoticz state On 10.0.0.99
```

#### Smarter Coffee Example

These are the example commands to add triggers which update Domoticz. Assuming linux and running as a service (else drop the sudo): Use your own sensors idx's & iKettle 2.0 host, Domoticz host, login & password :-)
 
__Sensors__
```
sudo ibrew trigger add Domoticz CARAFE "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=197&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz READY "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=211&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz WORKING "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=221&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz ENOUGHWATER "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=213&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz CARAFEREQUIRED "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=219&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz COFFEEBUSY "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=196&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz COFFEEHEATER "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=215&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz GRINDER "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=214&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz HOTPLATE "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=218&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz COFFEESTATUS "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=216&nvalue=0&svalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz COFFEEDEFAULTCHANGED "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=223&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz COFFEESETTINGSCHANGED "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=224&switchcmd=§N" 10.0.0.98
sudo ibrew trigger add Domoticz WATERLEVELTEXT "http://127.0.0.1:8080/json.htm?type=command&param=udevice&idx=227&nvalue=0&svalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz MODETEXT "http://127.0.0.1:8080/json.htm?type=command&param=switchlight&idx=209&switchcmd=§N" 10.0.0.98

```

__User Variables__
```
sudo ibrew trigger add Domoticz GRINDTEXT "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Grind Text&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz MODE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Mode&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz CUPS "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Cups&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz STRENGTH "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Strength&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz STRENGTHTEXT "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Strength Text&vtype=2&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz HOTPLATE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Hotplate&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz GRIND "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Grind&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz WATERLEVEL "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Waterlevel&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTCUPS "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Cups&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTSTRENGTH "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Strength&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTSTRENGTHTEXT "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Strength Text&vtype=2&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTGRIND "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Grind&vtype=0&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTGRINDTEXT "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Grind Text&vtype=2&vvalue=§N" 10.0.0.98
sudo ibrew trigger add Domoticz DEFAULTHOTPLATE "http://127.0.0.1:8080/json.htm?type=command&param=updateuservariable&vname=Coffee Default Hotplate&vtype=0&vvalue=§N" 10.0.0.98
```

__Boolean State__

Very important step, do not forget!

```
sudo ibrew trigger Domoticz state On 10.0.0.98
```

### HomeKit ~ [HomeBridge](https://github.com/nfarina/homebridge)

Yes, you can! Connect your iKettle or Smarter Coffee to HomeKit... just follow the following steps!

Alternativly you could use https://github.com/nferro/homebridge-http-json

#### Software

Install the following software to bridge iBrew with HomeKit

 * [Homebridge](https://github.com/nfarina/homebridge)
 * [cmdSwitch2](https://github.com/luisiam/homebridge-cmdswitch2)

#### Setup

Part of config file relevant to iKettle, iKettle 2.0 or Smarter Coffee

Fill in your own device host (either IP address or hostname) and location to iBrew, 

 * If you use an IP address: PLEASE use a static IP address! (assign in your router)
 * If you are the lucky owner of a router that assigns dynamic IP addresses with hostnames attached (usually in the form of device.local or device.lan) you can use that. If you are lucky, else use a static IP.
 * If you only have ONE device: you can use autodetection (and leave out the ip or hostname) but it adds a 2 seconds time penalty.


#### HomeBridge example config iKettle 

```
	"platforms": [{
		"platform": "cmdSwitch2",
		"switches": [{
			"name": "iKettle",
			"on_cmd": "/Users/Tristan/Coding/iBrew/ibrew legacy heat 10.0.0.3",
			"off_cmd": "/Users/Tristan/Coding/iBrew/ibrew legacy stop 10.0.0.3",
			"state_cmd": "/Users/Tristan/Coding/iBrew/ibrew legacy status 10.0.0.3 | grep 'Heating'"
            "manufacturer": "iBrew",
            "model": "iBrew iKettle",
            "serial": "44DE1AD79BC",
            "polling": true,
            "interval": 1,
		}]

```

#### HomeBridge example config iKettle 2.0
  
```
	"platforms": [{
		"platform": "cmdSwitch2",
		"switches": [{
			"name": "iKettle 2.0",
			"on_cmd": "/Users/Tristan/Coding/iBrew/ibrew start 10.0.0.99",
			"off_cmd": "/Users/Tristan/Coding/iBrew/ibrew stop 10.0.0.99",
			"state_cmd": "/Users/Tristan/Coding/iBrew/ibrew status 10.0.0.99 | grep 'busy'",
            "manufacturer": "iBrew",
            "model": "iBrew iKettle 2.0",
            "serial": "44DE2AD79BC",
            "polling": true,
            "interval": 1
		}]
```

#### HomeBridge example config Smarter Coffee

```
	"platforms": [{
		"platform": "cmdSwitch2",
		"switches": [{
			"name": "Smarter Coffee",
			"on_cmd": "/Users/Tristan/Coding/iBrew/ibrew start 10.0.0.98",
			"off_cmd": "/Users/Tristan/Coding/iBrew/ibrew stop 10.0.0.98",
			"state_cmd": "/Users/Tristan/Coding/iBrew/ibrew status 10.0.0.98 | grep 'busy'",
            "manufacturer": "iBrew",
            "model": "iBrew Smarter Coffee",
            "serial": "44DE3AD79BC",
            "polling": true,
            "interval": 1
		}]
```




#### Example HomeBridge config file

If you do not use any other HomeBridge devices, you can use and alter the following 
example config file for iKettle 2.0 and Smarter Coffee. 

```
{
	"bridge": {
		"name": "Homebridge",
		"username": "CC:22:3D:E3:CE:30",
		"port": 51826,
		"pin": "031-45-154"
	},

	"description": "Homebridge",

	"platforms": [{
		"platform": "cmdSwitch2",
		"switches": [{
			"name": "iKettle 2.0",
			"on_cmd": "/Users/Tristan/Coding/iBrew/ibrew start 10.0.0.99",
			"off_cmd": "/Users/Tristan/Coding/iBrew/ibrew stop 10.0.0.99",
			"state_cmd": "/Users/Tristan/Coding/iBrew/ibrew status 10.0.0.99 | grep 'busy'",
            "manufacturer": "iBrew",
            "model": "iKettle 2.0 Intermezzo",
            "serial": "90DE2AD79BC",
            "polling": true,
            "interval": 1
		},
        {
			"name": "Smarter Coffee",
			"on_cmd": "/Users/Tristan/Coding/iBrew/ibrew start 10.0.0.98",
			"off_cmd": "/Users/Tristan/Coding/iBrew/ibrew stop 10.0.0.98",
			"state_cmd": "/Users/Tristan/Coding/iBrew/ibrew status 10.0.0.98 | grep 'busy'",
            "manufacturer": "iBrew",
            "model": "iBrew Smarter Coffee",
            "serial": "42DE3AD79BC",
            "polling": true,
            "interval": 1
		}]

	}]
}
```

### [Home Assistant](https://home-assistant.io)
[iBrew Forum Thread](https://community.home-assistant.io/t/smarter-coffee-ikettle/1870)

configuration.yaml:

```
switch:
  - platform: command_line
    switches:
      my_kettle:
        command_on: "/home/hass/ibrewcontrol.sh start"
        command_off: "/home/hass/ibrewcontrol.sh stop"
        command_state: "/home/hass/ibrewstatus.sh"
        friendly_name: Kettle
```

ibrewcontrol.sh
```
#!/bin/bash
COMMAND=$1
ibrew $COMMAND <your Kettle IP>
```

ibrewstatus.sh

```
#!/bin/bash
CMD='ibrew status <your kettle IP> |grep busy'
if [ -z "$CMD" ];then
        exit 1
else
        exit 0
fi
```

### [OpenHAB](http://www.openhab.org) 
[iBrew Forum Thread](https://community.openhab.org/t/smarter-coffee-machine-control-with-tcp-binding/12831)

### [Smartthings](https://www.smartthings.com) 
[iBrew Forum Thread](https://community.smartthings.com/t/smarter-coffee/22776/11)

## iBrew Mentioned
 * [knx](https://knx-user-forum.de/forum/supportforen/smarthome-py/1019085-logik-trigger-via-seitenaufruf)
 * [reddit](https://www.reddit.com/r/amazonecho/comments/54vpum/echo_with_kettle/)
 * [micasaverde](http://forum.micasaverde.com/index.php?topic=30336.30)

### Other

Have any links, info or help on other Smarthome controller software, please post in the issues!

## Versions
 * PHASE 1: [BRAINSTORMING] v0.0 Bean Grinder Pack 
 * PHASE 2: [PROTOTYPE]     v0.1 White Tealeaf Edition 
 * PHASE 3: [PROTOCOL]      v0.2 Tea Noire Sweet 
 * PHASE 4: [CONSOLE]       v0.3 Kettle Rattle 
 * PHASE 5: [WEB]           v0.4 Brewing on the 7th day 
 *          [CORE]          v0.4.4 Intermezzo!
 * PHASE 6: [PRERELEASE]    v0.5 The conundrum struggle
 * PHASE 7: [FINALCUT]      v1.0 Out of order!
 * PHASE 8: [BUGS]          v1.1 Ant trail!
 
### Upcoming for the last 3 versions  

Protocol
 * PROTOCOL: History message is not finished
 * PROTOCOL: Modifiers/patches!!! 
 * PROCOCOL: Time arguments (have not figured that out)
 * IKETTLE20: Fahrenheid not finished, please to not use.
 * IKETTLE20: Watersensor to something usefull (like the stupid left or right side handle, cuz the kettle weight balance is off, its inaccurate as fuck even in the smarter app :-/)
 * SMARTER COFFEE: Have not looked at single cup... needs a remote coffee machine session ;-)
 * SMARTER COFFEE: Did I accidently switch carafe required bit?
 * SMARTER COFFEE: Cups from the status and cups from the display setting is different 
 * SMARTER COFFEE: Timers protocol
 * SMARTER COFFEE: v0.5 Missing Coffee Smarter codes (working bit only?)
 * SMARTER COFFEE: Descaling data bit? (the smarter app has it...)
 * HELP: Add the missing pieces
 * SIMULATOR: Add carafe removal and water filling
 * SIMULATOR: Fix waterlevel and fix cups?

Interfaces
 * PYTHON: Better error handling
 * PYTHON: Make the print stuff more general
 * PYTHON: Strip zero from ip
 * PYTHON: fix wireless with the same name
 * PYTHON: filter out wrong responses... of know commands??? or atleast acknowledge them, (03 responses)
 * PYTHON: Beverages should be able to override keepwarm time... xCLI/REST
 * WEB: Web interface 
 * WEB: Auto relay when in web mode
 * WEB: API key, login
 * WEB: Settings iBrew (like blocking, patches, other stuff)
 * WEB: All REST api has no error check...
 * JAVASCRIPT: JSON Rest API
 * ME: hugs!

## LICENSE

The author has no contact with or support from Smarter, and is not affiliated in any way with the company that produces the appliances.


Copyright (c) 2016, Tristan Crispijn
All rights reserved.

Redistribution and use in source and binary forms, with or without modification, are permitted provided that the following conditions are met:

1. Redistributions of source code must retain the above copyright notice, this list of conditions and the following disclaimer.

2. Redistributions in binary form must reproduce the above copyright notice, this list of conditions and the following disclaimer in the documentation and/or other materials provided with the distribution.

3. You may not use source, binary forms or derivative work, with or without modification, for commercial purposes. 

4. Written consent of the iBrew creator Tristan Crispijn with original authentic signature on paper.


THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE DISCLAIMED. IN NO EVENT SHALL THE COPYRIGHT HOLDER OR CONTRIBUTORS BE LIABLE FOR ANY DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES (INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES; LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT (INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE. YOU AGREE TO NOT USE THIS SOFTWARE IN ANY WAY. SMARTER EMPLOYEES OR SMARTER AFFILIATED PEOPLE ARE NOT ALLOWED TO USE THIS SOFTWARE OR DERIVATIVE WORK. YOU AGREE THAT THE SOFTWARE CAN MONITOR THE USAGE OF THE SOFTWARE ITSELF AND OR THE APPLIANCES ATTACHED TO THE SOFTWARE, AND SEND IT BACK TO A MONITOR SERVER FOR BETTER SUPPORT. ENJOY!
               
