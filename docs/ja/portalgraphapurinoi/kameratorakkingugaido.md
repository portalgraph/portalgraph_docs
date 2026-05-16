---
description: ヘッドトラッキングをWebカメラで行う場合の設定方法を解説します。
---

# カメラトラッキング設定ガイド

Portalgraph設定

Portalgraphで制作されたアプリケーションを実行して設定画面を開き（標準ではF12キーで開く）、トラッカーアプリ自動起動にチェックし、その下のドロップダウンからCameraを選択すると、次回起動時に自動でカメラトラッキングソフトが起動します。

<figure><img src="../.gitbook/assets/image (40).png" alt=""><figcaption></figcaption></figure>

トラッカー位置はEyeCenterを選択し、適用をクリックします。目座標、目回転が全て0なら設定不要です。

<figure><img src="../.gitbook/assets/image (42).png" alt=""><figcaption></figcaption></figure>

「次へ」をクリックしキャリブレーション画面に遷移したら、「カメラ」をクリックします。

<figure><img src="../.gitbook/assets/image (46).png" alt=""><figcaption></figcaption></figure>

もし、PC内蔵の画面のすぐ上のWebカメラを使用し、一般的な16:9のモニターの場合、カメラトラッキング設定画面で画面サイズを入力してOKをクリックします。

<figure><img src="../.gitbook/assets/image (44).png" alt=""><figcaption></figcaption></figure>

もしもそうではない場合、上級モードをチェックして、画面サイズを手動で入力し、カメラの座標と角度を入力してください。XYZは画面に向かってそれぞれ上、右、奥方向が正方向になります。

<figure><img src="../.gitbook/assets/image (48).png" alt=""><figcaption></figcaption></figure>

## カメラトラッキングアプリ設定

カメラトラッキングアプリは、標準的なPC内蔵Webカメラに合わせて設定済みですので、もし本体内蔵カメラを使う場合はカメラを選択して適用をクリックするだけで設定完了です。

<figure><img src="../.gitbook/assets/camerapg.png" alt=""><figcaption></figcaption></figure>

特殊なカメラを使用していたり、より正確なトラッキングをしたい場合、「キャリブレーション」をクリックするとカウントダウンが始まるので、メジャーなどを使って距離を計測し、カメラの真正面50cmのところに目が来るよう顔を置いてください。カウントダウンが完了するとカメラの視野角、焦点距離が調整されます。

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

体験を快適にするための注意点は以下です。\
・CPU負荷を下げるため、カメラ解像度は低めにする（640×360で十分です）\
・高FPS対応のカメラだと反応性が良くなります\
・広視野角のカメラだと広い範囲で動けますが、視野の外側に行くほど歪みが発生します。\
・開発者はこの視野角120度、60fps対応のカメラを使っています。[https://amzn.asia/d/8dBhXX2](https://amzn.asia/d/8dBhXX2)\
・カメラの対応解像度、FPSは、Windowsのカメラアプリの設定の「ビデオの設定」から確認できます。

以上
