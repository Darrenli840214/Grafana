<h2 id="logstashenv">Logstash 環境安裝</h2>

1.  `wget https://artifacts.elastic.co/downloads/logstash/logstash-8.2.3-amd64.deb`

2.  `sudo dpkg -i logstash-8.2.3-amd64.deb`

3.  `sudo systemctl start logstash`

4.  `sudo systemctl status logstash`

5.  `sudo systemctl stop logstash (先關掉之後再用)`