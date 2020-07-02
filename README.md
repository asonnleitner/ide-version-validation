# The script checks IDE version, and keeps settings, logs and cache

Intellij IDEA, WebStorm, DataGrip, PhpStorm, CLion, PyCharm, RubyMine, GoLand and Rider

## Usage
- Close all IDE applications
- For first time only:
```shell script
chmod +x runme.sh
```
- Run script:
```shell script
./runme.sh
```
- Reboot


### Experimental: Version check automatically using launchd agent

- Load job into launchctl:
```shell script
chmod +x runme.sh
./runme.sh --prepare-env
```
- Unload job:
```shell script
launchctl unload ~/Library/LaunchAgents/com.jetbrains.reset.plist 
```

Every first day of each month the job will:
- Close all Intellij applications
- Reset evaluation
- Flush preference cache
