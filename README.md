/etc/logstash/conf.d/logstash.conf


sudo nano /etc/logstash/conf.d/logstash.conf


input {
  beats {
    port => 5044
  }
}

filter {
  if [event][code] == "4625" {
    mutate {
      add_tag => ["failed_login"]
    }
  }
}

output {
  elasticsearch {
    hosts => ["https://localhost:9200"]
    user => "elastic"
    password => "ТВОЙ_ПАРОЛЬ_elastic"
    ssl => true
    ssl_certificate_verification => false
    index => "%{[@metadata][beat]}-%{+YYYY.MM.dd}"
  }

  stdout { codec => rubydebug }
}



sudo -u logstash /usr/share/logstash/bin/logstash --path.settings /etc/logstash -t
