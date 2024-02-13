# Requirements

## Dojo 0.5.1

```bash
dojoup -v 0.5.1
```

## Scarb 2.3.0

```bash
curl --proto '=https' --tlsv1.2 -sSf https://docs.swmansion.com/scarb/install.sh | sh -s -- -v 2.3.0
```

## Starkli 0.1.20

```bash
starkliup -v 0.1.20
```

# Flow

## Run Katana

```bash
katana --disable-fee --invoke-max-steps 10000000
```

## Export variables

```bash
export STARKNET_RPC="http://localhost:5050/"
export STARKNET_KEYSTORE="keystore.json"
export STARKNET_ACCOUNT="account.json"
```

## Deploy the faucet

```bash
scarb build
starkli declare target/dev/faucet_Token.contract_class.json
starkli deploy 0x02af7d21d3a3b8463e23604639c25668d691c4541270e4f44e351d80463825f3
```