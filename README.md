# Pythonで書いたメモ帳
文字数制限（～文字以上・～文字以内）のある入力のために，Windouwsのメモ帳に常に文字数が表示されるものを使いたいと考え，
PythonのGUIモジュールwxPythonを使用して作成したスクリプトです．

exeファイルはスクリプトをpyinstallerでexe化したものです．
WindowsやLinuxのWineであれば実行できると思います．
exe化については以下のリンクを参照してください．
<br><a href="https://qiita.com/y-tsutsu/items/f687cf4b57442557aade" target="_blank">PyInstallerがPython3.6をサポートしてくれた</a>
                                                                      
## Windouwsのメモ帳との違い
作成したスクリプトに関して，

* 文字数が表示される（常に更新）ため，文字数制限のある入力の下書きに便利
* タブ表示でき，一つのウィンドウで複数のファイルを切り替えて表示

といった特徴があります．

## 現状の課題
### 2020/05/03
検索など，Windouwsのメモ帳が持つ機能を追加できていないため，方法が見つかれば実装したいと考えています．

また，印刷に関して，使用しているwx.htmlはcssが取り扱えないため，自動で折り返しての印刷ができず，
一行の文字数をカウントすることで強引に改行文字を入れて折り返しているように印刷データを作成しています．
そのため，上手く折り返されずに印刷の枠から切れてしまったり，可笑しな位置での改行があるかもしれません．
できるだけそのようなことがないように調整しましたが，印刷機能に関して完全とは言えません．
wx.html2はcssが使用できるようですが，wx.htmlのような使い方ができず，wx.html2の中でもSetPageメソッドはcssを読み込めずエラーが出ます．
cssが使用できれば印刷時に自動で折り返せると考えておりますが，現状解決策は見つかっていません．

基本的な機能以外にも，wxPythonのモジュールを用いてcsvやtsvファイルを読み込んでの表の表示やmp3といったオーディオファイルの再生を考えていますが，
wx.mediaによるオーディオファイル再生が中々上手く実装できません．．．
## 参考リンク
<!-- * <a href="" target="_blank"></a> -->
* <a href="https://wxpython.org/Phoenix/docs/html/wx.html.1moduleindex.html" target="_blank">wx.html</a>