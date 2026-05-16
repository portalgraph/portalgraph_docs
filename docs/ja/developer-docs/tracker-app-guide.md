---
description: Portalgraphのトラッカーアプリを独自実装する際の実装方法について解説します。
---

# トラッカーアプリ構築ガイド

## 概要

PortalgraphアプリケーションはOSC通信でトラッカーアプリから座標を受け取り、それに合わせた映像を表示します。受信プロトコルは[VirtualMotionTrackerのAPI](https://gpsnmeajp.github.io/VirtualMotionTrackerDocument/api/)の部分集合になっています。\
受信ポートは標準で49570番になります。

## API一覧

PortalgraphのOSC通信は以下のAPIをサポートします。

**/VMT/Room/Unity (int)index, (int)enable, (float)timeoffset, (float)x, (float)y, (float)z, (float)qx, (float)qy, (float)qz, (float)qw**\
Unity lik Left-handed space, Quaternion, and Room space. (Recommended)\
Unityと同じ左手系かつ、クォータニオンかつ、ルーム空間(推奨)

**/VMT/Room/UEuler (int)index, (int)enable, (float)timeoffset, (float)x, (float)y, (float)z, (float)rx, (float)ry, (float)rz**\
Unity lik Left-handed space, Euler angles, and Room space.\
Unityと同じ左手系かつ、オイラー角かつ、ルーム空間(推奨)

**/VMT/Input/Button (int)index, (int)buttonIndex, (float)timeoffset, (int)value**\
Button input. ボタン入力\
value(int):1=press, 0=Release

**/VMT/Input/Button/Touch (int)index, (int)buttonIndex, (float)timeoffset, (int)value**\
Button touch input. ボタンのタッチ入力\
value(int):1=press, 0=Release

**/VMT/Input/Trigger (int)index, (int)triggerIndex, (float)timeoffset, (float)value**\
Trigger input. トリガー入力\
value(float):0.0 ～ 1.0

**/VMT/Input/Trigger/Touch (int)index, (int)triggerIndex, (float)timeoffset, (int)value**\
Trigger touch input. トリガータッチ入力\
value(int):1=press, 0=Release

**/VMT/Input/Trigger/Click (int)index, (int)triggerIndex, (float)timeoffset, (int)value**\
Trigger click input. トリガークリック入力\
value(int):1=press, 0=Release

**/VMT/Input/Joystick (int)index, (int)joystickIndex, (float)timeoffset, (float)x, (float)y**\
Joystick input. ジョイスティック入力\
x,y(float):-1.0 ～ 1.0

**/VMT/Input/Joystick/Touch (int)index, (int)joystickIndex, (float)timeoffset, (int)value**\
Joystick touch input. ジョイスティックタッチ入力\
value(int):1=press, 0=Release

**/VMT/Input/Joystick/Click (int)index, (int)joystickIndex, (float)timeoffset, (int)value**\
Joystick click input. ジョイスティッククリック入力\
value(int):1=press, 0=Release<br>

## アプリの登録

作成されたトラッカーアプリは、Portalgraphから自動起動可能です。

<figure><img src="../.gitbook/assets/image (52).png" alt=""><figcaption></figcaption></figure>

F12キーを押して開かれる設定画面左下のトラッカーアプリにアプリのパスを入力すれば、起動時に自動で起動します。

また、\
（WindowsのDocumentsフォルダ）/Portalgraph/portalgraph\_user\_trackers.json\
にアプリを以下のように記述することで左下のドロップダウンにアプリを追加することが可能です。

```
{
  "trackerApps":[
    {
      "name":"Great Tracker",
      "path":"C:/YourGreatTracker.exe"
    }
  ]
}

```
