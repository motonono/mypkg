# mypkg2 カウント
[![test](https://github.com/motonono/mypkg2/actions/workflows/test.yml/badge.svg)](https://github.com/motonono/mypkg2/actions/workflows/test.yml)

talker.pyでカウントした数字をlistener.pyで表示します
talker.pyがパブリッシャを使ってメッセージ(カウントした数字)をトピックを通して送り、
listener.pyがサブスクライバーを使ってメッセージを受け取ります
また、talk_listen.launch.pyを使うことでtalkerとlistenerの両方の機能を一度に使うことができます

## トピックの名前とメッセージの型
   名前: /countup
   型：  16ビット符号付き整数


## 使い方
```
➀　talkerとlistenerを使う場合

パッケージをインストールした後端末を2つ用意する

片方の端末に

$ ros2 run mypkg talker

と入力し、そのあともう片方の端末に

$ ros2 run mypkg listener

と入力するとtalkerでカウントされている数字がlistenerを打った方の端末に表示される

(表示例)

[INFO] [1672591352.264734808] [listener]: Listen: 8
[INFO] [1672591352.752466694] [listener]: Listen: 9
[INFO] [1672591353.253440655] [listener]: Listen: 10
[INFO] [1672591353.753527085] [listener]: Listen: 11
[INFO] [1672591354.253675383] [listener]: Listen: 12


②　talk_listen.launch.pyを使う場合

パッケージをインストールした後

$ ros2 launch mypkg talk_listen.launch.py

と入力するとカウントされている数字が表示される

(表示例)

[INFO] [launch]: All log files can be found below /home/soma/.ros/log/2023-01-02-04-26-14-895653-LAPTOP-HQDBHS8P-4932
[INFO] [launch]: Default logging verbosity is set to INFO
[INFO] [talker-1]: process started with pid [4934]
[INFO] [listener-2]: process started with pid [4936]
[listener-2] [INFO] [1672601175.711184893] [listener]: Listen: 0
[listener-2] [INFO] [1672601176.196026819] [listener]: Listen: 1
[listener-2] [INFO] [1672601176.697546007] [listener]: Listen: 2
[listener-2] [INFO] [1672601177.197213510] [listener]: Listen: 3
[listener-2] [INFO] [1672601177.697309567] [listener]: Listen: 4
[listener-2] [INFO] [1672601178.196519683] [listener]: Listen: 5

```

## ROSのバージョン
   ROS2

## 必要なソフトウェア
   テスト済み: Python 3.7～3.10  

## テスト環境
 Ubuntu 22.04

## ライセンス
このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および使用が許可されています。
Ⓒ 2022 Souma Nomoto
