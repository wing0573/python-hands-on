# A研 Python 講習
## 目的
- 基礎的な Python 開発能力の取得
- 良いコードを書く練習
- Git, GitHub が使えるようになる


## 形式
演習形式で行う。この講習で開発したコードは GitHub に上げて (個人用のブランチ)，プルリクエストを投げる形で提出する。(Git, GitHub の使い方については最初の講習で説明する。)


## 課題に取り組むにあたって
- 積極的に先輩に質問したり，同期と相談しながら取り組むこと
- わからないのは問題ないが，どうしてわからないのか，どこにつまづいているのか言語化出来るようにすること
- ググる，コピペなんでもOK!
    - ググる力 (googlability) も能力の一つ
    - ただし，どうしてそのコードを書いたのかきちんと言語化出来るように

> 参考：[Python 公式ドキュメント](https://docs.python.org/ja/3/)


## 環境構築
### 1. `Homebrew` のインストール
ターミナルを起動して以下のコマンドを実行
```bash
$ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

#### `Homebrew` とは？
OSX (macOS) 用のパッケージマネージャー。様々なパッケージの管理 (インストール，アップグレード，etc.) を容易に行うことが出来るコマンドラインツール。
- プログラム言語 (Python, Go, Node.js など)
- テキストエディタ (Vim, Neovim, Emacs など)
- コマンドラインツール (git, curl, tree など)

> 参考：https://brew.sh/index_ja

### 2. `pyenv` のインストール
1. `Homebrew` を用いて `pyenv` をインストール
```bash
$ brew install pyenv
```

2. `pyenv` を使用するためのセットアップを行う
```bash
$ echo 'export PYENV_ROOT=/usr/local/var/pyenv' >> ~/.bash_profile
$ echo 'eval "$(pyenv init -)"' >> ~/.bash_profile
$ source ~/.bash_profile
```

3. `pyenv` を用いて，Python の最新バージョン (3.7.2) をインストール，およびセットアップを行う
```bash
$ pyenv install 3.7.2
$ pyenv global 3.7.2
$ pyenv rehash
```

#### `pyenv` とは
Linux において，Python の実行環境を管理するためのツール。2.x系, 3.x系を使い分ける，開発プロジェクトごとにバージョンを切り替えることなどに用いられる。

> 参考：https://github.com/pyenv/pyenv


### 3. `Pipenv` のインストール
`pip` をアップデートする
```bash
$ pip install -U pip
```

`pip` を用いて，`Pipenv` をインストールする
```bash
$ pip install pipenv
```

#### `pip` とは
Python のパッケージを管理するためのツール。サードパティ (公式が配布していないパッケージ) を管理するのに用いる。

> 参考：https://www.sejuku.net/blog/50417

#### `Pipenv` とは
簡単に Python の開発環境を作れる方法を提供するツール。`Pipfile` に対してパッケージの追加および削除を行うのに加え，自動でプロジェクト用の仮想環境を作成し，管理する。また `Pipfile.lock` も同時に生成し，これを利用して常にビルドが同じ結果になるようにする。

> 参考：https://pipenv-ja.readthedocs.io/ja/translate-ja/


### テキストエディタ
#### テキストエディタとは？
PC上でメモやプログラムを書くことの出来るソフト。Windowsでは「メモ帳」，Macでは「テキストエディット」という名前のアプリケーションがデフォルトで入っている。

メモ帳等でもプログラミングをすることは出来るが，プログラミング用のテキストエディタを使うことで効率よく開発作業が行うことが出来る。

様々なテキストエディタがあるがどれを使っても問題ないので，好みで選ぶと良い。

#### おすすめ
##### Visual Studio Code (VSCode)
Microsoft が開発したオープンソースのテキストエディタ。高機能かつインターフェースが洗練されているため，非常に使いやすい。正直これが一番良いと思う。

> 公式HP：https://code.visualstudio.com/

##### Atom
GitHub が公開したテキストエディタ。便利なプラグインが多く，またインターフェースが非常に見やすいため，初心者でも使いやすい。Windows，macOS，Linux で利用できるので誰でも手軽に使える。ただ少し動作が重たい。

> 公式HP：https://atom.io/

##### Vim
主にCUI環境 (ターミナル) で使われるエディタ。歴史が古く多くのユーザーに使われている。独特のキーバインドは最初はとっつきづらいが，なれると高速で作業ができるようになる。

> 公式HP：https://www.vim.org/

##### Emacs
Vim同様CUI環境で使われるエディタ。ターミナル上でのキーバインドと親和性が高く，最初は Vim よりは使いやすい？かもしれない。

> 公式HP：https://www.gnu.org/software/emacs/
