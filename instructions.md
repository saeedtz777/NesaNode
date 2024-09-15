# NesaNode
Start mining $nesa

items needed:
vps (linux,ubuntu).

https://huggingface.co account.

leap/keplr wallet.


prepare your vps and connect to it via ssh (putty app)
in putty run belowe code step by step :



----------------------1------------------------
sudo apt update && sudo apt upgrade -y
 
----------------------2------------------------
sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc
 
echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update
 
----------------------3------------------------
sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
 
----------------------4------------------------
sudo groupadd docker
sudo usermod -aG docker $USER
 
----------------------5------------------------
sudo apt install jq -y 
 
----------------------6------------------------
bash <(curl -s https://raw.githubusercontent.com/nesaorg/bootstrap/master/bootstrap.sh)





after completinhabove steps , you will be redirected to new pages . 

in first page choose: wizard

nexts are your details 

choose monkier name (anything)

write youe email

next is hugging face acceess token "" login to hugging face , go to profile => setting => access token =>> 
create new one => name your access token and give it all the permmission you see there (check all items) => create token =>
you will recive a token , copy that and save => enter that on node setup page .

then it will ask for your leap/keplr wallet private key ,

then referral code (feel free to use mine:  nesa1pcqrv2gnv4cyty64998lqr8lsmrtnf3d5d0vcs )

wait for it to complete and done .

check your node status : https://node.nesa.ai/nodes 
