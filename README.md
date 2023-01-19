# oai5gcn-with-ueransim

// OAI-5GCN

Deploy 5g core in VM1\
cd oai5gcn-with-ueransim
docker-compose -f docker-compose-oai5gcn.yaml up -d\

//RAN
Install ueransim in VM2\
# install cmake
# UERANSIM does not work with the apt version of cmake, that's why we need to install snap and the snap version of cmake:
sudo apt update 
sudo apt upgrade 
sudo apt install make g++ libsctp-dev lksctp-tools 
iproute2 sudo snap install cmake --classic

# install ueransim
git clone https://github.com/aligungr/UERANSIM
cd UERANSIM
make
open UERANSIM/config/open5gs-gnb.yaml
and edit configuration 
