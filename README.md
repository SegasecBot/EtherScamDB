# Ethereum Scam Database

*An open-source database to keep track of all the current ethereum scams*

## Usage

If you haven't already, click [here](https://nodejs.org/en/download/) to download Node.JS

- Download the latest release from [here](https://github.com/MrLuit/EtherScamDB/archive/master.zip).
- Go ahead and open a command line in the release folder
- Install all necessary packages by running ```npm install```
- Build and serve the project using `node run.js`

Generating should take around 2 minutes the first time or after a clean, but when `cache.json` is already present it should launch instantly.

## Flags

- `--clean` Clean up all the old files and folders
- `--update` Manually update all content

## Contribute

Fork this project and edit `_data/data.yaml`. Every item can have the following properties:

- **id**: A unique incremental integer
- **name**: The title of the scam, should probably not be longer than 64 characters
- **status**: The status of a scam. If `status` isn't provided and `url` is, status will be autogenerated with the `--update` flag  **(Optional)**
- **description**: A full description for the scam **(Optional)**
- **url**: The protocol + hostname for a scam website, without a trailing `/` **(Optional)**
- **category**: The category under which the item falls **(Optional)**
- **addresses**: An array of all ethereum addresses that were involved in this scam, with leading '0x'  **(Optional)**

## API

To make use of our database, the following API can be used:

- [api/scams](https://etherscamdb.info/api/scams/)
- [api/addresses](https://etherscamdb.info/api/addresses/)
- [api/ips](https://etherscamdb.info/api/ips/)
- [api/verified](https://etherscamdb.info/api/verified/)
- [api/blacklist](https://etherscamdb.info/api/blacklist/)
- [api/whitelist](https://etherscamdb.info/api/whitelist/)
- [api/check/<domain/ip/address>](https://etherscamdb.info/api/check/myetherwallet.com)

## Donate

If you would like to help without contributing on GitHub yourself you can send some ETH or any other ERC20 token to [etherscamdb.eth](https://etherscan.io/address/etherscamdb.eth) :clap: