```sh
echo "\nJAVA install"
sudo apt install default-jre

echo "\nSCALA"
cd ~/Downloads
echo "\nDownloading"
wget http://www.scala-lang.org/files/archive/scala-2.13.6.deb
echo "\nDepackaging"
sudo dpkg -i scala-2.13.6.deb

echo "\nInstalling pip and python3"
sudo apt install python3-pip

echo "\nInstalling py4j"
sudo pip install py4j

echo "\nSPARK"
cd ~/Downloads
echo "\nDownloading"
wget https://archive.apache.org/dist/spark/spark-3.2.0/spark-3.2.0-bin-hadoop3.2.tgz
echo "\nUntaring"
sudo tar -xzf spark-3.2.0-bin-hadoop3.2.tgz
echo "\nRenaming"
mv spark-3.2.0-bin-hadoop3.2 spark
#----------------------------------------------------------------------

echo "\nAsserting successful installations"
java -version
scala -version
python3 --version
pip --version
# No way to visualize if py4j is installed


# Stopping at the end:
$SHELL
```
