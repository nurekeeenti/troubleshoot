sudo rm -f /usr/share/keyrings/elastic-keyring.gpg

curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch \
| sudo gpg --dearmor --yes -o /usr/share/keyrings/elastic-keyring.gpg
