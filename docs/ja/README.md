# Portalgraphとは

[English documents is here.](https://app.gitbook.com/s/R4jDeJrvuIogaygztZi7/)

Portalgraphは、プロジェクターやPC画面でVR空間を楽しむUnity用ソフトウェア開発環境です。ユーザーの動きに合わせて映像が変化することで、スクリーンの中に本当に空間が存在し、上下左右遠近、自由な位置から3Dでその空間を覗き込む体験ができます。

<figure><img src=".gitbook/assets/IMG_6760_.jpg" alt=""><figcaption><p>Portalgraphの利用例</p></figcaption></figure>

また、一般的なプロジェクタースクリーンだけでなく、机の上に投影したり、複数のディスプレイを張り合わせた箱や天井等にもVR空間を表示することができます。

<figure><img src=".gitbook/assets/IMG_6730_.jpg" alt=""><figcaption><p>机に投影されたPortalgraph</p></figcaption></figure>

<figure><img src=".gitbook/assets/IMG_6869_.jpg" alt=""><figcaption><p>２つの液晶ディスプレイを組み合わせた箱でのPortalgraph</p></figcaption></figure>

開発者はUnityで容易にこのようなデモを構築可能となっています。

### まずはこちらからスタート

Portalgraphを体験したい人向け

{% content-ref url="quick-start/anatanopcwovrnishitemiyou.md" %}
[anatanopcwovrnishitemiyou.md](quick-start/anatanopcwovrnishitemiyou.md)
{% endcontent-ref %}

{% content-ref url="quick-start/3dpurojekutwovrnishitemiyou.md" %}
[3dpurojekutwovrnishitemiyou.md](quick-start/3dpurojekutwovrnishitemiyou.md)
{% endcontent-ref %}

Portalgraphアプリを作ってみたい人向け

{% content-ref url="/broken/pages/MdlNPgidi9qTZbGvNmdV" %}
[Broken link](/broken/pages/MdlNPgidi9qTZbGvNmdV)
{% endcontent-ref %}



Portalgraphはリアルタイムでユーザーの視点を検出し、その視点に合わせた映像を3Dで生成し表示します。\
これにより、スクリーンの中に空間が存在するように見え、覗き込むことができます。\
視点の検出はWebカメラによる顔認識か、VIVEトラッカーを頭部に装着することで行います。\
左右分割、上下分割、アナグリフ、左右2系統出力の3D出力が可能で、3Dプロジェクター、3Dテレビ、アナグリフ等の3D映像装置に対応します。

Porltagraphランタイムは、ユーザーの視点を追跡する、Portalgraphアプリケーション本体から独立したソフトウェアとして実装され、OSC経由でアプリケーションに座標を送信します。現在はWebカメラによるフェイストラッキングとVIVEトラッカーによるトラッキングに対応しています。

<figure><img src=".gitbook/assets/portalgraph概要.png" alt=""><figcaption></figcaption></figure>

トラッキングアプリとPortalgraph本体の通信プロトコルは公開されているので、ご自身で独自のトラッキングアプリを実装することも可能です。
