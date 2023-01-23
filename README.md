# diary
これまで行ったことの記録用



# 2022年5月12日より記述する

## ある程度コンプラに反しない程度で業務のことも記述する

### 引き継ぎ内容 brc事業部proj
#### 技術は主にjs(スクレイピングのライブラリなどetc)
 - ローカル環境の構築

### 漫画proj
#### 技術は主にjs(Next)
 - 管理画面
   - 検索機能実装

### リファクタリング
#### 読んだもの
 - プリンシプルオブプログラミング
  - レガシーコード改善ガイド(わすれているので再読する)
 - laravel本(下)
#### 改善前
 - laravel
   - Serviceの実装数が多い状態
     - 同じ個所や似た箇所はまとめる

### テスト
既存のテストが作成されていて、実装に追加の項目が出来た際はテストの内容修正ではなく、新たに追加項目をテスト出来る部分を追加修正する
※方針間違っているかも

#### テスタビリティ
#### テスト駆動開発

### 環境構築
#### WSL2
Docker + VSCode + WSL2 & Laravelでweb環境を作成する

9月17日に自分で作成して遊べる環境を作成
作成した環境はrepositolyはprofileを参照

##### 以下参照したもの

1. [WSLドキュメント](https://docs.microsoft.com/ja-jp/windows/wsl/install)
2. [WindowsでWSL2を使って「完全なLinux」環境を作ろう！](https://www.kagoya.jp/howto/it-glossary/develop/wsl2_linux/)
3. [WSL2+Docker Desktop+UbuntuでLaravel9の開発環境を構築する](https://www.inet-solutions.jp/technology/laravel_sail/)

##### 問題に関連したもの

1. [DockerでWSL2を使うと上手くいかなかった話](https://laraweb.net/environment/9462/)
2. [gitでbranchの履歴が違った際にpush出来なかった話](https://qiita.com/mikumikumikumiku/items/3353018c72a1bf306f21)

### WSL2 + Next.js + Prisma

### WSL + Remix + Prisma + Tailwind
業務で行った

#### AWS + Docker

#### ngrok
ngrokというローカル環境にipを付け公開出来るサービスを利用し仮想的OGP画像の確認を行った
ローカルオブジェクトストレージに入れた画像と3000番ポートで動いているseedDataで入れた画像が別のサーバでホストされている問題があったがDBを直接操作して強引に検証した。
