# Nticket contract

```sh
% yarn build # build only
% yarn deploy # build and deploy on new address on testnet
```


# Contract Methods

1. Add New Event to the collection

```shell
near call dev-1657213279159-36060368407168 nft_create_series '{"creator_id":"iamtester.testnet","token_metadata":{"title":"My Second Event #002","description":"Awesome Metalfest","media":"https://d49r1np2lhhxv.cloudfront.net/www/photos/SWRBarroselasMetalfest2018_C1.jpg","copies":20},"price":"7"}' --accountId iamtester.testnet --depositYocto 5520000000000000000000
```

2. View first 10 events on contract

```shell
near view dev-1657213279159-36060368407168 nft_get_series '{"from_index":"0","limit":10}'
```

3. Buy NFT
```shell
near call dev-1657213279159-36060368407168 nft_buy '{"token_series_id":"2","receiver_id":"phil03.testnet"}' --accountId phil03.testnet
```