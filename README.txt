お手軽IDE
=========

インストール不要の、Eclipse (Pleiades) 風 Java・HTML・DB・Spring 独習環境です。
zip を展開して start.bat (Mac は start.command) をダブルクリックするだけで、ブラウザに IDE が開きます。
Eclipse も JDK も Tomcat も Oracle Database も、管理者権限も要りません。
Java (JRE 17)、Spring Boot のライブラリ一式、データベース (H2・Oracle 互換モード) を zip に同梱しています。

教材には、Qiita の入門シリーズ「【Java入門】目次 ( https://qiita.com/chida0818/items/1f0f457d575d4a675c16 )」「【HTML入門】目次 ( https://qiita.com/chida0818/items/4efc23bf7222b2377b2d )」「【DB入門】目次 ( https://qiita.com/chida0818/items/d1fbd989a20e8eed1cbc )」「【Spring入門】Webアプリを作りながら学ぶ ( https://qiita.com/chida0818/items/878ad4d31ab922743e01 )」を使います。
右側の「教材」に本文が表示され、教材のコードをエディターやワークシートに反映したり、実行結果を教材と比べたりできます。

【ダウンロード】

OtegaruIDE.zip ( https://github.com/GreatChida/Otegaru/releases/latest/download/OtegaruIDE.zip ) をダウンロードしてください (約 113MB)。Windows と Mac で同じ zip を使います。
版ごとの説明は Releases ( https://github.com/GreatChida/Otegaru/releases ) にあります。

【Eclipse のプラグイン (テスト版)】

本物の Eclipse (Pleiades 2026-06) の中で、Qiita の「Java入門」「HTML入門」「Spring入門」を Qiita と同じ見た目で読み、コードの反映や実行結果の比較ができるプラグインです。
インストール方法は こちら ( https://greatchida.github.io/Otegaru/eclipse/ ) を見てください。

【動作環境】

・Windows 11、または macOS (Apple Silicon)
・Google Chrome (最新版)。ほかのブラウザは対象外です
・インターネット接続 (Qiita の最新の教材を読み込むため。つながらないときは、内蔵の教材で進められます)

Chrome が既定のブラウザでない場合は、起動したあと、黒いウィンドウ (Mac はターミナル) に表示されるアドレスを Chrome で開いてください。

【使い方 (Windows)】

1. ダウンロードした zip を右クリックして プロパティ を開き、下の「セキュリティ」の 許可する にチェックを入れて OK を押します。
   (インターネットから取得したファイルのため、これをしないと起動時に警告が出ることがあります)
2. zip を好きな場所に展開します (例: デスクトップ)。深いフォルダーの中は避けてください。
3. 展開した OtegaruIDE フォルダーの start.bat をダブルクリックします。黒いウィンドウが開き、ブラウザにお手軽IDE が表示されます。
4. 最初の起動では、学ぶ教材と、書いたプログラムの保存先を確かめて 起動 をクリックします (「最初の起動」を参照)。
5. 終わるときは、メニューの ファイル → 終了 を選ぶか、黒いウィンドウを閉じます。

【使い方 (Mac)】

1. ダウンロードした zip をダブルクリックします。OtegaruIDE フォルダーができます。好きな場所 (例: 書類) に移してください。
2. OtegaruIDE フォルダーの start.command をダブルクリックします。
3. 最初の 1 回だけ、「"start.command" は開いていません」などと表示されて起動できません。このときは 完了 をクリックして閉じます (ゴミ箱に入れる は押さないでください)。
4. Apple メニュー → システム設定… → プライバシーとセキュリティ を開き、「セキュリティ」の欄の「"start.command" がブロックされました」の右にある このまま開く をクリックします。確認の画面でも このまま開く をクリックし、パスワードを入力します。
5. ターミナルのウィンドウが開き、ブラウザにお手軽IDE が表示されます。最初の起動では、学ぶ教材と保存先を確かめて 起動 をクリックします。
6. 終わるときは、メニューの ファイル → 終了 を選ぶか、ターミナルのウィンドウを閉じます。

2 回目からは、start.command をダブルクリックするだけで起動します。
ショートカットは Mac の Eclipse と同じく、Ctrl の代わりに ⌘ を使います (保存は ⌘S、実行は ⌘F11)。補完だけは Control + Space です。
macOS の初期設定では Control + Space が入力ソースの切り替えに使われているので、システム設定の キーボード → キーボードショートカット… → 入力ソース で「前の入力ソースを選択」のチェックを外してください。

【最初の起動】

最初の起動では、次の 2 つを確かめる画面が出ます。

・学ぶ教材: 「入門シリーズ (HTML/DB/Java/Spring/Git)」か「Spring超入門 (はじめての人向け)」を選びます。あとから、メニューの ヘルプ → 教材の切り替え で変えられます。
・保存先: 書いたプログラムを保存するワークスペースの場所です。最初は、ドキュメント (Mac は書類) の workspace フォルダーです。

入門シリーズを選んだときは、画面中央の「Java入門を見ながら始める」などをクリックすると、右側にその教材が表示されます。

【保存場所】

・書いたプログラムは、ワークスペースに、Eclipse と同じ形 (workspace/java/src/ch03/Basic.java など) で保存されます。.project と .classpath も作るので、後で本物の Eclipse の ファイル → インポート → 既存プロジェクトをワークスペースへ で取り込めます。
・データベースの内容 (コミットした表・データ・ユーザー) は、ワークスペースの .otegaru/h2 フォルダーに保存されます。
・選んだ保存先は、展開したフォルダーの workspace.json に記録されます。場所を選び直すときは、お手軽IDE を終了してから workspace.json を削除し、もう一度起動します。

【画面】

画面の左上の「画面」で、2 つの画面を切り替えます。

・IDE の画面: Eclipse と同じ画面です。Java プロジェクト・動的 Web プロジェクト (Tomcat で実行)・Spring スターター・プロジェクト (Spring Boot で実行) を作って動かせます。
・DB の画面: SQL Developer と同じ画面です。接続を作り、ワークシートで SQL を実行します (文の実行 Ctrl+Enter、スクリプトの実行 F5)。エラーは Oracle と同じ ORA- の番号と文言に置き換えて表示します。

右側の「教材」に表示する本文は、教材の上の切り替えで選べます。

・Qiita の最新 (既定): Qiita から最新の記事を読み込み、Qiita と同じ見た目で表示します。読み込んだ本文は 30 分間ブラウザに保存し、その間は読み込み直しません (Qiita の取得回数の上限は 1 時間に 60 回です)。読み込めないときは、前回読み込んだ本文か内蔵の本文を表示します。
・内蔵の教材: zip に入っている本文を表示します。

教材の章の頭には、Eclipse・Oracle Database と違うところを補う「お手軽IDE メモ」が出ることがあります。

【Eclipse と同じように使えるもの】

・ファイル → 新規 → Java プロジェクト / 動的 Web プロジェクト / Spring スターター・プロジェクト / パッケージ / クラス / インターフェース
    → ○ (Eclipse と同じダイアログ)
・保存 (Ctrl+S) すると自動でコンパイル
    → ○ (Eclipse と同じコンパイラー ECJ を使用)
・行の左の赤い ×、波線、マーカー・ビュー、パッケージ・エクスプローラーの ×
    → ○ (エラー文は Pleiades と同じ日本語)
・実行 (Ctrl+F11)、実行 → Java アプリケーション
    → ○ (コンソールに <終了> 表示。例外は赤い文字で、行番号のリンクから該当の行を開ける)
・補完 (Ctrl+Space)、sysout main for foreach if try などのテンプレート
    → ○ (import も自動で入る)
・フォーマット (Ctrl+Shift+F)、コメントの切り替え (Ctrl+/)、インポートの編成 (Ctrl+Shift+O)
    → ○
・ソース → getter および setter の生成 / toString() の生成 / コンストラクターの生成
    → ○
・クイック・フィックス (Ctrl+1)、宣言を開く (F3)、行へ移動 (Ctrl+L)
    → ○ (よく使うもの)
・エディターの文字の大きさ (Ctrl+Shift++ で大きく、Ctrl+- で小さく)
    → ○
・コンソールからの入力 (Scanner)
    → ○
・キー・アシスト (Ctrl+Shift+L)
    → ○

ダイアログを開いている間も、教材はスクロールして読めます。ダイアログはタイトルバーをドラッグして動かせます。
Mac では表の Ctrl を ⌘ に読み替えてください (補完の Control + Space は除く)。
ブラウザーの都合で Ctrl+N・Ctrl+W・Ctrl+T (Mac は ⌘N・⌘W・⌘T・⌘Q・⌘H・⌘M) は使えません。

【Eclipse・Oracle Database と違うところ】

・データベースは、Oracle Database ではなく H2 (Oracle 互換モード) です。メッセージの文面など、Oracle Database と違うところがあります。正確に決められないエラーは「※ 推定です」と表示し、H2 の元のメッセージも見られます。
・デバッガー (ブレークポイント) はありません。

【困ったときは】

・start.bat を開くと「Windows によって PC が保護されました」などの警告が出る
    → 使い方 (Windows) の 1. のとおり、zip の「許可する」にチェックを入れてから展開し直してください。
・「Windows セキュリティ」で、ネットワークへのアクセスを許可するか聞かれる
    → お手軽IDE は、このパソコンの中だけで使います。「キャンセル」を押してかまいません。
・ブラウザが開かない、または Chrome 以外のブラウザで開く
    → 黒いウィンドウ (Mac はターミナル) に表示されているアドレスを Chrome で開いてください。
・Mac で「"start.command" は開いていません」と出る
    → 使い方 (Mac) の 3.〜4. のとおり、システム設定の「プライバシーとセキュリティ」で このまま開く をクリックしてください。
・Mac で補完 (Control + Space) が効かない
    → 使い方 (Mac) の最後のとおり、キーボードショートカットの「前の入力ソースを選択」のチェックを外してください。
・教材に「Qiita の取得回数の上限」と出る
    → しばらく待ってから「再読み込み」を押すか、教材の切り替えで「内蔵の教材」を選んでください。

【仕組み】

・zip に同梱の Java (JRE 17) で、お手軽IDE のサーバーを動かします。画面はブラウザに表示します。
・コンパイルには ECJ (Eclipse Compiler for Java) を、データベースには H2 (Oracle 互換モード) を使います。
・Spring Boot のアプリケーションは、同梱のライブラリ一式で、インターネットからの追加のダウンロードなしに動きます。

【ライセンス】

・お手軽IDE 自体: ライセンスは未定です。
・Java 実行環境 (OpenJDK 17.0.19 の JRE。Eclipse Temurin): GPL v2 + Classpath Exception
・ECJ (Eclipse Compiler for Java) ( https://github.com/eclipse-jdt/eclipse.jdt.core ) 3.45.0: Eclipse Public License 2.0。ソース・コードは Maven Central ( https://repo1.maven.org/maven2/org/eclipse/jdt/ecj/3.45.0/ ) から入手できます。
・H2 Database Engine ( https://h2database.com/ ) 2.5.252: MPL 2.0 / EPL 1.0
・Spring Boot ( https://spring.io/projects/spring-boot ) 4.1.2 と関連するライブラリ: 主に Apache License 2.0 (各ライブラリのライセンスに従います)
・CodeMirror ( https://codemirror.net/5/ ) 5.65.16: MIT License
・marked ( https://marked.js.org/ ) 12.0.2: MIT License
・教材本文: Qiita「【Java入門】 ( https://qiita.com/chida0818/items/1f0f457d575d4a675c16 )」「【HTML入門】 ( https://qiita.com/chida0818/items/4efc23bf7222b2377b2d )」「【DB入門】 ( https://qiita.com/chida0818/items/d1fbd989a20e8eed1cbc )」「【Spring入門】 ( https://qiita.com/chida0818/items/878ad4d31ab922743e01 )」シリーズ (chida0818) の記事です。
