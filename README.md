# oai5gcn-with-ueransim

// OAI-5GCN

Deploy 5g core in VM1\
cd oai5gcn-with-ueransim
docker-compose -f docker-compose-oai5gcn.yaml up -d

//RAN
Install ueransim in VM2

sudo apt update\ 
sudo apt upgrade \
sudo apt install make g++ libsctp-dev lksctp-tools \
iproute2 sudo snap install cmake --classic\

git clone https://github.com/aligungr/UERANSIM  
cd UERANSIM \
make
open UERANSIM/config/open5gs-gnb.yaml
and edit configuration 
