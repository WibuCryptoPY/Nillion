# Nillion
From : https://wibucrypto.pro/ | Telegram @wibuairdrop142


# GUIDE

# Step 1 : Update System
```sudo apt update && sudo apt upgrade -y```

# Step 2 : Install Prerequisites & Docker
```sudo apt install apt-transport-https ca-certificates curl software-properties-common -y && curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add - && sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable" && sudo apt-get install docker-ce docker-ce-cli containerd.io docker-compose-plugin -y```

# Step 3 : Download accuser Image
```docker pull nillion/retailtoken-accuser:v1.0.0```

# Step 4 : Create accuser directory
```mkdir -p nillion/accuser```

# Step 5 : Run the container to initialise accuser & register
```docker run -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:v1.0.0 initialise```

# Step 6 : Setup wallet
Faucet bằng ví Keplr : https://faucet.testnet.nillion.com/
Connect wallet : https://verifier.nillion.com/verifier

# Step 7 : Running the accuser
```docker run -d -v ./nillion/accuser:/var/tmp nillion/retailtoken-accuser:v1.0.0 accuse --rpc-endpoint "http://65.109.222.111:26657" --block-start 5040477```

# Step 7 : Check verifier logs
```# List Available Docker Container
docker ps

# Display logs
docker logs -f <container-id>```
