# リポジトリの概要
<ロボットシステム学　課題１>

第7回、第8回で作成したデバイスドライバーをベースに、オリジナリティーある改造をして、GitHubに置いてください。デバイスドライバーでデバイスを動かしている様子をビデオに撮影してYouTubeに公開してください。第9回の内容も考慮し、リポジトリにはライセンスや著作権の記述もしてください。
# デバイスドライバーの実装内容
第7回、第8回で作成したデバイスドライバーをベースに、4色のLEDを使ってもうすぐやってくる1人寂しいクリスマスを明るく彩ってくれる「世界一しょぼいイルミネーション」を作りました。
# 動作環境
・Raspberry Pi 4 ModelB(8G)  
・Ubuntu 20.04
# 使用したもの
・Raspberry Pi 4 ModelB(8G) ×1  
・ブレッドボード　×1  
・LED 緑　×1  
・LED 赤　×1  
・LED 青　×1  
・LED 黄　×1  
・抵抗　220Ω　×4  
・ジャンパー線　オス-メス　×8
# 回路
LED 緑をGPIO25、LED 赤をGPIO24、LED 青をGPIO23、LED 黄をGPIO18、他方はGNDに接続します。
# インストール方法
1. `$ git clone https://github.com/FujitaRyo/Robosys2020_Task1cd Robosys2020_Task1/myled`
2. `$ make`
3. `$ sudo rmmod myled`
4. `$ sudo insmod myled.ko` 
5. `$ sudo chmod 666 /dev/myled0`
# 使用方法
 `$ echo 0 > /dev/myled0`    LED全て消灯  
 `$ echo 1 > /dev/myled0`    LED全て点灯   
 `$ echo 2 > /dev/myled0`    イルミネーション開始
# デモ動画
https://www.youtube.com/watch?v=ds-Fmy8gWzk
# ライセンス
GNU General Public License v3.0
