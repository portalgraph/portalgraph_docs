# あなたのPC画面をVR空間にしてみよう

このページでは、無料配布されているユニティちゃんライブステージ！for Portalgraphを使ってユーザーに既存のPortalgraphアプリで遊ぶ方法を解説します。一般的なPCモニターと、Webカメラによる支店トラッキングと、アナグリフ（赤青）メガネで画面の中にVR空間が現れるような体験ができます。PC画面は最大30インチ以下で、画面から1m以内で見ることを想定しています。

Portalgraphは画面の大きさ、位置とユーザーの視点を元に映像を生成します。そのため、システムに画面サイズとカメラの見え方を把握させるキャリブレーションが必要になるので、その方法を解説します。

<figure><img src="../.gitbook/assets/IMG_7458.JPG" alt=""><figcaption></figcaption></figure>

## 必要なもの

Windows 10以降のPC（GPU搭載、またはIntel Coreシリーズ第10世代以降か同等のCPU）\
Webカメラ\
アナグリフ（赤青）3Dメガネ\
　[https://www.stereoeye.jp/shop/index.html](http://toy-box.shop-pro.jp/?pid=4563970) (推奨)\
　[https://amzn.asia/d/438qF7P](https://amzn.asia/d/438qF7P)

## 使用方法

Portalgraphランタイムがインストールされてない場合は、事前にインストールします。\
[https://portalgraph.booth.pm/items/6256749](https://portalgraph.booth.pm/items/6256749)

次に、ユニティちゃんライブステージ！ for Portalgraphをダウンロードし、解凍し、UnityChan CRS.exeをダブルクリックして実行します。\
[ユニティちゃんライブステージ！ for Portalgraph](https://portalgraph.booth.pm/items/3234733)

<figure><img src="../.gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>

カメラトラッキングアプリが自動で起動するので、カメラを選択して「適用」をクリックし、ユニティちゃんライブステージのウインドウに戻ります。

<figure><img src="../.gitbook/assets/camerapg.png" alt=""><figcaption></figcaption></figure>

#### ※もしもカメラ映像が表示されない場合は

カメラトラッキングアプリとユニティちゃんライブステージを終了し、VC++ランタイムをインストールして起動し直してください。\
[https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170)

#### ※カメラの調整

カメラトラッキングアプリは、標準で一般的なWebカメラの視野角（FOV）に合わせて調整されていて、それを元に顔の座標を取得します。もしも大きく異なるFOVのカメラを使用していて右下に表示される座標が現実とズレている場合は、カメラトラッキングアプリをキャリブレーションをしてください。

「キャリブレーション」をクリックするとカウントダウンが始まるので、カメラ真正面50cmの場所に目が来るように待機すれば自動で数値が設定されます。

<figure><img src="../.gitbook/assets/image (51).png" alt=""><figcaption></figcaption></figure>

### キャリブレーション

Portalgraphは動作するのに画面の大きさと座標が必要なので、キャリブレーションでシステムに入力します。

Portalgraphアプリケーションの初回起動時はカメラトラッキングの設定画面が表示されます（表示されない場合は、F12キーを押して設定画面を表示し「カメラ」タブを選択してください）。画面サイズを入力してください。

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

もし画面の中が歪んで見える場合は、「手動調整」をクリックすると、微調整が可能になります。モニターの中央真正ｋら見て、画面中心から出てる棒が真っ直ぐに見えるようにカーソルキー上下左右で調整して「OK」をクリックしてください。

<figure><img src="../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

「閉じる」をクリックすると画面の中にユニティちゃんが現れるので、アナグリフ（赤青）メガネをかけると自由な角度からユニティちゃんが動いてるのが3Dで見られます。

<figure><img src="../.gitbook/assets/IMG_7458.JPG" alt=""><figcaption></figcaption></figure>

Portalgraphアプリケーションは標準で以下のキー操作が出来ます。

WASDRF…前後左右上下移動（Shiftと同時押しで低速移動）\
QE TG ZC…左右、上下、傾き回転（Ctrlと同時押しで90度回転）\
12…スケール変更\
3…スケールリセット

画面のサイズ、傾きに合わせてちょうどいいカメラ位置、角度、スケールに合わせてください。
