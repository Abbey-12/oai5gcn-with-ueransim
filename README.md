# oai5gcn-with-ueransim

**Deploy  OAI-5GCN in VM1**


cd oai5gcn-with-ueransim

docker-compose -f docker-compose-oai5gcn.yaml up -d

**Install ueransim in VM2 for RAN testing**


sudo apt update 

sudo apt upgrade 

sudo apt install make g++ libsctp-dev lksctp-tools 

iproute2 sudo snap install cmake --classic

git clone https://github.com/aligungr/UERANSIM  
cd UERANSIM 

make

open **UERANSIM/config/open5gs-gnb.yaml** and
edit the  configuration  as **oai5g-gnb.yaml** and **oai5g-ue.yaml** 
