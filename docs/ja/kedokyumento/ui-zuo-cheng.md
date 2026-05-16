# UI作成

PortalgraphでUIを表示する方法を解説します。Portalgraphはワールドの縮尺に関わらず必ず同一サイズで画面に表示され、左右分割や上下分割の3Dで正常に表示され、マウス、タッチ操作での入力に対応するUIを提供します。

PortalgraphでUIを表示する際は、通常のCanvasではなく、利用してるレンダリングパイプラインに合わせて以下のプレハブを使用します。

* Built-in……Assets/Portalgraph/Prefab/ScreenCanvas
* URP……Assets/Portalgraph/Prefab/ScreenCanvasURP
* HDRP……Assets/Portalgraph/Prefab/ScreenCanvasHDRP

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

シーン内に配置されたプレハブのPortalgraphCanvasのScreenにシーンに配置したPortalgraphプレハブのScreens/Screenをセットすることで、その画面にフルサイズでこのUIが表示されます。

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

使用するラベルはTextMesh Proのものを使ってください。このCanvasはワールドスペースのため、手前にオブジェクトがあるとラベルが隠されて見えません。これを防ぐためにラベルのフォントアセットのシェーダーはTextMeshPro/Mobile/Distance Field Overlayにしてください。

<figure><img src="../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

PortalgraphのUIは、マウス操作またはタッチ操作に対応しています。マウス操作の場合、左右分割3Dの場合は画面の左半分、上下分割3Dの場合は画面の上半分がクリック可能になっています。タッチ操作の場合は、3D方式にかかわらず、画面全体がタッチ可能で、見た目通りの場所がクリックされます。

マウス操作とタッチ操作の切り替えは各画面の設定画面で行います。Portalgraphアプリの実行中にF12キーを押して設定画面を開き、「次へ」→「Input」からMouseまたはTouchを選択してください。

<figure><img src="../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
