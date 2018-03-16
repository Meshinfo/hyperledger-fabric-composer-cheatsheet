# Setup and use local Fabric environment

## Download

```bash
mkdir ~/fabric-tools && cd ~/fabric-tools # your future place for tools

curl -O https://raw.githubusercontent.com/hyperledger/composer-tools/master/packages/fabric-dev-servers/fabric-dev-servers.zip
unzip fabric-dev-servers.zip
cd ~/fabric-tools
./downloadFabric.sh # pull all required docker containers
```

## Control

Optionally, choose the Fabric version through ENV: `export FABRIC_VERSION=hlfv11` (this chooses Fabric 1.1, `hlfv1` would be 1.0). This ENV will be used in all the scripts in `fabric-tools`.

The first start:

```bash
    cd ~/fabric-tools
    ./startFabric.sh # start environment
    ./createPeerAdminCard.sh # required admin cart
```

Start the Composer playground on [http://localhost:8080/login]. After startup, `PeerAdmin@hlfv1` card should be visible. The last part in the name of the card is the Fabric version. Make sure it matches with your Fabric network. It's controlled through the `FABRIC_VERSION` ENV, too.

```bash
composer-playground
```

Stop all:

```bash
./stopFabric.sh
```

Tear down all state:

```bash
./teardownFabric.sh
```

## Destroy everything

```bash
docker kill $(docker ps -q) # kill all running containers
docker rm $(docker ps -aq) # remove all containers
docker rmi $(docker images dev-* -q) # remove all images of pattern dev-*
```


