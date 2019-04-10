# ブートローダについて

このプロジェクトでは```USBaspLoader```をUSBブートローダとして使用しています。
- https://www.obdev.at/products/vusb/usbasploader.html
- Plaid用カスタマイズ済みブートローダ   
https://github.com/hsgw/USBaspLoader/tree/plaid
  - 何も書き込まれていないATMEGA328Pにブートローダを書き込む場合は、フューズビットの書き込みも忘れずに。

## キットを購入された場合、ブートローダはATMEGA328Pに書き込み済みです

## Windows
デバイスドライバのインストールが必要です。   
zadigを使用して```libusbK```を導入して下さい。
- https://zadig.akeo.ie/
- https://ht-deko.com/arduino/usbasp.html

## ブートローダモードへの入り方
1. USBケーブルを差し込みます
2. ```RESET``` スイッチを押したままにする
3. ```BOOT``` スイッチを押したままにする
4. ```RESET``` スイッチを離す
5. ```BOOT```スイッチを離す

ブートローダモードに入れば、PCのデバイスマネージャなどで```usbasp```として認識されます。

## ブートローダがPCから認識されない
- ATMEGA328Pの近くの部品とはんだづけを確認する
  - ATMEGA328Pの向き
  - BOOTスイッチとRESETスイッチのはんだづけ
  - USBコネクタ
  - R1,R2,R3,D49,D50

- 他のケーブル、PC、USBハブを試す
  - USBハブをはずして直接PCに接続する

## avrdudeでのテスト
```usbasp```として認識されたあと、以下のコマンドをターミナルで実行します。
もしQMK Firmwareのセットアップをしていない場合は、[firmware.md](./firmware.md)のセットアップを済ませて下さい。

```
avrdude -c usbasp -p m328p
```

何も問題なければ以下のような表示がされます。

```
$ avrdude -c usbasp -p m328p
avrdude.exe: AVR device initialized and ready to accept instructions
Reading | ################################################## | 100% 0.00s
avrdude.exe: Device signature = 0x1e950f (probably m328p)
avrdude.exe done.  Thank you.
```

## NEXT
[QMK Firmwareのビルドと書き込み](./firmware.md)