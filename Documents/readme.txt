FOJP Community Fork v1.4.0
━━━━━━━━━━━━━
FOJP2のメンテナンス版です。翻訳作業中に見つけた不具合を勝手ながら修正しました。



必要なプログラムとファイル
━━━━━━━━━━━━━
FOJP Community Forkの動作には以下のファイルが必要になります。

●Visual Studio 2019 用 Microsoft Visual C++ 再頒布可能パッケージ(x86版)
以下のページの「Visual Studio 2015, 2017, 2019, and 2022」から
「x86: vc_redist.x86.exe」をダウンロードし、インストールしてください。(x64版ではないので注意)
自分でインストールした事がなくても、他のプログラムやゲームのインストーラーによって導入済みであれば不要です。
https://support.microsoft.com/ja-jp/help/2977003/the-latest-supported-visual-c-downloads

いつのまにか配布ページが英語になってたので直リンク: https://aka.ms/vs/16/release/vc_redist.x86.exe


●Microsoft Core XML Services (MSXML) 6.0
以下からダウンロードできます。でもXP SP3以降のWindowsであれば最初から入っていると思います。
https://www.microsoft.com/ja-jp/download/details.aspx?id=3988


●FOSEまたはNVSE(xNVSE)
以下のサイトからダウンロードしてください。
FOSE: http://fose.silverlock.org/
NVSE: https://github.com/NVSEx/NVSE/releases


●辞書ファイル
現在のところ、有志の方が作成したバニラ翻訳辞書は以下の物が存在します。MODの翻訳辞書は各自で探すか作ってください。
・Fallout 3用
本体日本語化辞書: https://ux.getuploader.com/fo3dlc_t/download/361
DLC日本語化辞書: https://ux.getuploader.com/fo3dlc_t/download/397
・Fallout: New Vegas用
Fo:NV 日本語翻訳作業所 有志翻訳辞書: https://fonvj.ngnl.org/
FoNV 英語名詞を日本語名詞化: https://ux.getuploader.com/fo3dlc_t/download/405
・Fallout 3 ＆ New Vegas両対応
Fallout一括翻訳セット: https://onedrive.live.com/?cid=CF71A3D695ED6DE5&id=CF71A3D695ED6DE5!3776

有志の方が作られたまとめファイルや一括導入プログラムを使うと楽に導入できます。



インストール手順
━━━━━━━━
基本的にFOJP2と同じです。
導入の際はVortexやMod Organizer 2のようなMOD管理ソフトの利用を勧めます。(直導入でも問題はありません)

1. あらかじめゲームを正しく起動・プレイできるか確認してください。とくにFallout 3。
2. Fallout 3を遊ぶならFOSEを、Fallout New VegasならNVSEを導入する。(手順は省略)
3. Falloutをインストールしたフォルダ(Fallout3.exeかFalloutNV.exeがあるフォルダ)に「fojp.xml」をコピーする。
4. 「_fojp.dll」をFOSE・NVSEのプラグインフォルダへコピーする。
   FOSEのプラグインフォルダは「Fallout 3をインストールしたフォルダ\data\fose\plugins」、
   NVSEのプラグインフォルダは「Fallout NVをインストールしたフォルダ\data\nvse\plugins」となります。
   フォルダが無い場合は自分で作成してください。pluginsとpluginを間違えないよう注意！
5. 「日本語化用データ」フォルダの中身を、Falloutインストールフォルダ内の「data」フォルダへコピーする。
6. 「マイドキュメント\My Games\Fallout 3」フォルダ(もしくは 「マイドキュメント\My Games\Fallout NV」フォルダ)の中にある「fallout.ini」をメモ帳で開き
   [Archive]セクションから「bInvalidateOlderFiles」を探して、数値を0から1へ変更する。ターミナルの翻訳に必要となります。
   fallout.iniが存在しない場合、一度ゲームランチャーを起動してください。
7. fojp.xmlの<replacetext>から</replacetext>の間に使用する辞書の情報を登録する。
   辞書情報は使用する辞書に付属するreadme.txtに書いてあるはずなので、そこからコピペしてください。

以上で完了です。
ゲームを起動する時はfose_loader.exeかnvse_loader.exeから起動してください。



バージョンアップ方法
━━━━━━━━━━
FOJPのDLLを上書きし、設定を付属のfojp.xmlへ移してください。



他のMODとの競合について
━━━━━━━━━━━━
・「Data\Menus」内のXMLファイルを上書きされると、ターミナルとキャラクタークリエイション画面が翻訳できなくなります。
　VUI+やDarnUIなど、該当するMODと同時に使う場合はそれらのMODをFOJPのファイルで上書きしてください。
　VortexやMod Organizer 2ならFOJP関係のファイルを上記MODより下に配置してください。
・「Data\Texture\Fonts」内のファイルは上書きされても構いません。



その他
━━━
・FOJPを使うことによるセーブデータへの影響は一切ありません。好きなタイミングで導入と削除ができます。
・Unicodeには対応していません。なのでPCの言語設定次第で文字化けしたりと挙動が変わります。
・もし問題や改善点を見つけたらスレやTwitter等で報告していただけるととても助かります。
　特にnvac.logにFOJPのDLL名が載っていた場合はログの該当する行とfojp.logのBase Addressを報告してもらえるとありがたいです。
・よかったら「Fallout 3/NV バニラ翻訳補完辞書」も使ってみてください。
　バニラ辞書で翻訳できないシステムメッセージやスタッフロールなどを翻訳します。
　Fallout 3/NV バニラ翻訳補完辞書: https://ux.getuploader.com/FO3/download/640



日本語化に関するTIPS
━━━━━━━━━━
●推奨MOD
日本語化とは関係ありませんが、安定動作のために以下のMODの導入を推奨します。
導入方法はちょっと長くなってしまうので、お手数ですが各自で調べてください。
・Fallout 3
4GB Patch: https://ntcore.com/?page_id=371
NVAC(NV用のMODですがFO3でも使用可能です): https://www.nexusmods.com/newvegas/mods/53635
・Fallout: New Vegas
FNV 4GB Patcher: http://www.nexusmods.com/newvegas/mods/62552
NVAC: https://www.nexusmods.com/newvegas/mods/53635

バグ修正MODのUUF3PとYUPもお勧めですが、テキストの修正を含んでいるので対応する辞書を導入しないと一部が翻訳できなくなります。
またバグ修正MODは削除やアップデートをすると不具合が出やすいので取り扱いには注意が必要です。

Windows 10を使っている人は絶対にFOSRとNVSRを導入しないでください。


●推奨インターフェイスMOD
バニラのUIは表示範囲が狭く、コンテナメニュー画面のコンテナ名などを正しく翻訳できない事があるのでVanilla UI Plusの導入をおすすめします。
インストールの際は「No Font Tweak」オプションを選択する必要があります。
Vanilla UI Plus: https://www.moddb.com/mods/vanilla-ui-plus

もしDarNified UIを導入する場合、DarNified UI Font Dummiesは導入しないでください。一部のフォント設定がバニラの物になってしまい、レイアウトが少し崩れます。
またDarNified UIは画面左上通知メッセージのの表示範囲が狭いため、一部正しく翻訳できない場合があります。


●プレイヤー名を翻訳する
プレイヤー名とその翻訳を辞書に登録するか、あるいはfojp.xmlの描画テキストフィルター設定に登録すれば、セリフやメモ内に現れるプレイヤー名も翻訳できます。


●NPCの台詞を翻訳する
ゲーム内設定で「その他の字幕」を有効にしてください。


●NPCが遠すぎて台詞の字幕が表示されない問題の対処法
lStewieAl's TweaksというMODを導入するとNPCの台詞が表示される距離を調整できます。
バニラの表示距離設定ではジェイソン・ブライトの演説を翻訳できないので、気になる方は導入してみてください。
設定ファイルのbCustomSubtitleDistanceを1にすると機能が有効になり、fSubtitleDistanceの数値で表示距離を変更します。
ジェイソンの演説を表示するには1000くらい必要です。(バニラは500)
lStewieAl's Tweaks(NV用): https://www.nexusmods.com/newvegas/mods/66347

残念ながら、この機能は今のところFallout3版のlStewieAl's Tweaksには搭載されていないようです。


●セリフ送りが速すぎて読み切れない場合の対処法
F4キーでコンソール画面を開く事で会話を一時停止できます。
またNew Vegas であればlStewieAl's TweaksのbNoAutoContinueDialogを有効にする事で、画面をクリックするまでセリフが進まなくなります。


●ラジオを翻訳する
ラジオに連動して字幕を表示するMODを併用する事で、FOJPによる翻訳ができるようになります。
ただし以下のMODはバニラのラジオしか対応していません。
またDarNified UIを導入するとメッセージ領域が狭くなり翻訳できない場合があります。
・Fallout 3
Radio Subtitles for Fallout 3 GOTY: https://www.nexusmods.com/fallout3/mods/23939
・Fallout: New Vegas
New Vegas韓国語化パッチ: https://blog.naver.com/zhekuen
右上の(1)と書かれている場所からFallout+New+Vegas.7zをダウンロードし、
そこからRadio_KOR.espを取り出してください。日本語環境で他のファイルを導入すると表示が崩れるので注意。


●ムービーを翻訳する
FOJPでは翻訳できないのでbikmodを併用してください。
Fo3-and-FoNV-イントロED字幕+bikmodv0.3e.zip: https://ux.getuploader.com/fo3dlc_t/download/427


●You're SPECIAL!やVit-o-matic Vigor Testerを翻訳する
ゲームシステムの説明を含む重要なテキストですが、これらは文字データではなくテクスチャなのでFOJPでは翻訳できません。
日本語テクスチャに差し替えるMODが有志の手で作られているので、そちらを併用してください。
-You're SPECIAL!日本語化
https://ux.getuploader.com/fo3dlc_t/download/349
-Vitomatic日本語化
https://ux.getuploader.com/fo3dlc_t/download/347
https://ux.getuploader.com/fo3dlc_t/download/348


●ハッキング画面のフォントを変更する
fallout.iniの「sFontFile_5」を好みのfntに変更し、さらにfojp.xmlの翻訳対象外フォントに追加してください。
ハッキング画面用のフォントは他と同時に使わないよう注意。翻訳できなくなります。


●日本語以外のPCで日本語化する(Translate to Japanese on a non-Japanese computer)
FOJPはUnicodeに対応していないので、日本語以外のPCで使用するにはLocale Emulatorを使い、言語設定を日本語にする必要があります。
また、英語版以外のFalloutには対応していません。

FOJP does not support Unicode, so if you want to use this on a non-Japanese computer, you need to change the language setting to Japanese using "Locale Emulator".
Also, FOJP is not compatible with non-English version Fallout.

Locale Emulator: https://pooi.moe/Locale-Emulator/


●日本語以外に翻訳する
fojp.xmlの<config id="CharacterSet" value="128"/>の数値を変更してください。
そして辞書を登録し、Locale Emulatorを使って目的の言語で起動すれば翻訳できます。

CharacterSetの値は以下のサイトを参照。
https://docs.microsoft.com/en-us/previous-versions/windows/desktop/bb322881(v=vs.85)


●メモリ削減機能を持つMODとの競合について
ENBやNVTFにはメモリ消費を削減して高負荷MOD使用時のCTDを劇的に減らす機能がありますが、残念ながらこれらはFOJPと競合してしまいます。
現在は競合回避のためFOJPに同等の機能を搭載しています。
また、下記のd3d9.dllモードを利用することでも使用できるようになります。


●FOJPと競合してしまうMODと同時に使う方法
FOJPは以下のMOD(の一部機能)との競合が確認されています。
-ENBのReduceSystemMemoryUsage設定 (いわゆるENBoost)
-NVTFのbModifyDirectXBehavior設定とその関連設定
これらとの競合を回避するには、d3d9.dllとして擬態するFOJPCFの機能を利用する必要があります。
※やっつけで作った機能なので互換性は保証しません！うまく動かない場合はたぶんFOJPが原因です！
※メモリ削減だけが目的であればd3d9.dllモードを使う必要はありません。FOSE/NVSEモードでApplyMemoryPatchを有効にすれば同じ効果があります。

・d3d9.dllモードの使用方法
1. 「_fojp.dll」の名前を「d3d9.dll」に変更する。
2. 「d3d9.dll」をFallout.exe/FalloutNV.exeと同じフォルダへ配置する。
5. FOSE/NVSEプラグインフォルダにFOJPが入っているなら削除する。

・d3d9.dllモードでENB・SweetFX・SMAA Injector・DXVKと併用する方法
1. 上記「・d3d9.dllモードの使用方法」を実行する。
2. ENBなどに付属する「d3d9.dll」の名前を変える。(例えばd3d9_enb.dllとか)
3. fojp.xmlを開き、「ProxyLibraryPath」のvalueにENBのDLL名を記入する。
4. fojp.xmlの「LoadDLLAsD3D9」の値を1にする。

・d3d9.dllモードでReShadeと併用する方法
1. 上記「・d3d9.dllモードの使用方法」を実行する。
2. ReShadeのDLLの名前を変える。(例えばd3d9_reshade.dllとか)。
3. fojp.xmlを開き、「ProxyLibraryPath」のvalueにReShadeのDLL名を記入する。
4. fojp.xmlの「LoadDLLAsD3D9」の値を0にする。（ここ間違えないよう注意！1だと起動しません）


●その他細かいこと
-F4キー(初期設定)でコンソールを表示できます。
-F11キー(初期設定)で原文と翻訳文を切り替えられます。
-F12キー(初期設定)で表示されているテキストをログに出力できます。



トラブルの対処法
━━━━━━━━
うまく動作しない時はfojp.logファイルも読んでください。いくつかの問題は何らかの警告が表示されます。

●起動しない
-「●必要なプログラムとファイル」に書かれたファイルをインストールしてください。
-FOSE/NVSEモードのFOJP、d3d9.dllモードのFOJP、そしてENBを同時に使うと起動しません。FOJPは複数同時に導入しないでください。


●全く翻訳できず原文のままになってしまう
-FOJPは英語版のFalloutにしか対応していません。
-F11キーを押してもフォントが切り替わらない場合、FOJPが有効になっていません。正しく導入できているか確認してください。
-F11キーを押すとフォントが切り替わる場合は導入か設定が間違っていると思われます。fojp.logを確認してみてください。
-fojp.logに「辞書を読み込めなかった」と表示される場合、辞書を登録できていません。
-fojp.logに「fntファイルを読み込めなかった」と表示される場合、同梱の日本語化用データをdataフォルダへ入れてください。
 独自のフォントを使っていて、それがbsaに封入されている場合はBSA Browserなどで取り出してください。
-DLL形式のMODが干渉して動作しなくなる場合があります。一つずつ外して確認してください。
-NVSEプラグインモードでNVTFのbModifyDirectXBehaviorを使うと翻訳できなくなります。d3d9.dllモードか内蔵のメモリ機能で代用してください。
 「The Frontier」にはbModifyDirectXBehaviorが有効になっているNVTFが同梱されているので注意。


●一部のテキストだけ翻訳できない
-使用している辞書がそのテキストに対応しているか確認してください。butterfly search等のテキスト検索ソフトを使うと楽です。またF12キー(初期設定)でログ出力すると翻訳の成否を確認できます。
-pip-boy内など、狭い領域に表示されるテキストはハイフネーションされてテキストが変化する場合があります。
-FOJPは文字テクスチャのUV座標を元に文字を解析しています。
 なので万が一、UV座標が完全に一致する文字がいくつも存在するとFOJPがテキストを正しく認識できなくなります。その場合はfojp.logに警告が表示されるので確認してください。


●ターミナル画面とキャラクタークリエイション画面が翻訳できない
-これらの画面は翻訳対象外に指定されたフォントを使用しているので、バニラのままだと翻訳できません。
 翻訳するには同梱の日本語化用ファイルを導入してください。
-日本語化用メニューファイルが他のMODで上書きされると翻訳できなくなります。インストール順に気を付けてください。
-fallout.ini内の「bInvalidateOlderFiles」が1になっているか確認してください。


●長文のターミナルだけ翻訳できない
computer_menu.xmlファイルが古いものと思われます。同梱の日本語化用ファイルを使用してください。


●ハッキング画面と、ロケーション発見時に浮かび上がる地名と、クエスト開始時・終了時に浮かび上がるクエスト名が翻訳できない
これらは現状だと翻訳できない上に表示が崩れるので、翻訳対象外フォントに指定することで翻訳処理を回避しています。


●翻訳文が文字化けする
以下を確認してください。
-辞書ファイルの文字エンコードは「ANSI」(日本語環境だとShift_JIS)のみの対応です。エンコーディングを確認してください。
-Windowsの「Unicode 対応ではないプログラムの言語」設定が日本語になっているか確認してください。以下はWindows 10における確認法です。
 1. Windowsの設定から「時刻と言語」→「言語」→「管理用の言語の設定」と開く。
 2. 「Unicode 対応ではないプログラムの言語」から「システム ロケールの変更」を開き、現在のシステムロケールを「日本語(日本)」に設定してOKを押す。
 3. PCを再起動する。
 4. 理由があって日本語以外に設定していた場合はプレイ後に元に戻してください。
-Locale Emulatorを使用している場合はLocale Emulatorの言語設定を翻訳する言語に合わせてください。


●翻訳辞書を作ったけれど一部のテキストが翻訳できない
ゲーム中にF12キー(初期設定)を押すと、画面に表示されているテキストが全てfojp.logに記録されます。
このテキストはFOJP内部の形式なので、そのまま英語辞書に登録すれば翻訳できるはずです。
ただし、正規表現の影響を受けるテキストはそのまま登録しても使用できません。

fojp.xmlから「AlwaysLoggingText」の設定を有効にすると、翻訳エンジンに渡されたテキストが全てfojp.logへ出力されます。
こちらは正規表現による整形を施した状態でテキストを出力するのでそのまま辞書に使用できます。


●d3d9.dllモードで動かない
以下を確認してください。
-DLLの名前は「d3d9.dll」にしてください。
-fojp.logに「d3d9.dllモードでフックします」と記述されているか確認してください。
-「d3d9.dll」はFallout 3もしくはFallout: New Vegasのインストールフォルダへ配置してください。FOSE/NVSEプラグインのフォルダに置くとFOSE/NVSEプラグインモードとして稼働します。


●d3d9.dllモードでENBと同時に使えない
-fojp.xmlのProxyLibraryPathに記述したDLLとENBのDLL名が同じか確認してください。拡張子を忘れずに。
-fojp.xmlのLoadDLLAsD3D9の値が1になっているか確認して下さい。


●d3d9.dllモードでReShadeと同時に使えない
-fojp.xmlのLoadDLLAsD3D9の値が0になっているか確認して下さい。


●d3d9.dllモードをENBと同時に使うとxinputの設定が効かなくなる
fojp.xmlのProxyLibraryPathにENBのDLL名を書いて、読み込み順をFOJP→ENBの流れにすれば解消できるはずです。
もし何らかの理由でENB→FOJPの流れ(enblocal.iniにFOJPのDLL名を書く)にしなければならない場合は、おまけDLLフォルダの_fojp_pad_assigner.dllをFOSE/NVSEプラグインとして使うと解決します。


●lStewieAl's Tweaksを導入するとログにフォントに関する警告がいっぱい並ぶ
たぶん無視して大丈夫です。(バージョン6.98時点では)



ソースコードについて
━━━━━━━━━━
・FOJPCFはFOJP2を(勝手に)改変して作りました。なので権利等はFOJP2の作者様が保有しています。
　FOJP2にはライセンスの記述がないので再利用についての制限はわかりません。(いちおう2chで「誰かまかせた」と10年前に言ってたから改変しても大丈夫…だと思う)
　とはいえ勝手に書き換えてる身なので、私からFOJPCFの改変・再配布等を禁止する事はありません。
　テキスト類は私が書いたものなので転載可能です CC4.0 BYという事にしてください。
・FOJP2のソースコードはこちら: https://ux.getuploader.com/fo3dlc_t/download/417
・コンパイルするにはDirectX SDKとBoostが必要です。後者はvcpkgでインストールしてください。
・FOJPはこんな感じの流れで動作しています。
  1. Hook.cppでグラフィック処理をフックし、FOJPDirect3D9を被せる。
  2. FOJPDirect3D9(Ex)→FOJPDirect3DDevice9(Ex)→FOJPVertexBuffer9とラッパーを作成していく
  3. ラッパーが横取りした頂点バッファをFOJPAnalyzerで調べて英文を抽出
  4. FOJPTranslatorで翻訳文を作成
  5. FOJPRendererで翻訳文のテクスチャと頂点バッファを作成して描写



謝辞
━━
このプログラムは様々な人やMODが共有した知見を元にして作られました。この場を借りてお礼申し上げます。
NexusのMODはできたらEndorseしてあげてください。

・FOJP2
もしFOJPのソースコードが公開されていなければ、私の能力でこれを作る事は間違いなく不可能でした。重ねて感謝します。

・不具合や記述ミスを指摘していただいた方々
自分では気が付きにくいのでとても助かりました。

・FOSE: https://fose.silverlock.org/
・NVSE: https://github.com/NVSEx/NVSE/releases
機能を使用させていただきました。

・computers_menu v3.zip: https://ux.getuploader.com/fo3dlc_t/download/442
・Fallout3+日本語化キット[20090308]S氏暫定最終ver[1].zip: https://ux.getuploader.com/fo3dlc_t/download/379
勝手ながら、同梱のメニューファイルはこちらの物をお借りしました。

・FOJP用VANILLA1.7.0.3日本語化[20110123].zip: https://ux.getuploader.com/fo3dlc_t/download/361
・FOJP用5DLCs日本語化[20120302]α版.rar: https://ux.getuploader.com/fo3dlc_t/download/397
・Fo:NV 日本語翻訳作業所 有志翻訳辞書: https://fonvj.ngnl.org/
・FoNV 英語名詞を日本語名詞化 v1.0: https://ux.getuploader.com/fo3dlc_t/download/405
・Fallout一括翻訳セット: https://onedrive.live.com/?cid=CF71A3D695ED6DE5&id=CF71A3D695ED6DE5!3776
・NVAC: https://www.nexusmods.com/newvegas/mods/53635
・Vanilla UI Plus: https://www.moddb.com/mods/vanilla-ui-plus
・lStewieAl's Tweaks (Fallout NV用): https://www.nexusmods.com/newvegas/mods/66347
・Radio Subtitles for Fallout 3 GOTY: https://www.nexusmods.com/fallout3/mods/23939
・Fo3-and-FoNV-イントロED字幕+bikmodv0.3e.zip: https://ux.getuploader.com/fo3dlc_t/download/427
・You're SPECIAL!日本語化ファイル: https://ux.getuploader.com/fo3dlc_t/download/349
・Vitomatic日本語化ファイル1: https://ux.getuploader.com/fo3dlc_t/download/347
・Vitomatic日本語化ファイル2: https://ux.getuploader.com/fo3dlc_t/download/348
引用させていただきました。

・Fallout: New Vegas 韓国語化パッチ: https://blog.naver.com/zhekuen
fojp.xmlの設定やラジオの翻訳方式を参考にさせていただきました。

・New Vegas Tick Fix: https://github.com/carxt/New-Vegas-Tick-Fix
・Oblivion Display Tweaks: https://github.com/ersh1/Oblivion-Display-Tweaks
・New Vegas Reloaded: https://github.com/Alenett/TES-Reloaded-Source-NEW
・PluginTestingGrounds: https://github.com/SlavicPotato/PluginTestingGrounds
DirectXに関するコードを参考にさせていただきました。
また、New Vegas Reloadedからはメモリ削減機能のコードを参考にさせていただきました。



コードを引用したMODの本許諾表示
━━━━━━━━━━━━
●New Vegas Reloaded (https://github.com/Alenett/TES-Reloaded-Source-NEW)
Copyright (C) 2020 Alessio Tamburini (aletamburini78@gmail.com)
All rights reserved.

Contributor(s):
 - Timeslip
 - scanti
 - ShadeMe
 - Ethatron
Additional contributions to the development MUST be authorized from the author.
 
Redistribution and use of the source code and binary, with or without modification, are permitted provided that the following conditions are met:

	  * the above copyright notice
	  * the conditions
	  * the following disclaimer
	  
THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDER(AUTHOR) 'AS IT IS'.
THE SOFTWARE IS DISTRIBUTED FOR FREE AND ANY EXPRESS OR IMPLIED MONEY REQUEST IS DISCLAIMED: YOU ARE FREE TO DONATE MONEY TO THE AUTHOR.
The licence terms can be eventually changed ONLY by the author.

You can contact the author for informations.

Official forum: www.tesreloaded.com
━━━



LEN-B
