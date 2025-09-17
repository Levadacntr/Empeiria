# Empeiria
screen -Rd empeiria
emped tx distribution withdraw-rewards $(emped keys show empewallet --bech val -a) --chain-id "empe-testnet-2" --from $(emped keys show empewallet -a) --commission --gas auto --gas-adjustment 1.5 --fees 30uempe -y
