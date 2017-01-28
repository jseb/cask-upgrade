# cask-upgrade
Upgrades all installed casks which have newer versions available.

## Features
* shows a summary of all outdated casks before upgrading
* dry-run mode to only show outdated but not upgrade (similar to brew update
  without brew upgrade).
* retry mechanism that will attempt upgrade 3 times in case of failure
* warning message on exit that prints out any casks that were not successfully
  re-installed. In case install failed even after the retries, or the script
  was aborted during installation.

## Screenshots
Upgrading casks

![Alt text](https://raw.github.com/jseb/cask-upgrade/screenshots/screenshots/1.png)

## Try it out
By simply pasting this in your terminal:

```
source <(curl https://raw.github.com/jseb/cask-upgrade/master/cask-upgrade)
```
And then typing ```cask-upgrade -h```. I recommend using the ```-d``` switch
for dry run at first, if many large casks are outdated the full upgrade can
take quite some time.

## Installation
Clone the repo (or just download the file), and add this to the end of your
.bash_profile:

```
source path/to/cask-upgrade/cask-upgrade
```
