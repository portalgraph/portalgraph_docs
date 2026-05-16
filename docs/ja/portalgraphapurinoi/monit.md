# 外部モニター設定方法

PortalgraphでPCに接続された3Dプロジェクター等を使う際の設定方法を解説します。プロジェクターなど大きな画面を使う場合は、VIVEトラッカーを使用します。

Portalgraphアプリケーションを実行中にF12キーを押すと設定画面が開きます。

<figure><img src="../.gitbook/assets/image (95).png" alt=""><figcaption></figcaption></figure>

右側のビュー数にPortalgraph画面を表示する画面数を入力し、スクリーンに表示したい画面番号を入力します（１はメインディスプレイ、2以降がサブディスプレイ。実行環境に依存します）。

<figure><img src="../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

**「適用」をクリックすることで値は反映されます。クリックしないと反映されません。使用するスクリーンが変わった場合、アプリケーションの再起動が必要になります。**

**オフセット、スケールは通常は編集不要です。表示領域を限定したい場合を除き以下は読み飛ばしてください。**\
もしも画面内の一部だけに表示したい場合に指定します。オフセットは左下を0,0、右上を1,1とし、スケールは0～1になります（Unityのカメラのビューポートと同じです）。

<figure><img src="../.gitbook/assets/image (99).png" alt=""><figcaption></figcaption></figure>

3Dドロップダウンから、使用する3Dプロジェクター等に合った3D方式を選択してください。

<figure><img src="../.gitbook/assets/image (100).png" alt=""><figcaption></figcaption></figure>



* Side-By-Side・・・左右分割3D
* Top-And-Bottom・・・上下分割3D
* Anaglyph・・・赤青3Dメガネ。右のドロップダウンから色の分割方式が選択できます。
* No 3D・・・3Dを使用しない
* 2 outputs・・・2系統の映像出力に左右の目の映像を分割して出力します。設定中の画面に左目映像、サブ画面ドロップダウンで選んだ画面に右目映像を出力します。

設定後、VIVEトラッカーを使用して画面のキャリブレーションを行います。VIVEトラッカー使用前の設定とキャリブレーションは、以下を参考にしてください。\
[VIVE使用トラッカー設定ガイド](https://portalgraphvr.gitbook.io/portalgraphdokyumento/~/revisions/naaasCiU7LCLg5iaMiiI/quick-start/vivetorakkgaido)<br>

