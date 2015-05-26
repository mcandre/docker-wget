# docker-wget - a Docker container for wget

# DOCKER HUB

https://registry.hub.docker.com/u/mcandre/docker-wget/

# EXAMPLES

```
$ make
docker build -t mcandre/docker-wget .
docker run --rm mcandre/docker-wget -O- http://icanhazip.com
40.50.60.70
docker run --rm mcandre/docker-wget -O- http://ron-swanson-quotes.herokuapp.com/quotes && echo ""
{"quote":"Give a man a fish and feed him for a day. Don't teach a man to fish and feed yourself. He's a grown man. And fishing's not that hard."}
```

## Mirroring websites

```
docker run --rm -v $(pwd)/mirrors:/mnt mcandre/docker-wget -P /mnt -mpNHk -D www.gnu.org -np http://www.gnu.org/software/wget/manual/
```

# REQUIREMENTS

* [Docker](https://www.docker.com/)

## Optional

* [make](http://www.gnu.org/software/make/)

## Debian/Ubuntu

```
$ sudo apt-get install docker.io build-essential
```

## RedHat/Fedora/CentOS

```
$ sudo yum install docker-io
```

## non-Linux

* [VirtualBox](https://www.virtualbox.org/)
* [Vagrant](https://www.vagrantup.com/)
* [boot2docker](http://boot2docker.io/)

### Mac OS X

* [Xcode](http://itunes.apple.com/us/app/xcode/id497799835?ls=1&mt=12)
* [Homebrew](http://brew.sh/)
* [brew-cask](http://caskroom.io/)

```
$ brew cask install virtualbox vagrant
$ brew install boot2docker
```

### Windows

* [Chocolatey](https://chocolatey.org/)

```
> chocolatey install docker make
```
