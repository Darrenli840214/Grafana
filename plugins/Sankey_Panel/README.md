# Grafana Plugins - Sankey Panel 

<h2 id="use">用途</h2>

可以製作可視化水流數據，並且水流的寬度將與所選指標成比例，用以快速目測出哪一個

<h2 id="install">安裝方式</h2>

搜尋 Grafana Plugins 中的 Sankey Panel 並點擊 INSTALL 或於終端機中輸入以下指令

```linux
grafana-cli plugins install netsage-sankey-panel
```
<h2 id="example">範例</h2>

![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/Sankey_Panel.png)

<h2 id="do_example">使用方式</h2>
1. 進入編輯儀表板畫面，於右方選擇Sankey Panel後，於Query欄位放入一個可量化的指標，兩個或以上不同的類別，指標可以輸入Lucene語法搜尋，如下圖

![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/sankeystep1.png)

2. Sankey主要調整右方的Sankey Panel欄位
![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/sankeystep2.png)
* Single Link color only ：只顯示一種顏色
* Node color ：種類節點的顏色
* Node width ：節點的寬度
* Node padding ：調整水流的厚度
* Layout iterations：調整水流整體的排列

<h2 id="do_example">實作範例</h2>

![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/test1.png)
![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/test2.png)
![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/test3.png)
![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/test4.png)
![img](https://github.com/Darrenli840214/Grafana/blob/main/plugins/img/test5.png)
