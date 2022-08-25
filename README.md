# SW2022
#Elastic 설치
sudo apt-get update
sudo apt-get install openjdk-11-j
java –version
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64 
export PATH=$JAVA_HOME/bin/:$PATH export CLASS_PATH=$JAVA_HOME/lib:$CLASS_PATH
sudo ufw disable
sudo iptables –F
sudo apt-get install iptables-persistent netfilter-persistent
sudo apt install net-tools

sudo iptables -A INPUT -p tcp --dport 9200 -j ACCEPT

netstat –nap
sudo apt-get update
sudo apt install apt-transport-https
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add – sudo sh -c 'echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" > /etc/apt/sources.list.d/elastic-7.x.list'
sudo apt update
sudo apt install elasticsearch
sudo systemctl enable elasticsearch.service
sudo service elasticsearch star
sudo service elasticsearch stop

#Logstash 설치
sudo apt-get update
sudo apt-get install openjdk-11-j
java –version
export JAVA_HOME=/usr/lib/jvm/java-11-openjdk-amd64 
export PATH=$JAVA_HOME/bin/:$PATH export CLASS_PATH=$JAVA_HOME/lib:$CLASS_PATH
sudo apt-get update
sudo apt install apt-transport-https
wget -qO - https://artifacts.elastic.co/GPG-KEY-elasticsearch | sudo apt-key add – sudo sh -c 'echo "deb https://artifacts.elastic.co/packages/7.x/apt stable main" > /etc/apt/sources.list.d/elastic-7.x.list'
sudo apt update
sudo apt install logstash
sudo systemctl enable logstash
sudo service logstash start
sudo service logstash stop

#Kibana설치
sudo apt-get update
sudo apt-get install kibana
sudo systemctl enable kibana 
sudo service kibana start
