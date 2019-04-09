Ethereum Network Stats with POA and POW support
===============================================
[![Build Status][travis-image]][travis-url] [![dependency status][dep-image]][dep-url]

This is a visual interface for tracking proof-of-work ("mainnet") and proof-of-authority ("testnet") network status. It uses WebSockets to receive stats from running nodes and output them through an angular interface. It is the front-end implementation for [ethstats-client](https://github.com/goerli/ethstats-client).

## Proof-of-Authority
![Screenshot](src/images/screenshot-poa.png "Screenshot POA")

* Demo: https://kovan-stats.parity.io/
* Demo: https://stats.goerli.net/

#### Prerequisite
* node
* npm

#### Installation
Make sure you have node.js and npm installed.

Clone the repository and install the dependencies:

```bash
git clone https://github.com/goerli/ethstats-server
cd ethstats-server
npm install
sudo npm install -g grunt-cli
```

#### Build
In order to build the static files you have to run grunt tasks which will generate dist directories containing the js and css files, fonts and images.

```bash
grunt poa
```

#### Run
Start a node process and pass the websocket secret to it.

```bash
WS_SECRET="asdf" npm start
```
Find the interface at http://localhost:3000

By default the IP Address of the client nodes is hidden from the frontend. If you want to transmit this information (although it is never used in the frontend), you can add the environment variable ```HIDE_IP=false```

## Proof-of-Work (Legacy)

![Screenshot](src/images/screenshot-pow.png "Screenshot POW")

* Demo: https://ropsten-stats.parity.io/

Same as above, just run the `pow` build task in Grunt.

```bash
grunt pow
WS_SECRET="asdf" npm start
```

:-)

[travis-image]: https://travis-ci.org/goerli/ethstats-server.svg
[travis-url]: https://travis-ci.org/goerli/ethstats-server
[dep-image]: https://david-dm.org/goerli/ethstats-server.svg
[dep-url]: https://david-dm.org/goerli/ethstats-server
