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

**Add CRAN packages**

sudo add-apt-repository ppa:c2d4u.team/c2d4u4.0+

**RStudio Installation**

*Import public key from keyserver*
gpg --keyserver keyserver.ubuntu.com --recv-keys 3F32EE77E331692F

*Validate build signature*

andrei@t2-xps:~/Downloads$ dpkg-sig --verify rstudio-2021.09.0-351-amd64.deb
Processing rstudio-2021.09.0-351-amd64.deb...
GOODSIG _gpgbuilder FE8564CFF1AB93F1728645193F32EE77E331692F 1632173111
andrei@t2-xps:~/Downloads$ 

sudo gdebi rstudio-2021.09.0-351-amd64.deb 


