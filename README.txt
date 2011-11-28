NAME
    jqSkin - Web application UI control library

DESCRIPTION
　jqSkinはウェブブラウザ上にシンセサイザーのパネルのようなGUIを表示するための
　JavaScriptライブラリです。パネル、ノブ、スイッチの3種類のUIコントロールが
　含まれています。jQuery UIの機能を使用しており、インタフェースもjQuery UIに
　準拠しています。

■Panel
　　背景画像表示用のコントロール。機能はほとんどありませんが他のコントロールと
　　同じような書式で表示できるようにするために用意されています。

　　オプションとデフォルト値：
　　　id　　ID
　　　left　横位置(10)
　　　top 　縦位置(10)
　　　image 画像ファイルのURL

　　使用例
　　　　$('<img />').panel({
　　　　　　id: 'panel',
　　　　　　image: 'images/panel.jpg',
　　　　　　left: 20,
　　　　　　top: 20
　　　　}).appendTo('#draw');

■Knob
　　ノブ表示用のコントロール。クリックして縦方向にドラッグするとノブが回転して値が
　　変化します。画像はアニメーションの各フレームを縦に並べた形式で、PNGの透明色
　　（アルファチャンネル）も使用可能です。

　　オプションとデフォルト値：
　　　id　　　ID
　　　left　　横位置(100)
　　　top 　　縦位置(100)
　　　width　 1フレームの横幅(32)
　　　height　1フレームの高さ(32)
　　　flames　アニメーションのフレーム数
　　　min　　 最小値(0)
　　　max　　 最大値(100)
　　　sense　 マウス移動距離に対するノブ回転の感度(250)
　　　value　 値(0)
　　　image　 画像ファイルのURL

　　コールバック：
　　　start　 マウスドラッグ開始
　　　stop　　マウスドラッグ終了
　　　change　マウスドラッグ中の値変化

　　ゲッター／セッター：
　　　.knob("value")　　　値取得
　　　.knob("value", n) 　値設定

　　使用例
　　　　$('<img />').knob({
　　　　　　id: 'knob01', image: 'images/knob.png',
　　　　　　left: 50,
　　　　　　top:  50,
　　　　　　width: 32,
　　　　　　height: 32,
　　　　　　value: 50
　　　　}).appendTo('#draw');

■Switch
　　2種類のステータスを持つスイッチ表示用のコントロール。クリックするたびにステータス
　　が切り替わります。スイッチやボタンのほかLEDの表現にも使用できます。画像は2種類の
　　フレームを縦に並べた形式で、PNGの透明色（アルファチャンネル）も使用可能です。

　　オプションとデフォルト値：
　　　id　　　　 ID
　　　left　　　 横位置(100)
　　　top 　　　 縦位置(100)
　　　width　　　1フレームの横幅(32)
　　　height　　 1フレームの高さ(32)
　　　clickable　クリック可能(true)
　　　value　　　値(0)
　　　image　　　画像ファイルのURL

　　コールバック：
　　　click　 マウスクリック

　　ゲッター／セッター：
　　　.switch("value")　　　値取得
　　　.switch("value", n) 　値設定

　　使用例
　　　　$('<img />').switch({
　　　　　　id: 'sw01', image: 'images/switch.png',
　　　　　　left: 100,
　　　　　　top:  50,
　　　　　　width: 32,
　　　　　　height: 32,
　　　　　　value: 1
　　　　}).appendTo('#draw');


REQUIREMENT
　jQueryおよびjQuery UI(core, mouse, widget)を使用しています。
　これらのライブラリも必ず指定してください。

HISTORY
    2011/11/29 最初のバージョン

URL
    http://github.com/aike/jqskin


