# RotateCropMauiBlazorApp
画像の特定エリアを矩形で指定し、そこを切り抜きするサンプル。 矩形は回転することができる。
[RotateCropWinUI3App](https://github.com/jupitris/RotateCropWinUI3App)の.NET MAUI Blazor版。
Blazor自体がWebViewを使うため、画像や図形の描画に[Maui.Graphics](https://maui.graphics/)は使えず、代わりに[HTML5 Canvas API](https://developer.mozilla.org/ja/docs/Web/API/Canvas_API)をラップした[Excubo.Blazor.Canvas](https://github.com/excubo-ag/Blazor.Canvas)を使っています。

段階的に機能を追加したので、以下の構成に分かれています。

1. Drawing Path
   4点の座標を使ってCanvasに矩形を描画する
2. Drawing Board
   マウスで好きな矩形をCanvasに描画する
3. Crop Image
   表示された画像に対し、マウスで好きな矩形を描画＆角度を決めて切り抜く

# Usage

リポジトリをクローンします。

```
git clone https://github.com/jupitris/RotateCropMauiBlazorApp.git
```

`Crop Image` において、初期表示する矩形がバックバッファからフロントバッファに複写されない事象があります。
あとはスライダーに連動した矩形の動きがいまいちな感じです。その他、きっちり動作検証しているわけではないので、動きのおかしな部分があると思います。
大目に見てください。
