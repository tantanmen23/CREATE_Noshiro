# CREATE_Noshiro
2015年8月の能代宇宙イベントで打ち上げたCREATEのロケットに搭載したアビオニクス、「われのロガー2」のプログラム及び発注基板データ。

基板にはLPC1114とATtiny2313の二つのマイコンが搭載されている。
搭載したパーツは
- LPC1114FBD48 (メインマイコン)
- ATtiny2313-20MU (サブマイコン)
- MPU9250 (9軸センサー)
- ADXL375 (3軸大加速度センサー)
- MPL3115A2 (気圧センサー)
- BQ25071 (LiFePo充電制御チップ)
- TPS63001DRCTF4 (3.3V DC/DCコンバーター)
- LTC3872 (12V DC/DCコンバーター)
- TWE-strong (ダウンリンク用無線機器)

っていう感じ。結局のところ時間切れでATtiny2313は動かせなかった…

## われのロガー2_ATtiny2313
UARTでGPSを読んで、SPIでデータをLPC1114に渡すプログラム
## われのロガー2_LPC1114
LPC1114がGPS以外のデータ取得・SDカードへの書き込み・パラシュート開放指令を行うプログラム
## 基板
作った基板データ、Elecrowで発注した。