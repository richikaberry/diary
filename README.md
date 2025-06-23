# diary
これまで行ったことの記録用

# 学生時代
- 2017年4月 専門学校入学
  - PHPを主に学習した
    - LAMP環境での実装が主だったもの
    - Laravelを用いたチーム開発
      - この時にgitに初めて触れました
  - 他にC#やJavaなどを授業として学習した
    - インストーラー画面をC#を用いて開発しました
    - Android StudioでJavaやkotlinを使用して、モバイルアプリケーションの作成が好きでした
- 2021年3月 同専門学校を卒業
- 同年 4月に株式会社ゼネラルリンクに入社

# 2021年4月からのものを以下に記載する

## コンプラに反しない程度で業務のことを記述します

### 広告効果計測ツールの追加機能作成
#### docker + laravel + React
 - 一部媒体の担当
   - 他の媒体と違い広告掲載元でAPIが存在せず、広告効果をcsvにしたものを取り込みビジネス側が見やすいものに描画する機能を作成

### 引き継ぎ内容 brc事業部proj
#### 技術は主にjs(スクレイピングのライブラリなどetc)
 - puppeteerを使用してクローリング

### 漫画proj
#### 技術は主にTypeScript(Remix, Next.js)
 - 自社従業員用の管理画面
   - 検索機能実装
   - プライバシーポリシーなどの投稿画面の実装

 - ユーザー画面
   - クリエイター一覧表示(並び順を変更など)

### 2022年12月から「よめるも」として掲載
 - この時にRemixとNext.jsに初めて触り、Remixは自分の強みとなるフレームワークになった

# 2024年1月以降のもの

### 移管作業
#### 購入したメディアをエンジニアとして自社に移管した
 - メディアの移管先として何が最も良いかを考え移管した

### 施工王
#### 施工王建て付け
 - 施工王デプロイ環境の構築
  - デプロイフローの手順化

 - 待遇診断
  - 残業時間、休日数、年収を入力いただけば、自社でこれまで扱った求職者さん方と比較して現在の待遇を診断出来るというもの
  - docker + Remix + Prisma + AWS を用いて開発からリリースまでを担当

 - 施工職種向けコラム記事掲載サイト「施工王」を施工職種向け求人掲載サイトにリニューアル
   - PHPやライブラリなどを使用して対応

### リファクタリング
#### 読んだもの
 - リーダブルコード
  - 定期的に読み直しているが、ちゃんとプログラミングの深さを知るとやっぱり難しいですね
 - プリンシプルオブプログラミング
 - レガシーコード改善ガイド(わすれているので再読する)
 - laravel本(下)
#### 改善(リファクタリング)前
 - laravel
   - Serviceの実装数が多い状態
     - 同じ個所や似た箇所はまとめる
     - Traitを使用した

 - Remix
   - component化の粒度が適切でなかった
   - 使い回し易い形に修正

 - DB
   - 正規化出来ていないいない状態だった
     - ある程度まで正規化して重複データを消した
     - 仕様上、やり過ぎにないほどに留めている

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

#### circleci
circleci/config.ymlの設定
docker imageを用いたenvironmentの設定
開発環境で使用するMySQLやDocker-comopose.ymlはdockerレジストリに存在するのでそこに合わせた設定にする必要があった。
docker imageにはcimg/mysqlは存在しなかったのでdocker image としてMySQLを使用して、authのusernameとpasswordをデフォルトのもので設定している。
docker image は `docker images`コマンドで確認する。
portも確認しておくと良い。

### WordPress
施工王でWordPressを使用した
