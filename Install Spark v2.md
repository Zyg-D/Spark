```sh
sudo apt update

echo "\nJAVA install"
sudo apt install default-jre -y

echo "\nSCALA install"
sudo apt-get install scala

echo "\nSPARK"
cd ~/Downloads
echo "\nDownloading"
wget -O tgzed.tgz https://downloads.apache.org/spark/spark-3.4.0/spark-3.4.0-bin-hadoop3.tgz
echo "\nUntaring"
tar -xzf tgzed.tgz
echo "\nMove directory"
sudo mv spark-3.4.0-bin-hadoop3 /usr/local/spark ############################# Needs change

echo "\nConfigure ~/.bashrc"
nano ~/.bashrc
# Append manually (without hashtag and space):
# export PATH=$PATH:/usr/local/spark/bin
# Press: ^x y Enter

echo "\nLoad the environment variables to the opened session"
source ~/.bashrc

echo "\nRun Spark shell"
spark-shell

```
