# bal-sui

## Obtain gas token

```bash
# Check current account's gas token balances
gas_address=$(sui client gas  |  sed -n '3 p' | cut -d' ' -f2,5)
sui client transfer-sui --amount 1000000 --to 0xa7d262f7599441aef3499d7f6b5b69ef35610259 --sui-coin-object-id $gas_address --gas-budget 1000

# Check desiered account's gas token balances
sui client gas 0xa7d262f7599441aef3499d7f6b5b69ef35610259
```
