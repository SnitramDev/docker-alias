# Docker alias and functions

Useful command line alias for [Docker](https://www.docker.io/). This is for my usage. I will not accept PRs which **I** don't need (now it's enough for me). If you want your own alias, you can fork this and add your own. 

1. Go to your home directory: cd ~/ 
2. Add to .zshrc or to .bash_profile

## Docker Toolbox

### Get IP from docker machine
docker-machine ip

### Docker login error
#### Error: error getting credentials - err: exec: "docker-credential-osxkeychain": executable file not found in $PATH, out:
#### Solution:
1. brew install docker-credential-helper
2. docker login -> should work now

### Speed up Docker in MacOS
1. Install docker machine NFS:
brew install docker-machine-nfs (https://github.com/adlogix/docker-machine-nfs)

2. Restart your computer

3. Mount in your docker VM (e.g. default):
docker-machine-nfs default --mount-opts="nolock,vers=3,tcp,fsc,rw,noatime"


### If you receive the "Cannot detected the NFS mount :(" error, then do the following:
1. docker-machine regenerate-certs default
2. docker-machine-nfs default

"default" is the docker machine name.

3. docker-machine-nfs default --mount-opts="nolock,vers=3,tcp,fsc,rw,noatime"

## Reference

- [Useful Docker Bash functions and aliases](http://kartar.net/2014/03/useful-docker-bash-functions-and-aliases)
- [15 QUICK DOCKER TIPS](https://labs.ctl.io/15-quick-docker-tips/)
