# python-config-object
[![MIT License](http://img.shields.io/badge/license-MIT-blue.svg?style=flat)](LICENSE)  
iniファイルに記述されている設定をPython内から取得しやすくするためのConfigオブジェクト

## 作者
Masaya Suzuki <suzukimasaya428@gmail.com>

## バージョン
0.0.1

## 開発言語・必要なソフトウェア
* [Python](https://www.python.org/) 3.x

## 使い方
1. Pythonのプログラムが格納されているディレクトリに移動します、
1. `git clone https://github.com/massongit/python-config-object configs`コマンドを実行します。
1. プログラム内で以下のような形で使用します。
    ```py
    import pathlib
    
    import configs
    
    # Configオブジェクト
    # (pathlib.Pathでiniファイルが格納されているディレクトリを指定する)
    conf = configs.Config(pathlib.Path.cwd())
    
    # iniファイルに記述されている設定を取得する
    conf.get('設定ファイル名 (拡張子なし)', 'セクション名', '設定名')
    
    ```

## ディレクトリ構造
* .gitignore: Gitの管理から除外するファイル一覧
* \_\_init\_\_.py
* config.py: Configオブジェクト
* LICENSE: ライセンス
* README.md: README (MarkDown形式)
