# 3DプロジェクターをVR空間にしてみよう

このページではPortalgraphでPCに接続された3Dプロジェクター等を使う際の設定方法を解説します。プロジェクターなど大きな画面を使う場合は、VIVEトラッカーを使用します。

Portalgraphは画面の大きさ、座標とユーザーの視点を元に映像を生成します。そのため、システムに画面サイズと座標を把握させるキャリブレーションが必要になるので、その方法を解説します。

#### 必要なもの

Windows 10以降のPC（GPU搭載、または過去5年以内のIntel Coreシリーズ程度のCPU）\
SteamVRのインストール\
Portalgraphランタイムのインストール\
[https://portalgraph.booth.pm/items/6256749](https://portalgraph.booth.pm/items/6256749)\
VIVEトラッカー\
3Dプロジェクターまたは3Dテレビと対応3Dメガネ

### 設定方法

Portalgraphランタイムがインストールされてない場合は、事前にインストールします。\
[https://portalgraph.booth.pm/items/6256749](https://portalgraph.booth.pm/items/6256749)

次に、Portalgraph使用アプリをダウンロードし、解凍し、実行します。\
[https://booth.pm/ja/items/6253714](https://booth.pm/ja/items/6253714)

今回はサンプルとして、ユニティちゃんライブステージ！ for Portalgraphを使用します。ダウンロードし、解凍し、UnityChan CRS.exeをダブルクリックして実行します。\
[ユニティちゃんライブステージ！ for Portalgraph](https://portalgraph.booth.pm/items/3234733)

#### 初回設定

スタートメニューの検索窓に「Tracker Portalgraph」と入力し、VIVEトラッカー用トラッキングアプリを起動します。初回起動時に以下のように設定の修正を促すメッセージが表示されます。VIVEトラッカーは標準でVRヘッドセットとセットで使うように設定されているため、VRヘッドセット無しで使用するための設定の変更が必要になります。「修正する」をクリックした後、画面のメッセージに従って、SteamVRを終了してください。

<figure><img src="../.gitbook/assets/image (23).png" alt=""><figcaption></figcaption></figure>

#### 画面設定

Portalgraphアプリケーションを起動し、実行中にF12キーを押すと設定画面が開きます。「トラッカー/カスタム」タブを選択してください。

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

左上のトラッカー位置は「Forehead（額）」、左中央のトラッカーアプリ自動起動は「VIVE Tracker」を選択してください。

右側のビュー数にPortalgraph画面を表示する画面数を入力し、スクリーンに表示したい画面番号を入力します（１はメインディスプレイ、2以降がサブディスプレイ。実行環境に依存します）。<br>

<figure><img src="../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

**「適用」をクリックすることで値は反映されます。クリックしないと反映されません。使用するスクリーンが変わった場合、アプリケーションの再起動が必要になります。再起動後、再びF12を押してこの画面を開いてください。**

トラッカー位置は、VIVEトラッカーを取り付ける場所を指定します。通常はForehead（額）をおすすめします。トラッカーは赤の矢印がある方向にUSB端子が向くように取り付けてください。

<figure><img src="../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (93).png" alt=""><figcaption></figcaption></figure>

トラッカーアプリ自動起動にチェックが付いているとアプリ起動時に自動でトラッカーアプリが起動します。OpenVRを選択すると、自動でVIVEトラッカー用トラッキングアプリが起動するようになります。

<figure><img src="../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

「次へ」をクリックしてキャリブレーション画面を開きます。

<figure><img src="../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

3Dドロップダウンから、使用する3Dプロジェクター、3Dテレビ等に合った3D方式を選択してください。

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>

* Side-By-Side・・・左右分割3D
* Top-And-Bottom・・・上下分割3D
* Anaglyph・・・赤青3Dメガネ。右のドロップダウンから色の分割方式が選択できます。
* 2D・・3Dを使用しない
* 2 outputs・・・2系統の映像出力に左右の目の映像を分割して出力します。設定中の画面に左目映像、サブ画面ドロップダウンで選んだ画面に右目映像を出力します。

設定後、VIVEトラッカーを使用して画面のキャリブレーションを行います。「トラッカー」をクリックするとトラッカー設定画面が開きます。画面サイズをメートル単位で入力し、キャリブレーションをクリックして、画面中央にトラッカーを合わせてカウントダウンを待つとキャリブレーションされます。

<figure><img src="../.gitbook/assets/image (38).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/IMG_2551.png" alt=""><figcaption></figcaption></figure>

設定画面を閉じて、VIVEトラッカーと3Dメガネを装着して画面を見ると画面の中にVR空間が広がるのが感じられます。

<figure><img src="../.gitbook/assets/IMG_6760_.jpg" alt=""><figcaption></figcaption></figure>
