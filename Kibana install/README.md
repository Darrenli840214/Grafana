<h2 id="kibanaenv">Kibana 環境安裝</h2>

1.  `wget https://artifacts.elastic.co/downloads/kibana/kibana-8.2.3-amd64.deb`

2.  `sudo dpkg -i kibana-8.2.3-amd64.deb`

3.  `sudo sh /usr/share/elasticsearch/bin/elasticsearch-certutil ca --pem` 之後按enter

4.  `sudo -s (進入root模式，ctrl+d 可退出)`

5.  `cp /usr/share/elasticsearch/elastic-stack-ca.zip /etc/kibana`

6.  `cd /etc/kibana`

7.  `sudo apt-get install unzip -y`

8.  `unzip elastic-stack-ca.zip`

9.  `cp /etc/elasticsearch/certs/http_ca.crt /etc/kibana/ca`

10.  `chgrp kibana /etc/kibana/ca/*`

11.  `chown kibana /etc/kibana/ca/*`

12.  `/usr/share/elasticsearch/bin/elasticsearch-reset-password -i -u kibana_system (按 y 後，改 kibana 密碼)`

13.  `sudo nano /etc/kibana/kibana.yml (直接將下面程式碼貼在最上層)`

    server.host: "0.0.0.0"
    elasticsearch.username: "kibana_system"
    elasticsearch.password: "自己設定的密碼(步驟12)"
    server.ssl.enabled: true
    server.ssl.certificate: /etc/kibana/ca/ca.crt
    server.ssl.key: /etc/kibana/ca/ca.key
    elasticsearch.hosts: ["https://自己ip:9200"]
    elasticsearch.ssl.certificateAuthorities: [ "/etc/kibana/ca/http_ca.crt" ]
    elasticsearch.ssl.verificationMode: none


14.  `sudo systemctl start kibana`

15.  `sudo systemctl restart kibana (有時無法開啟要重啟 kibana)`

16.  `在瀏覽器中輸入 https://自己ip:5601`

17.  補充：`如是用雲端虛擬機，則需另在去防火牆規則中新增 5601/tcp port (eg. GCP 要去虛擬私有雲網路中的防火牆設定)`