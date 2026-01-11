curl -fsSL https://artifacts.elastic.co/GPG-KEY-elasticsearch \
| sudo gpg --dearmor -o /usr/share/keyrings/elastic-keyring.gpg


ls -l /usr/share/keyrings/elastic-keyring.gpg
