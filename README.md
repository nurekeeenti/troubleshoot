winlogbeat.event_logs:
  - name: Security

output.logstash:
  hosts: ["192.168.56.103:5044"]
