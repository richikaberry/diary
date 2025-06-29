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

#### コンプラに反しない程度で業務のことを記述します

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
   - Topページの作成などを担当

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
作成した環境はrepositolyのLaravel-templateを参照

#### Mac Docker環境
- Cook Dogの環境がそうです

#### WordPress Docker環境
- Privateになりますが、上記環境の作成が可能です
- レンタルサーバーにある環境をそのまま、開発環境とすることが出来ます

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
メディア移管したものの構成がWordPressだったので、その際に学習し、追加開発などを行なった。

## これまでに読んだ本
- [プロを目指す人のためのTypeScript入門 安全なコードの書き方から高度な型の使い方まで](https://www.amazon.co.jp/%E3%83%97%E3%83%AD%E3%82%92%E7%9B%AE%E6%8C%87%E3%81%99%E4%BA%BA%E3%81%AE%E3%81%9F%E3%82%81%E3%81%AETypeScript%E5%85%A5%E9%96%80-%E5%AE%89%E5%85%A8%E3%81%AA%E3%82%B3%E3%83%BC%E3%83%89%E3%81%AE%E6%9B%B8%E3%81%8D%E6%96%B9%E3%81%8B%E3%82%89%E9%AB%98%E5%BA%A6%E3%81%AA%E5%9E%8B%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9%E3%81%BE%E3%81%A7-Software-Design-plus/dp/4297127474?tag=googhydr-22&source=dsa&hvcampaign=books&gad_source=1)
- [TypeScriptとReact/Next.jsでつくる実践Webアプリケーション開発](https://www.amazon.co.jp/TypeScript%E3%81%A8React-Next-js%E3%81%A7%E3%81%A4%E3%81%8F%E3%82%8B%E5%AE%9F%E8%B7%B5Web%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3%E9%96%8B%E7%99%BA-%E6%89%8B%E5%B3%B6-%E6%8B%93%E4%B9%9F/dp/4297129167)
- [PHPフレームワーク Laravel 実践開発](https://www.amazon.co.jp/PHP%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AF-Laravel%E5%AE%9F%E8%B7%B5%E9%96%8B%E7%99%BA-%E6%8E%8C%E7%94%B0-%E6%B4%A5%E8%80%B6%E4%B9%83/dp/4798059072/ref=sr_1_1_sspa?adgrpid=85568052222&dib=eyJ2IjoiMSJ9.u1VgSJoGTH5k5RTY6BkJ6o0cBQxt2BZ1yetQv7y4Bn-d3Moj646viv2JnWJg4PukyMGuNxLkIxemdqKiQ2mOFY6-2Y7XMBtf7yBR0JWfsgSI5Gig2Y7rNDCcOZmzIemsIGco0UqxA8au5Mgj2D87l6UYM1RyTYsZTKKpox29AqFT8wMufspea_ptNa5hT7cEoDiWTKi8XFSNXxJ-hgngYSMfgCLCMYsmvI0au3xslNoNaYyhUfjmxtPJgnix8nVzZrwbhUx_I-M1DWbCgxcmjf6H0TYR_i4Ofyeu8C1na3U.iVDqtCZnVci9fUUt8pPQHNUyWJPbkcqZ5mWMqIx2O3U&dib_tag=se&hvadid=678999093796&hvdev=c&hvexpln=0&hvlocphy=1009308&hvnetw=g&hvocijid=9076286250871594973--&hvqmt=e&hvrand=9076286250871594973&hvtargid=kwd-891718879164&hydadcr=1821_13656974&jp-ad-ap=0&keywords=php%E3%83%95%E3%83%AC%E3%83%BC%E3%83%A0%E3%83%AF%E3%83%BC%E3%82%AFlaravel%E5%AE%9F%E8%B7%B5%E9%96%8B%E7%99%BA&mcid=a894a0a7a9dc3dfab09022e3f421284f&qid=1751239081&sr=8-1-spons&sp_csd=d2lkZ2V0TmFtZT1zcF9hdGY&psc=1)
- [レガシーコード改善ガイド](https://www.amazon.co.jp/%E3%83%AC%E3%82%AC%E3%82%B7%E3%83%BC%E3%82%B3%E3%83%BC%E3%83%89%E6%94%B9%E5%96%84%E3%82%AC%E3%82%A4%E3%83%89-Object-Oriented-SELECTION-%E3%83%9E%E3%82%A4%E3%82%B1%E3%83%AB%E3%83%BBC%E3%83%BB%E3%83%95%E3%82%A7%E3%82%B6%E3%83%BC%E3%82%BA/dp/4798116831/ref=sr_1_1?adgrpid=156327580482&dib=eyJ2IjoiMSJ9.Kem2f28RTWMOu7rFHElhzpdyJLNK2fJG8Fvj5qZdDLJhY2TpP1ax2OXKdcIF6yZF894jPFZ_fFRZPVGon3gO4x-XhsluLJ30py3SXRy88tYfghQNIuqJW3V-yrvyI7D20i4uLJEJbWvwQLDTpWSLweEfgqB1fmOUNx2onAnOWcg.ucpbMhW6bje_d6_oRZmWe1II6d2JpTFjEAy6ijazrEQ&dib_tag=se&hvadid=678960091419&hvdev=c&hvexpln=0&hvlocphy=1009308&hvnetw=g&hvocijid=4960662874872939295--&hvqmt=e&hvrand=4960662874872939295&hvtargid=kwd-2260029545698&hydadcr=1793_13656984&jp-ad-ap=0&keywords=%E3%83%AC%E3%82%AC%E3%82%B7%E3%83%BC%E3%82%B3%E3%83%BC%E3%83%89+%E6%94%B9%E5%96%84+%E3%82%AC%E3%82%A4%E3%83%89&mcid=4299ee2cfc723dc8bb711899f1c38a8a&qid=1751239150&sr=8-1)
- [プリンシプル オブ プログラミング3年目までに身につけたい一生役立つ101の原理原則](https://www.amazon.co.jp/%E3%83%97%E3%83%AA%E3%83%B3%E3%82%B7%E3%83%97%E3%83%AB-%E3%82%AA%E3%83%96-%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9F%E3%83%B3%E3%82%B03%E5%B9%B4%E7%9B%AE%E3%81%BE%E3%81%A7%E3%81%AB%E8%BA%AB%E3%81%AB%E3%81%A4%E3%81%91%E3%81%9F%E3%81%84%E4%B8%80%E7%94%9F%E5%BD%B9%E7%AB%8B%E3%81%A4101%E3%81%AE%E5%8E%9F%E7%90%86%E5%8E%9F%E5%89%87-%E4%B8%8A%E7%94%B0-%E5%8B%B2/dp/4798046140)
- [Web APIの設計](https://www.amazon.co.jp/s?k=web+api+%E3%81%AE%E8%A8%AD%E8%A8%88&adgrpid=149103126875&hvadid=678993809020&hvdev=c&hvexpln=0&hvlocphy=1009300&hvnetw=g&hvocijid=6372416094363405553--&hvqmt=e&hvrand=6372416094363405553&hvtargid=kwd-2079840944346&hydadcr=28576_14790595&jp-ad-ap=0&mcid=d2d2f0450c4f3e7c958db5b77380fd40&tag=googhydr-22&ref=pd_sl_8n0envnrcm_e)
- [エンジニアが知っておきたい思考の整理術　複雑な情報を【理解する】【伝える】テクニック](https://www.amazon.co.jp/%E3%82%A8%E3%83%B3%E3%82%B8%E3%83%8B%E3%82%A2%E3%81%8C%E7%9F%A5%E3%81%A3%E3%81%A6%E3%81%8A%E3%81%8D%E3%81%9F%E3%81%84%E6%80%9D%E8%80%83%E3%81%AE%E6%95%B4%E7%90%86%E8%A1%93-%E8%A4%87%E9%9B%91%E3%81%AA%E6%83%85%E5%A0%B1%E3%82%92%E3%80%90%E7%90%86%E8%A7%A3%E3%81%99%E3%82%8B%E3%80%91%E3%80%90%E4%BC%9D%E3%81%88%E3%82%8B%E3%80%91%E3%83%86%E3%82%AF%E3%83%8B%E3%83%83%E3%82%AF-%E9%96%8B%E7%B1%B3-%E7%91%9E%E6%B5%A9/dp/4295018295?tag=googhydr-22&source=dsa&hvcampaign=books&gad_source=1)
- [失敗から学ぶRDBの正しい歩き方 (Software Design plus)](https://www.amazon.co.jp/%E5%A4%B1%E6%95%97%E3%81%8B%E3%82%89%E5%AD%A6%E3%81%B6RDB%E3%81%AE%E6%AD%A3%E3%81%97%E3%81%84%E6%AD%A9%E3%81%8D%E6%96%B9-Software-Design-plus-%E6%9B%BD%E6%A0%B9/dp/4297104083?tag=googhydr-22&source=dsa&hvcampaign=books&gad_source=1)
