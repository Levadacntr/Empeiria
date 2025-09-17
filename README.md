# Empeiria
screen -Rd empeiria
emped tx distribution withdraw-rewards $(emped keys show empewallet --bech val -a) --chain-id "empe-testnet-2" --from $(emped keys show empewallet -a) --commission --gas auto --gas-adjustment 1.5 --fees 30uempe -y
emped tx staking edit-validator \
  --commission-rate="0.2" \
  --from=wallet \
  --chain-id=empe-testnet-2 \
  --gas=auto --gas-adjustment=1.5 --fees=10uempe \
  -y
sudo journalctl -u emped -fo cat --no-hostname
emped status | jq
sudo systemctl restart emped

