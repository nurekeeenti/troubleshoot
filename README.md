sudo rm -f /usr/share/keyrings/elastic-keyring.gpg

curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch \
| sudo gpg --dearmor --yes -o /usr/share/keyrings/elastic-keyring.gpg



sudo nano /etc/kibana/kibana.yml


sudo /usr/share/elasticsearch/bin/elasticsearch-create-enrollment-token -s kibana

