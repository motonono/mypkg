# mypkg2 カウント
[![test](https://github.com/motonono/mypkg2/actions/workflows/test.yml/badge.svg)](https://github.com/motonono/mypkg2/actions/workflows/test.yml)

talker.pyでカウントした数字をlisner.pyで表示します

## 使い方
```
パッケージをダウンロードした後端末を2つ開く

片方の端末に

$ ros2 run mypkg talker

と入力し、そのあともう片方の端末に

$ ros2 run mypkg listener

と入力するとtalkerでカウントされている数字がlistenerを打った方の端末に表示される

(例)
[INFO] [1672591352.264734808] [listener]: Listen: 8
[INFO] [1672591352.752466694] [listener]: Listen: 9
[INFO] [1672591353.253440655] [listener]: Listen: 10
[INFO] [1672591353.753527085] [listener]: Listen: 11
[INFO] [1672591354.253675383] [listener]: Listen: 12
[INFO] [1672591354.752795790] [listener]: Listen: 13
[INFO] [1672591355.253550405] [listener]: Listen: 14
[INFO] [1672591355.753403867] [listener]: Listen: 15
```

## 必要なソフトウェア


## テスト環境
 Ubuntu 20.04

## ライセンス
このソフトウェアパッケージは、3条項BSDライセンスの下、再配布および使用が許可されています。
Ⓒ 2022 Souma Nomoto
