---
description: Portalgraphプレハブの設定項目を解説します。開発者が編集する必要のない項目は、取り消し線を付けます。
---

# 設定項目

### Portalgraphオブジェクト設定

<figure><img src="../.gitbook/assets/image (57).png" alt=""><figcaption></figcaption></figure>



項目

Saves Screen Center\
チェックされている場合、Portalgraphに対する画面中央点（ScreenCenter）のローカル座標を保存し、次回シーンを開いた際に座標が引き継がれる。

Save Name\
画面中央点の座標の保存名。名称が同一の場合、別シーンでも設定が引き継がれる。

~~Default Screen Center~~\
~~画面中央点。標準ではPortalgraph/ScreenCenterを指し示す。編集不要。~~

~~Default Screen~~\
~~デフォルト画面。標準ではPortalgraph/Screens/Screenを指し示す。2画面以上ある場合はこれをクローンする。編集不要。~~

Auto Screen Height\
0より大きい場合、その高さが画面に収まるように自動で縮小する。デフォルトのスケールで収まる場合はそれ以上には縮小しない。

~~Coordinate System~~\
~~トラッカー座標系。編集不要。~~

Tracker Type\
トラッカー種別。キャリブレーション画面で選択可能なキャリブレーション種別に反映される。\
Both   VIVEトラッカー、カメラ両方\
Tracker   VIVEトラッカー\
Camera   Webカメラ

~~Tracker~~\
~~頭に取り付けるトラッカー。編集不要~~

~~Eyes~~\
~~Coordinate System内での視聴者の両目を指定する。編集不要。~~

Screen Eyes\
マルチスクリーンでマルチプレイヤー対応する際に、スクリーンに特定のEyesを指定する。\
例えば2つのスクリーンを使用し2番目の画面では別のトラッカーを使用する場合、\
・Portalgraph/CoordinateSystem/Trackers/HeadTrackerをコピー\
・Portalgraph/CoordinateSystemのOSCServerのTrackersにコピーしたHeadTrackerを追加\
・ScreenEyesの要素数を2にし、2番目に(コピーしたHeadTracker)/EyeCenterを指定\
とする。

Main Camera\
Portalgraphを表示する画面とPC本体のメイン画面が異なる場合に、メイン画面に表示するCamera。

Pops Up\
もしもチェックされてる場合、スクリーンより手前に映像が浮かび上がる。

~~Screen Center Matches Origin~~\
~~チェックすると毎フレームScreenCenterをOriginに一致させる（手持ち式構成やVRヘッドセットとの空間同期用）。通常はオフのまま、キャリブレーション後の位置に固定する。編集不要~~

Calibration Key Code\
設定画面を開くボタン

~~Calibration Grid~~\
~~キャリブレーション時に表示されるグリッドコンポーネント。編集不要。~~

Config File Base Name\
設定ファイル名。設定ファイルはDocumentsフォルダに保存され、複数アプリで共有される。もしも共有したくない場合はこれを独自名称に変更する。

Uses External Tracker App\
チェックされてる場合、設定画面の外部トラッカーアプリ設定フィールドが可視化される。これがチェックされていて、さらに設定画面で外部トラッカーアプリ使用チェックボックスがチェックされてる場合、起動時に指定されたトラッカーアプリが起動する。

Calibration Start SE\
キャリブレーション開始時に流すSE

Calibration Count Down SE\
キャリブレーションのカウントダウン時に流れるSE。時報。

~~Calibration Canvas Prefab~~\
~~キャリブレーション画面のプレハブ。設定不要。~~

~~Main Screen Canvas Prefab~~\
~~メイン設定画面プレハブ。設定不要~~

### Portalgraphヒエラルキー設定

<figure><img src="../.gitbook/assets/image (63).png" alt=""><figcaption></figcaption></figure>

ScreenCenter\
画面の中心になる座標を表すオブジェクト。カメラを移動させたい場合はこのオブジェクトを移動させる。\
アタッチされているScreenCenterControllerはキーボードによる操作を行うので、不要な場合は非アクティブ化してください。移動・回転キーはInspectorで変更可能です。

Screens/Screen\
各画面ごとの制御を行う。2画面目以降はこのオブジェクトがコピーして使用される。カメラに背景色、ポストエフェクト等を設定する場合は、Cameras以下のCameraオブジェクトに設定する。

Camera\
マルチディスプレイで使用する際に1画面目をPortalgraphの表示に使わない場合、こちらのカメラの画像が１画面目に表示される。

CoordinateSystem\
トラッキング座標系。もしも全体を拡大または縮小したい場合は、こちらのオブジェクトを拡大縮小する。\
アタッチされているTransformScaleControllerコンポーネントがキー入力による拡大縮小を実装しているので、不要な場合は非アクティブ化する。

LeftHand、RightHand\
右手コントローラー、左手コントローラーを表すオブジェクト

OSCServer\
トラッキングソフトからの通信を受信します。標準で49570番ポートで受信しますが、もしも変更したい場合はアタッチされたUOscServerコンポーネントのPortを変更する。<br>
