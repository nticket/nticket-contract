# Nticket contract

```sh
% yarn build # build only
% yarn deploy # build and deploy on new address on testnet
```


# Contract Methods

1. Add New Event to the collection

```shell
near call dev-1657213279159-36060368407168 nft_create_series '{"creator_id":"iamtester.testnet","token_metadata":{"title":"My First Event #001","description":"Awesome Metalfest","media":"https://g.denik.cz/46/e9/plzen-metalfest-hudebni-festival-amfiteatr-lochotin-21.jpg"},"price":"5"}' --accountId iamtester.testnet --depositYocto 5520000000000000000000
```

2. View first 10 events on contract

```shell
near view dev-1657213279159-36060368407168 nft_get_series '{"from_index":"0","limit":10}'
```