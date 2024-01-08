# NG Namespaces Initialization

Transaction to init Maemalade NG's namespaces and keysets.

All 0 to 19 Kadena chains have been initialized. The repository will be useful only
when new chains will be added to Kadena.


## How to

1 - Decrypt the temporary jey
```sh
gpg -d tmp_key.key.gpg
```

2 - Modify the file create-ns-keys.tkpl

- sender
- gas paying key

3 - Generate transaction
```sh
kda gen -t create-ns-keys.tkpl
kda sign tx.yaml -k tmp_key.key
kda sign tx.yaml ...... (key for GAS)
```

4 - Test and sign the transaction
```sh
kda local tx.json
kda send tx.json
```
