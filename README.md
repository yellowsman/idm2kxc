# idm2kxc

ID ManagerからKeePassXCへのデータマイグレーションを支援するツールです。  
ID ManagerからエクスポートされたCSVファイルをKeePassXCのフォーマットに合わせて整形しインポート作業を効率化します。

- item1,item2に書かれた情報をコメントに追記します
- ディレクリの階層構造をKeePassXCに合わせた形に変換します

# 対応バージョン

- ID Manager: ver8.1
- KeePassXC: 2.7.12

# 使い方

## 準備

ID ManagerがエクスポートするCSVファイルは元のディレクトリの階層構造を完全に表現できていません。  
そのためCSVファイルをそのままインポートしても元のディレクトリの階層構造を再現できません。  
この問題を解消するためにID Manager上で次の作業を行った上でCSV形式にエクスポートをしてください。

- サブディレクトリと親ディレクトリの境界に親ディレクトリと同名のディレクトリを作成する

## ツール実行

```sh
gh clone yelloswman/idm2kxc
cd idm2kxc
gleam run -- origin_export_file.csv fixed_export_file.csv
```
