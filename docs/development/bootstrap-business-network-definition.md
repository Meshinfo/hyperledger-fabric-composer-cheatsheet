# Bootstrapping a Business Network Definition project

Easily bootstrapping projects for Composer is done with Yeoman (`npm install -g yo`). Yeoman knows generators. Generators for Composer are maintained in [a directory of the hyperledger/composer Github repository](https://github.com/hyperledger/composer/tree/master/packages/generator-hyperledger-composer) under `generators/`.

There are [the following generators available](https://github.com/hyperledger/composer/tree/master/packages/generator-hyperledger-composer/generators).

We need `businessnetwork` to create a new Business Network Definition:

```bash
yo hyperledger-composer:businessnetwork
```

It will ask a few questions which you need to answer. The result is a new directory representing a freshly created Business Network Definition. Have fun!
