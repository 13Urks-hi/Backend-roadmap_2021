# ターミナルの使い方

## そもそもターミナルとはなんぞや💻

ターミナルとは、テキストベースのプログラムを実行するためのテキストインターフェースのこと。
 - 言葉の意味は**端末**
 - この項目では**コマンドライン**でコマンドを実行することについての説明をしていく

Web開発のツールを使っている多くの場合、コマンドラインを開き、コマンドを実行するということを行うのが一般的。  
コマンドを入力するツールを **CLI(コマンドラインインターフェース)** ツールと呼ぶ。  
(コマンドラインの難点？は *黒い画面に文字打つところだけ* 、みたいなのばかりで最初見た時はびっくりするはず...)

### ターミナルの歴史と利便性👴

- 起源は1950年代から60年代頃、その頃のターミナルは今とは全く違うようなもの
- ターミナルは生まれてから、デスクトップやクラウド、マイクロコンピュータや携帯電話などのあらゆるオペレーティングシステムに一貫して存在し続けている
- ターミナルは基本的なファイルシステムや機能に直接アクセスできるため、自分が何をしているのかを理解できていれば複雑なタスクも迅速に実行するのに便利
- 自動化にも有効で、数百のファイルのタイトルを瞬時に更新するコマンドを記述することが可能
  - FinderやExplorer、GUIをつかうよりずっとはやい

**これからもターミナルはなくなることはないでしょう...**👍

## ターミナルへのアクセス

現在多くの開発者は、 **Unixベース** のツールを使っている。
また、多くのチュートリアルもUnixベースをサポートしていることが多い。(Unixベースであればほとんどのシステム利用可能であるため)
- UnixやLinuxの話、OSの話は次項でも詳しくやる

### Linux/Unix
- 上で記載したように、LinuxやUnixではデフォルトでターミナルが使用可能で、アプリケーションの中にリストアップされているもの

### macOS
- いつもつかっているmacOS、このGUIの下には **Darwin** というUnixライクなシステムがある
  - Unixのような、といえどほぼUnixと同じと思ってよい
- macOSでターミナルは `Applications/Utilities/Terminal` で利用可能
  - ターミナルっていうアプリがあるね

### Windows
- Windowsのターミナル(コマンドライン)は他のプログラミングツールと同様に、他のオペレーティングシステムほどシンプルなものではない
  - かといってそんなに難しいものでもないから安心して
- 以前から **cmd** という **独自の** ものがあり、Unixコマンドとの一致性がなく旧式の Windows DOSプロンプトに相当するもの
- **Powershell** や **Gitbash** (Windows用のgitツールセット) などWindowsのターミナルを利用するための他のより良いものもある
- ただ、Windowsにとっていまの最良の選択肢はおそらく **Windows Subsystem for Linux(WSL)** 
  - Windows10の内部から直接LinuxOSを実行するための相互レイヤ。仮想マシンを必要としないWindows上で直接 _本当のターミナル_ を実行できるようにするためのもの
  - Windowsストアから無料でインストールできる

#### コマンドラインとターミナルは何が違うの...?
- 同じ意味とされることが多く、ただの言い方の違い
- 技術的にはターミナルはシェルを起動して接続するためのソフト、コマンドラインは言葉の通りコマンドを入力してたカーソルが点滅する行のこと

## 基本的なターミナルのコマンドたち
コマンドと、そのコマンドでできることを少しだけ紹介

- コンピュータのディレクトリやファイルの操作
  - `cd` ディレクトリを移動
  - `mkdir` ディレクトリの作成
  - `touch` ファイルの作成（と、そのデータの変更）
  - `cp` ファイルの作成 
  - `mv` ファイルの移動
  - `rm` ファイルの削除およびディレクトリの削除
- `curl` 指定したURLで見つかったファイルをダウンロード
- `grep` 大きなテキストの中の部分検索
- `less`, `cat` ファイルの内容を１ページずつ表示する
- `awk`, `tr`, `sed` テキストの変換（例えばHTMLファイル内のすべてのdivをarticleに変更する)

### コマンドをつなげる
  - `;`, `&&`, `||`　を使用することで一連のコマンドを順次実行することができる
    - `&&`　記号の前にあるコマンドが **成功** すると記号の後ろに続くコマンドが実行される
    - `||` 記号の前にあるコマンドが **失敗** すると記号の後ろに続くコマンドが実行される 
  - `|`　を使用すると複数のコマンドを変更して実行することができる

他にも色々たくさんあるよ！

## ターミナルコマンドで気をつけたいこと
ターミナルコマンド操作は単純、  
それによって複雑なコマンドを組んだりするときにはそのコマンドが何をするのかをよく考えた上で実行することを心がけよう。  
[コマンドを試すサイト](https://glitch.com/) とかもあるのでそこで試してから本当に実行するのもよし。

