# Install Hyperledger Fabric and Composer pre-requisites

## Fabric

System requirements:

- MacOSX, Unix or Windows 10
- Docker version 17.06.2-ce or greater (check using `docker --version`)
- Docker Compose version 1.14.0 or greater (check using `docker-compose --version`)
- Go programming language installed and version 1.9.x or greater (check using `go version`)
- Node.js version 8.9.x or greater and NPM (check using `node --version`)
- Python version 2.7 or greater (check using `python --version`)
- `$GOPATH` set (check using `echo $GOPATH`)

You might want to add the following to your .bashrc` file:

```bash
export GOPATH=$HOME/go
export PATH=$PATH:$GOPATH/bin
```

Operating system specialities:

- You are using Windows? Take notice of [these additional Windows requirements](http://hyperledger-fabric.readthedocs.io/en/latest/prereqs.html#windows-extras).
- MacOSX: The latest LTS version of Node is recommended. You can use `nvm` for it: `nvm install --lts && nvm use --lts && node --version`

## Additional requirements for using Composer

- Operating Systems: Ubuntu Linux 14.04 / 16.04 LTS (both 64-bit), or Mac OS 10.12
- Git: 2.9.x or higher (check using `git --version`)

You are using Ubuntu? Run the following script to install the pre-requisites, if not yet available.

```bash
curl -O https://hyperledger.github.io/composer/prereqs-ubuntu.sh
chmod u+x prereqs-ubuntu.sh
./prereqs-ubuntu.sh
```

## Note on editors

A recommended editor for developing Fabric & Composer is VSCode. There is a extension that enabled syntax highlighting for the Composer specific concepts.
