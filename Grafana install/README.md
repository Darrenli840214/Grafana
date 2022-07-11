<h2 id="grafanaenv">Grafana 環境安裝</h2>

*配備 4 Cpus以上 Linux 版本 Ubuntu 20.04*

1.  `sudo apt-get install -y adduser libfontconfig1`

2.  `wget https://dl.grafana.com/oss/release/grafana_9.0.0_amd64.deb`

3.  `sudo dpkg -i grafana_9.0.0_amd64.deb`

4.  `sudo systemctl enable --now grafana-server`

5.  `systemctl status grafana-server.service (確認有無啟動)`

6. `如是用雲端虛擬機，則需另在去防火牆規則中新增 3000/tcp port (eg. GCP 要去虛擬私有雲網路中的防火牆設定)`

![img](img/GCP_firewall.png)