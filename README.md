# myled-driver

4セメ課題

---

# 内容

講義で作成したものを編集し作成した。

・0を入力した場合左の赤のLEDだけが点灯する。

・1を入力した場合右の緑のLEDだけが点灯する。

・2を入力した場合左右両方のLEDが点灯する。

・3を入力した場合左右両方のLEDが消灯する。

---

# 環境・道具

## 環境
・Raspberry Pi 4 Model B

・Ubuntu 20.04.1 LTS
## 道具
・ブレッドボード
・LED(赤)
・LED(緑)
・抵抗(1KΩ)x2
・ジャンパー線 オス-オス x2
・ジャンパー線 オス-メス x3

---

# ビルド

## 実行方法
```sh
$ git clone https://github.com/anriku1216/myled-driver.git
$ cd myled-driver/
$ make
$ sudo insmod myled.ko
$ sudo chmod 666 /dev/myled0
```
## 回路
gpio25とGNDの間に緑のLEDと抵抗
gpio24とGNDの間に赤のLEDと抵抗

---

# 実行

## 赤のLEDの点灯

```sh
$ echo 0 > /dev/myled0
```

## 緑のLEDの点灯

```sh
$ echo 1 > /dev/myled0
```

## 両方のLEDの消灯

```sh
$ echo 3 > /dev/myled0
```

## 両方のLEDの点灯

```sh
$ echo 2 > /dev/myled0
```

# 終了

```sh
$ sudo rmmod myled0
$ make clean
```

---

# デモ動画

YouTubeにあげた動画はこちら


---

# 著者

[Rikuto Andou](http://github.com/anriku1216)

ベースのプログラム開発者：[Ryuichi Ueda](http://github.com/ryuichiueda)

---
# ライセンス

[GNU General Public License v3.0](http://github.com/anriku1216/myled-driver/blob/main/COPYING)


















