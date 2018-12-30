
# ロボットシステム学
## robsys2018 課題１ 16C1015 井村 彩聖
### 課題１　内容
LEDを2つ点灯させ, logを書き込ませる

* 動画: https://www.youtube.com/watch?v=T2O8ubznePI

### 動作方法
* LEDの確認

```
$make 
$sudo insmod myled.ko
$sudo chmod 666 /dev/myled0
$echo r > /dev/myled0		# 赤のLEDを点灯
$echo g > /dev/myled0		# 緑のLEDを点灯
$echo 0 > /dev/myled0		# 全てのLEDを消す
```
* logの確認
```
$tail /var/log/messages
[  415.690529]Merry
[  420.418501]Xmas!!
```
* 削除する
```
$sudo rmmod myled
```
### 参考資料
https://github.com/ryuichiueda/robosys_device_drivers

https://github.com/ryuichiueda/robosys2018/blob/master/06.md

