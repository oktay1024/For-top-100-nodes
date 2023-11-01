# For-top-100-nodes
<h1 align=center> If you want to keep your old-eth-mainnet-node use this steps-no gas-needed </h1>


>If your node is down already, follow this steps to make it online back, without paying any gas fee </h1>

#Firstly, be sure that, you back up your "peer-id.json" file (thats located in root/quickstart-archaeologist and old version ".env" (we will use it for some info) 

#Lets clean the old files first and start to set up
```console
cd && rm -rf quickstart-archaeologist

git clone https://github.com/sarcophagus-org/quickstart-archaeologist && cd quickstart-archaeologist

cp .env.sample .env
nano .env 
```
#Now, we have a new version of ".env" file, we will fill it with our old info and there is some new settings in it. we will use etherium mainnet wss connection.Simply, register an infura account from " app.infura.io" no card needed and free for daily 100k request. Then get your wss url from your dashboard.
[infura dashboad](


#Try to fill all lines with your informations like on the photo


![new version .env file](https://github.com/flechemano/For-top-100-nodes/blob/main/Screenshot_20231101-125946.jpg)

#After we fill the ".env" file, correctly ctrl + x and y
#Also,we will use new docker compose command to pull and start to node

```console

COMPOSE_PROFILES=service NETWORK=mainnet docker compose pull
COMPOSE_PROFILES=service NETWORK=mainnet docker compose up -d

