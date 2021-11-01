# r_programming

**Update Indices**
sudo apt update -qq

**Install helper packages**
sudo apt install --no-install-recommends software-properties-common dirmngr

**Add signing key**
wget -qO- https://cloud.r-project.org/bin/linux/ubuntu/marutter_pubkey.asc | sudo tee -a /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc

gpg --show-keys /etc/apt/trusted.gpg.d/cran_ubuntu_key.asc 

echo $(lsb_release -cs)

**Add repository**
sudo add-apt-repository "deb https://cloud.r-project.org/bin/linux/ubuntu $(lsb_release -cs)-cran40/"

**Install R and its dependencies**
sudo apt install --no-install-recommends r-base
