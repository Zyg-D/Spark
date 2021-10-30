```sh
sudo apt update

echo "\nJAVA install"
sudo apt install default-jre -y

echo "\nSPARK"
cd ~/Downloads
echo "\nDownloading"
wget -O tgzed.tgz https://downloads.apache.org/spark/spark-3.2.0/spark-3.2.0-bin-hadoop3.2-scala2.13.tgz
echo "\nUntaring"
tar -xzf tgzed.tgz
mv spark-3.2.0-bin-hadoop3.2-scala2.13 spark ############################# Needs change
echo "\nMove directory"
sudo mv ~/Downloads/spark/ /usr/lib/

echo "\nConfigure spark-env.sh"
cd /usr/lib/spark/conf/
echo "\nCopy the template file"
cp spark-env.sh.template spark-env.sh
# Append manually
nano spark-env.sh
# (without hashtag and space)
# JAVA_HOME=/usr/lib/jvm/default-java
# SPARK_WORKER_MEMORY=1g
# Press: ^x y Enter

echo "\nConfigure .bashrc"
# Append manually
nano ~/.bashrc
# (without hashtag and space)
# export JAVA_HOME=/usr/lib/jvm/default-java
# export PATH=$PATH:$JAVA_HOME/bin
# export SPARK_HOME=/usr/lib/spark
# export PATH=$PATH:$SPARK_HOME/bin
# Press: ^x y Enter
echo "\nLoad the environment variables to the opened session"
source ~/.bashrc

echo "\nRun Scala shell"
$SPARK_HOME/bin/spark-shell
```
