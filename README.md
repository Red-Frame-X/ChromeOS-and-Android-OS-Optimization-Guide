# Chrome-OS-and-Android-OS-Optimization-Guide
ChromeOS・Android OS：最適化ガイド
- Original：<https://writening.net/page?cEEujp>

## About Me
「IT学習の一環」として、デバイス設定の記録やAdGuard Custom Rules / UserScript / Regexの作成などに取り組んでいます。
AdGuard Filters Issuesへの報告や、Google、𝕏、ソフトウェア開発者様、サイト運営者様へのフィードバックも時々行っています。
MacBook Pro、Lenovo ThinkPad、Dell Inspironを経て、Chromebookへ移行しました。
現在使用しているデバイスは、Acer Chromebook Plus 514とGoogle Pixel 7aで、5chのノートPC板、Android板、ソフトウェア板を時折訪れている半ROMです。

**Contact**
- User Name：Red Frame X
- 𝕏：<https://x.com/Red_Frame_X>
- GitHub：<https://github.com/Red-Frame-X>
- Gists：<https://gist.github.com/Red-Frame-X>

---

## Subscription
Googleの多くのサービスでは、年額サブスクリプションを「月額 × 約10か月分」の料金で提供しており、割安になります。
ただし、年額サブスクリプションは一度支払うと、契約期間の途中で解約しても日割り計算による払い戻しは行われません。

### ◆ 利用中のサブスクリプション一覧
サブスクリプションの購読基準は、「ITインフラになり得ているか」と「保守の負担比率が、対処 > 利用になった」という点に尽きます。

- Amazon Prime（年額）
- ChMate スタンダードプラン（月額）
- Google AI Plus 200 GB（月額）
- mond｜Kdroidwinさんのメンバーシップ｜[Premium（月額）](https://mond.how/ja/kdroidwin)
- 𝕏プレミアム ベーシック（年額）
- YouTube Premium（年額）

トラブルを完全に避けるのであれば、サブスクリプションを一切契約しないのが最も安全です。
必要があって契約する場合は、トラブルの原因となりやすい携帯キャリア提供の月額オプションは避け、公式サイトが直接提供するプランを必要最小限選ぶのが無難です。

- **【お詫び/復旧】一部お客さまでドコモからご契約いただいたYouTube Premiumがご利用いただけない事象について**
  <https://www.docomo.ne.jp/info/notice/page/251222_03_m.html>

### ◆ Google One メンバーシップ・不具合
下記の購入特典と有料プランにおいて、システム上で重複適用できてしまう不具合がありました。
1. Chromebook Plusの購入特典（Google AI Pro 2 TB 1年間無料）
2. docomo 爆アゲ セレクション Google One ベーシック（100 GB）（月額）
3. Google AI Pro 2 TB（年額）

確認を怠ってこれらを重複適用してしまうと、Google OneのWebサイトでストレージ容量を正確に取得できず、コンテンツの確認ができなくなるエラーが発生します（<https://imgur.com/CNjeA2d>）。
Google One Webサイトの左側バー > 「ストレージとプラン」を選ぶと500エラーが表示され、ページを開けなくなります（<https://imgur.com/cIa8AJt>）。

Android版Google Oneアプリの左側バー > 「メンバーシップ プラン」の表示では、docomoのプランが優先して表示されるロックがかかり、解除が困難になります（<https://imgur.com/a/u9f38dX#3dKWbMC>）。

※ 以下2つの記述は未検証の仮説です。
1. Google One メンバーシップ プランの管理権限が、Googleからdocomoの月額プランへ一時的に移管されます。
2. dポイントが付与される代わりに、Google公式のAIプラン（Google AI Plus 200 GB〜）が選択できなくなります（[リンク](https://one.google.com/about/plans?hl=ja-JP&g1_landing_page=0)）。

不具合の内容をコピー＆ペーストできるようメモにまとめ、お問い合わせ方法からチャットを選択します。
- **Google One ヘルプ > お問い合わせ**: <https://support.google.com/googleone/gethelp>

なお、ahamo回線契約者は基本的にdocomoのサポートを受けることができません。
- **docomo｜ご意見・ご要望 > 「ご意見・ご要望はこちら 開く+」をクリック**: <https://www.docomo.ne.jp/support/inquiry/feedback/?hl=ja-JP>

過去に同様の不具合がなかったかRedditで検索したところ、既存の有料プランにGoogle Pixelの購入特典を重複適用した結果、Google One メンバーシップに問題が発生したという報告も見つかりました。

**Google free trial Premium AI Scam**
<https://www.reddit.com/r/GoogleOne/comments/1dqzsrv/google_free_trial_premium_ai_scam/>
- 2TBの年額プランを契約中のユーザーが、Pixel 8 Pro購入特典の4ヶ月無料トライアルを有効化した事例です。
- 元のプランが上位プランに強制変換された結果、支払い済みの契約期間が大幅短縮され、元のプランの権利が失われたと報告されています。

問題が長期化し、週に1回程度のペースでGoogle One ヘルプに進捗確認を求めても、定型文の返答しか得られないことがあります。
GoogleとdocomoにGoogle Oneの不具合を問い合わせても、たらい回しにされるばかりで、問題が解決する見込みがありませんでした。
これらの不具合の多くは、複数の契約がGoogle One メンバーシップ上で重複し、システムが矛盾した状態に陥ることが原因と考えられます。
Google One メンバーシップの重複を整理した後、時間の経過をおいても、それで全ての不具合が直るかどうかは分かりません。

<span style="color: red;">**いずれにしろ、Google One メンバーシップに適用する購入特典や有料プランは1つに限定するべきです。**</span>

### ◆ Google One メンバーシップ・不具合解決の最終手段
Google アカウント（<https://myaccount.google.com/>） > データとプライバシー > サービスを削除 > パスワード・PIN入力による本人確認 > 「Google サービスの削除」から「Google One」の情報削除を選択することで、Google One メンバーシップの初期化が可能です。
ただし、Google Oneに関連付けられた情報はすべて削除されるため、Google One メンバーシップに付与されていた購入特典や有料プランも失われます。

**参考サイト**
- **r/GoogleOne｜Reddit**: <https://www.reddit.com/r/GoogleOne/>

---

## ChromeOS Chrome 拡張機能
- **Manifest V2 のサポート タイムライン（サポート終了済み）**: <https://developer.chrome.com/docs/extensions/develop/migrate/mv2-deprecation-timeline?hl=ja>
*(※ コンシューマー版ChromeOSおよびChromeブラウザにおいて、Manifest V2拡張機能のサポートは順次終了・無効化されています。)*
- **Chrome Web Store 拡張機能**: <https://chromewebstore.google.com/category/extensions>

Chrome Web Store外から入手した拡張機能を自分でインストールする場合は、拡張機能ページの右上にあるトグルスイッチを切り替えて**デベロッパーモード**を有効にする必要があります。

### ◆ Tampermonkeyの導入
ブラウザに機能を追加するUserScriptを管理・実行できる無料のブラウザ拡張機能です。
<https://chromewebstore.google.com/detail/tampermonkey/dhdgffkkebhmkfjojejmpbldmpobfkfo>

Tampermonkeyを使用するためには、各拡張機能の内部設定から**ユーザースクリプトを許可する**トグルを有効にする必要があります。
<https://www.tampermonkey.net/faq.php?version=5.3.3&ext=dhdg#Q209>

- **Greasy Fork‐便利で安全なUserScript**: <https://greasyfork.org/ja>

<span style="color: red;">**留意点**</span>
以下のブラウザ拡張機能やUserScriptは、全てをインストールして使用しているわけではありません。ブラウザ拡張機能やUserScriptを入れすぎると競合を起こしてトラブルの原因になるため、数は少なければ少ないほど良いです。

- ブラウザ拡張機能の競合をAdguard Filtersの問題と誤認して報告したIssue
  <https://github.com/AdguardTeam/AdguardFilters/issues/228169>
- Gmail 「システムで問題が発生しました (#2014)
  <https://www.reddit.com/r/techsupport/comments/1b4rocl/oops_the_system_encountered_a_problem_2014/?tl=ja>

  ▶ 断定はできませんが、PhotoShowが原因だった可能性が高く、同様のブラウザ拡張機能でも同じ不具合が起きるかもしれません。

### コンテンツブロック・プライバシー関連
- **AdGuard Extra**
  - URL：<https://github.com/AdguardTeam/AdGuardExtra>
  - 説明：Anti-Adblocker対策用UserScript ‐ 対象サイトはFacebook、Twitchなど
- **AdGuard Browser Extension MV3**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/adguard-%E5%BA%83%E5%91%8A%E3%83%96%E3%83%AD%E3%83%83%E3%82%AB%E3%83%BC/bgnkhhnnamicmpeenaelnjfhikgbkllg?hl=ja)
  - 説明：Chrome 拡張機能 AdGuard Browser Extension MV3 > 後述
- **tinyShield**
  - URL：<https://github.com/List-KR/tinyShield/blob/main/README.ja.md>
  - 説明：Ad-Shield対策用のUserScript ‐ Tampermonkeyで購読して、Manifest V3のフィルタ更新制限を回避する
- **uBlacklist**
  - URL：<https://chromewebstore.google.com/detail/ublacklist/pncfbmialoiaghdehhbnbhkkgmjanfhe>
  - 説明：検索結果のフィルタリング、指定したサイトの検索結果を非表示にする > 後述

### YouTube関連
- **Enhancer for YouTube™**
  - URL：<https://chromewebstore.google.com/detail/enhancer-for-youtube/ponfpcnoihfmfllpaingbgckeeldkhle>
  - 説明：再生速度や音量のマウス制御、画質固定、テーマ変更、コメント非表示などYouTubeの機能を強化する
- **SponsorBlock for YouTube-動画の広告シーンを自動スキップ**
  - URL：<https://chromewebstore.google.com/detail/sponsorblock-for-youtube/mnjggcdmjocbbbhaepdhchncahnbgone>
  - 説明：YouTube動画内のスポンサーセグメントやイントロなどを、ユーザーの報告に基づき自動でスキップする

### ショッピング関連
- **Amazonレビュー信頼度判定 & 無限スクロール（サクラ識別 / 品質チェック）**
  - URL：[Greasy Fork リンク](https://greasyfork.org/ja/scripts/561755-amazon%E3%83%AC%E3%83%93%E3%83%A5%E3%83%BC%E4%BF%A1%E9%A0%BC%E5%BA%A6%E5%88%A4%E5%AE%9A-%E7%84%A1%E9%99%90%E3%82%B9%E3%82%AF%E3%83%AD%E3%83%BC%E3%83%AB-%E3%82%B5%E3%82%AF%E3%83%A9%E8%AD%98%E5%88%A5-%E5%93%81%E8%B3%AA%E3%83%81%E3%82%A7%E3%83%83%E3%82%AF)
  - 説明：Amazonのレビュアー投稿履歴を分析し、信頼度をS〜Dランクで視覚化（サクラ / やらせ / バイアス検出＆詳細レポート）。信頼度フィルタリング機能や、レビュー一覧の無限スクロール化も提供します
- **Condler**
  - URL：<https://chromewebstore.google.com/detail/condler/ejjdbndmmongojeafjlilnchmkppbeap>
  - 説明：Amazon検索結果の左側サイドバーに、価格、人気度、レビューが良い順などの並び替えや、Amazon公式出品のみに絞り込むボタンを追加する
- **Keepa - Amazon Price Tracker**
  - URL：<https://chromewebstore.google.com/detail/keepa-amazon-price-tracke/neebplgakaahbhdphmkckjjcegoiijjo>
  - 説明：Amazon商品の価格履歴グラフをページ上に表示し、設定した価格になると通知を受け取れるようにする
- **サクラチェッカーをAmazon内に直接表示 🔍️**
  - URL：[Greasy Fork リンク](https://greasyfork.org/ja/scripts/533121-%E3%82%B5%E3%82%AF%E3%83%A9%E3%83%81%E3%82%A7%E3%83%83%E3%82%AB%E3%83%BC%E3%82%92amazon%E5%86%85%E3%81%AB%E7%9B%B4%E6%8E%A5%E8%A1%A8%E7%A4%BA)
  - 説明：Amazonの商品ページに、サクラチェッカーのスコアと判定結果を高速で自動表示する

### 検索・ブラウジング補助
- **Buster: Captcha Solver for Humans**
  - URL：<https://chromewebstore.google.com/detail/buster-captcha-solver-for/mpbjkejclgfgadiemmefgebjfooflfhl>
  - 説明：音声認証とAIを活用してreCAPTCHAを自動で突破し、面倒な画像選択の手間をなくして快適なブラウジングを実現する
- **google-search-title-qualified**
  - URL：<https://chromewebstore.google.com/detail/google-search-title-quali/bjcnnhojddnonjmhlpdjcdcfmofliagb>
  - 説明：Google検索結果に、Googleが書き換えたタイトルではなく、サイト本来のタイトルを表示させる
- **simpleGestures**
  - URL：<https://chromewebstore.google.com/detail/simplegestures/flfminafiamnggnldfpilnfnmbgmiegn>
  - 説明：シンプルな設定と使い勝手にこだわったマウスジェスチャー
- **Tabs to Front v2**
  - URL：<https://chromewebstore.google.com/detail/tabs-to-front-v2/iiojfifkpjkhcdjfgekmfobhfdohlecg>
  - 説明：新しいタブを常にフォアグラウンド（最前面）で開く
- **VertiTab - 縦型タブ · AIブラウザエージェント**
  - URL：<https://chromewebstore.google.com/detail/vertitab-vertical-tabs/chejfhdknideagdnddjpgamkchefjhoi>
  - 説明：高度なタブ管理ツール、縦型タブ・ツリー型タブ・スナップショット・クラウド同期・生産性機能を搭載する
- **ブックマークサイドバー**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%B5%E3%82%A4%E3%83%89%E3%83%90%E3%83%BC/jdbnofccmhefkmjbkkdkfiicjkgofkdh)
  - 説明：ブラウザの端に、表示 / 非表示を切り替えられるブックマークサイドバーを追加する

### 特定サイト向け拡張
- **5CH STYLE FORMAT**
  - URL：<https://chromewebstore.google.com/detail/5ch-style-format/aidnencnedgaflbgacmcbcokcpancdac?hl=ja>
  - 説明：5chのスレッド記事の整形、URL直リンク化、画像・レスのPOP表示などにより多機能化する
- **ChatGPT Ctrl + Enter Sender**
  - URL：<https://chromewebstore.google.com/detail/chatgpt-ctrl+enter-sender/gbncgdhklmnckojlibfhdadpfbcdbnch?hl=ja>
  - 説明：ChatGPTなどのAIチャットにおいて、Enterキーを改行、Ctrl + Enterキーを送信に割り当て、誤送信を防ぐ
- **Google Chatの改行・送信キー設定**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/google-chat%E3%81%AE%E6%94%B9%E8%A1%8C%E3%83%BB%E9%80%81%E4%BF%A1%E3%82%AD%E3%83%BC%E8%A8%AD%E5%AE%9A/kabocfciobpmopkcbiphmgdljpdlighk)
  - 説明：Google Chatのメッセージ送信と改行のキー設定をカスタマイズする
- **Shadowban Scanner for Twitter / X**
  - URL：<https://chromewebstore.google.com/detail/shadowban-scanner-for-twi/enlganfikppbjhabhkkilafmkhifadjd>
  - 説明：𝕏のアカウントやツイートのシャドウバン、センシティブ判定を検出する。ろぼいんブログ（<https://roboin.io/>）提供。
- **Twitterᴾˡᵘˢ**
  - URL：[Greasy Fork リンク](https://greasyfork.org/ja/scripts/387969-twitter%E1%B4%BE%CB%A1%E1%B5%98%CB%A2)
  - 説明：オリジナル品質の画像を表示し、スパムツイートの削除機能をカスタマイズする
- **𝕏 Spam Highlighter**
  - URL：<https://github.com/shapoco/x-spam-highlighter>
  - 説明：PC向けWeb版𝕏（旧Twitter）のフォロワー一覧画面で、スパムの疑いがあるアカウント（投資、金配り、出会い系など）を自動で赤くハイライト表示する

### 業務効率化
- **Advanced Font Settings**
  - URL：<https://chromewebstore.google.com/detail/advanced-font-settings/caclkomlalccbpcdllchkeecicepbmbm?hl=ja>
  - 説明：Webサイトのフォント設定を変更する
- **Checker Plus for Gmail™**
  - URL：<https://chromewebstore.google.com/detail/checker-plus-for-gmail/oeopbcgkkoapgobdbedcemjljbihmemj?hl=ja>
  - 説明：Gmailを開かずに新着通知を受け、閲覧・削除・返信を可能にする
- **DeepL翻訳**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/deepl%EF%BC%9Aai%E7%BF%BB%E8%A8%B3%E3%81%A8%E6%96%87%E7%AB%A0%E4%BD%9C%E6%88%90%E3%83%84%E3%83%BC%E3%83%AB/cofdbpoegempjloogbagkncekinflcnj?hl=ja)
  - 説明：高品質なAI翻訳と文章校正を提供する
- **Extensity**
  - URL：<https://chromewebstore.google.com/detail/extensity/jjmflmamggggndanpgfnpelongoepncg?hl=ja>
  - 説明：インストール済みの拡張機能のオン・オフを、ワンクリックで素早く切り替えられる管理ツール
- **Google Keep Chrome 拡張機能**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/google-keep-chrome-%E6%8B%A1%E5%BC%B5%E6%A9%9F%E8%83%BD/lpcaedmchfhocbbapmcbpinfpgnhiddi?hl=ja)
  - 説明：閲覧中のページや選択テキスト、画像をGoogle Keepに素早く保存する
- **Google オフライン ドキュメント**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/google-%E3%82%AA%E3%83%95%E3%83%A9%E3%82%A4%E3%83%B3-%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88/ghbmnnjooekpmoecnnnilnnbdlolhkhi)
  - 説明：Googleドキュメント、スプレッドシート、スライドを、インターネット接続なしで編集できるようにする
- **PhotoShow**
  - URL：<https://chromewebstore.google.com/detail/photoshow/mgpdnhlllbpncjpgokgfogidhoegebod>
  - 説明：Webサイト上のサムネイル画像や画像URLにカーソルを合わせるだけで、高画質な画像を素早く拡大表示する
- **Shortcuts for Google™**
  - URL：<https://chromewebstore.google.com/detail/shortcuts-for-google/baohinapilmkigilbbbcccncoljkdpnd>
  - 説明：1000以上のGoogleサービスへのショートカットを、ポップアップ内にボタンで表示する
- **System Memory Usage**
  - URL：<https://chromewebstore.google.com/detail/system-memory-usage/fdefaodljgbdlmdhobjlechpgpblooeh>
  - 説明：システムのメモリ使用量をツールバーに表示する
- **ドキュメント、スプレッドシート、スライドで Office ファイルを編集**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/%E3%83%89%E3%82%AD%E3%83%A5%E3%83%A1%E3%83%B3%E3%83%88%E3%80%81%E3%82%B9%E3%83%AC%E3%83%83%E3%83%89%E3%82%B7%E3%83%BC%E3%83%88%E3%80%81%E3%82%B9%E3%83%A9%E3%82%A4%E3%83%89%E3%81%A7-off/gbkeegbaiigmenfmjfclcdgdpimamgkj)
  - 説明：Chromeブラウザ上でMicrosoft OfficeのWord、Excel、PowerPointファイルを直接開いて編集できるようにするGoogle公式拡張機能
- **ドライブ用アプリケーション ランチャー（Google）**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/%E3%83%89%E3%83%A9%E3%82%A4%E3%83%96%E7%94%A8%E3%82%A2%E3%83%97%E3%83%AA%E3%82%B1%E3%83%BC%E3%82%B7%E3%83%A7%E3%83%B3-%E3%83%A9%E3%83%B3%E3%83%81%E3%83%A3%E3%83%BC%EF%BC%88googl/lmjegmlicamnimmfhcmpkclmigmmcbeh)
  - 説明：ブラウザから直接、PCにインストールされた対応アプリケーションでGoogle Driveのファイルを開くことができる
- **設定**
  - URL：<https://chromewebstore.google.com/detail/settings/jkfjnjeniglhpiggnfpiombpaohknkie>
  - 説明：Google設定、拡張機能、閲覧データの管理を一元化する
- **素晴らしい画面の並べ替えとスクリーンショット（Awesome Screenshot）**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/%E7%B4%A0%E6%99%B4%E3%82%89%E3%81%97%E3%81%84%E7%94%BB%E9%9D%A2%E3%81%AE%E4%B8%A6%E3%81%B9%E6%9B%BF%E3%81%88%E3%81%A8%E3%82%B9%E3%82%AF%E3%83%AA%E3%83%BC%E3%83%B3%E3%82%B7%E3%83%A7%E3%83%83%E3%83%88/nlipoenfbbikpbjkfpfillcgkoblgpmj)
  - 説明：画面の録画やスクリーンショットのキャプチャを容易にし、録画や画像への注釈追加も可能にする

### 特殊用途
- **Chromebook リカバリ ユーティリティ**
  - URL：[Chrome ウェブストア リンク](https://chromewebstore.google.com/detail/chromebook-%E3%83%AA%E3%82%AB%E3%83%90%E3%83%AA-%E3%83%A6%E3%83%BC%E3%83%86%E3%82%A3%E3%83%AA%E3%83%86%E3%82%A3/pocpnlppkickgojjlmhdmidojbmbodfm?hl=ja)
  - 説明：Chromebookのリカバリメディアを作成するGoogle公式ツール

**参考サイト**
- Kdroidwinがおすすめする chrome拡張機能 Firefox アドオン ユーザースクリプト｜Kdroidwinの日記
  <https://kdroidwin.hatenablog.com/entry/sc>
- Kami-Browser-Add-on｜Kdroidwin
  <https://codeberg.org/Kdroidwin/Kami-Browser-Add-on>

---

## ChromeOS Chrome テーマ
視認性を重視しています
- **Chrome Web Store テーマ**: <https://chromewebstore.google.com/category/themes>

- **Royal Desert Sand**
  - URL：<https://chromewebstore.google.com/detail/royal-desert-sand/nnieplejkjaodhemceganohmdkfekkem>

---

## ChromeOS Chrome アプリ
- **Chrome アプリのサポート終了（順次終了済み）**: <https://support.google.com/chrome/a/answer/15950395?hl=ja>

---

## ChromeOS Android アプリ
- **Google Play アプリ**: <https://play.google.com/store/apps>

- **ChMate***
  - URL：<https://play.google.com/store/apps/details?id=jp.co.airfront.android.a2chMate>
  - 説明：5ちゃんねるを高速・快適に閲覧できるジェスチャーや画像インライン表示、強力なNG機能など、利便性とカスタマイズ性を極めた多機能なAndroid専用ブラウザアプリ
  - *ChromeOSでの不具合は後述*
- **personalDNSfilter***
  - URL：<https://play.google.com/store/apps/details?id=dnsfilter.android>
  - 説明：主にChMateでの広告ブロックを目的とし、副次的にアプリやブラウザのトラッキング・危険サイトをブロックする軽量アプリ
  - *詳細後述*
- **Google Home**
  - URL：<https://play.google.com/store/apps/details?id=com.google.android.apps.chromecast.app>
  - 説明：Google Nest等のスマートデバイスを一元管理し、ルーティンによる自動化や外出先からの遠隔操作で、快適なスマートホーム環境を実現する統合ハブアプリ
- **Google フォト**
  - URL：<https://play.google.com/store/apps/details?id=com.google.android.apps.photos>
  - 説明：写真や動画のクラウド自動バックアップで端末容量を節約し、AI検索や消しゴムマジック等の高度な編集から共有まで可能なGoogle提供の多機能ギャラリーアプリ

---

## Gemini プロンプト
Googleが開発した生成AI「Gemini」は、**プロンプト**（Prompt・指示文）を変えることで多様な「**推論**」が得られます。
しかし、回答は膨大な学習データに基づく「**推論**」であり、必ずしも「**事実**」や「**正解**」ではありません。
そのため、重要な情報は検索エンジンや複数の信頼できる情報源と照らし合わせ、根拠や真偽を確認することが大切です。
生成AIが事実ではない情報を作り出す現象を**ハルシネーション**（Hallucination・幻覚）といいます。
生成AIに回答を断言させるのではなく、「そう判断したソース（情報源）は出せますか？」と聞き返して、<span style="color: red;">**回答を生成するに至った経緯を一次情報とともに提示させる**</span>使い方が安全な場合もあります。

**AdGuard for AndroidとAndroid版Geminiアプリを使う上で必要な措置**
一般設定 > 詳細設定 > ローレベル設定 > AdGuardによる保護 > QUICバイパスパッケージに
`com.google.android.googlequicksearchbox`を追加する。
もしくはアプリの管理からAndroid版Googleアプリを除外する。

**プロンプトによる役割の設定**
一般ユーザーが特別なツールなしで今すぐ実践できるのが、プロンプトによってGeminiの役割を「特化」させる方法です。
これは、対話の冒頭でGeminiに特定の役割を明確に与えることで、特定の目的や知識領域に最適化するテクニックです。
使い方:「あなたは〇〇の専門家です」「〇〇として振る舞ってください」といった形で、具体的な役割を指示します。

**参考サイト**
- これで追いつく！生成AI「Gemini」これだけ知っておけば大丈夫｜🌴 officeの杜 🥥｜Akanemaru氏
  <https://officeforest.org/wp/%e3%80%902025%e5%b9%b4%e5%a4%8f%e3%80%91%e3%81%93%e3%82%8c%e3%81%a7%e8%bf%bd%e3%81%84%e3%81%a4%e3%81%8f%ef%bc%81%e7%94%9f%e6%88%90ai%e3%80%8cgemini%e3%80%8d%e3%81%93%e3%82%8c%e3%81%a0%e3%81%91/>

### ◆ 汎用プロンプト集
実際に使用したプロンプトの例ですが、回答の大まかな方向性は同じであるものの、内容は流動的です。

- **検索 1**: 〜とは？（知りたいことをすぐに検索）
- **検索 2**: 〜の主要な製造メーカーのWebサイトや詳細情報を提供する様々なサイトへのリンクが正常に機能するかどうかを確認し、箇条書きでリストアップしてください
- **検索 3**: 〇〇の✕✕について言及した投稿がないか、GitHubまたはReddit内を詳細に検索し、URLを表示してください（↲改行）URL先にある投稿の内容を分かりやすく箇条書きにして日本語で要約してください
- **画像**: 〜の画像を生成してください（画像の生成には若干時間がかかります）
- **為替**: $〜（USD）は日本円で何円になりますか？
- **計算**: レギュラーガソリンの単価が180円/l、車の燃費が10km/l、走行距離で3000kmを走った場合、燃料代はいくらになりますか？（走行距離 3000km÷燃費 10km/l×レギュラーガソリンの単価 180円/l=燃料代 54,000円）
- **翻訳**: 〜（↲改行）を正しい文法の日本語 or 英語に翻訳してください
- **要約**: 〜（↲改行）について分かりやすく箇条書きで要約してください
- **比較 + 要約**: 〇〇と✕✕の違いについて分かりやすく箇条書きで要約してください
- **分類 + 順列**: 項目を列挙（↲改行）列挙した上記の項目をカテゴリー分けし、 0~9, A~Z順に並べ替えてください
- **文章校正**: 〜（↲改行）この文章を修正後、校正してください
- **事実確認**: 〜（↲改行）この記述は正しいですか？
- **問題解決**: +をクリック → トラブル発生時のスクリーンショットをアップロード or Googleレンズでエラーメッセージを選択してテキストをコピー & ペースト → この問題を解決する方法を教えてください
- **代替提案**: 〜（↲改行）について別のアプローチ方法 or 代替手段はありませんか？
- **ファイル分析**: +をクリック → 分析したいファイルをアップロード → このファイルには悪意のあるコードやマルウェアが含まれていますか？
- **詐欺対策**: サイト名 or ドメインをコピー & ペースト（↲改行）このECサイトは詐欺サイトですか？
- **拡張機能の診断**: Chrome Web Storeの拡張機能インストールページのURLをコピー ＆ ペースト（改行）この拡張機能について、できる限り詳細に調査し、安全性を確認してください
- **価格調査**: 商品購入ページのURLをコピー & ペースト（↲改行）この商品は適正価格ですか？
- **正規表現 1**: 〇〇にマッチする正規表現を作成してください
- **正規表現 2**: 〇〇にマッチして✕✕にはマッチしない正規表現を作成してください
- **正規表現 3**: 作成した正規表現（↲改行）この正規表現の「動作を一切変えず」に、論理的に並べ替えて、ChMateのNG Wordで正しく動作するように調整してください（↲改行）typoや重複などの修正点がないか必ず最終チェックを行ってください

### ◆ パーソナライズ設定
- **パーソナライズ設定: 1**: Google検索で得られた結果を元に回答を作成する。冒頭に要約を表示する。URLがリンク切れしていないか必ず確認する。情報についてはメリットとデメリットの両方を解説する。ソースが検索エンジンのURLである場合、それが検索結果であることを明確に示す。
- **パーソナライズ設定: 2**: ITに関連するプロンプトは、uBlock Origin開発者のRaymond Hill氏、コンテンツブロックフィルタ開発者のYuki2718氏、AdGuard CTO兼共同創設者のAndrey Meshkov氏、AdGuard Filters統括責任者のAlex-302氏、情報セキュリティ・プライバシーのKdroidwin氏、Revanced・Morphe Contributorのkitadai31氏らに質問、回答、結論を査読してもらい、内容の正確性を再確認します。
- **パーソナライズ設定: 3**: AdGuard用には、uBlock Origin用の書き方（`+js`）は使わず、AdGuard専用の書き方（`#%#//scriptlet`）を使用してください。文字を含む要素を消す場合は、`div:has-text(...)`ではなく`:contains(...)`を使用してください。AdGuard for Androidでも軽く動作するように、できるだけシンプルなCSS（`##`）で記述し、どうしても必要な場合のみ、高度なCSS（`#$#`）や拡張機能（`:has`など）を使用してください。

---

## Code Editor

### Visual Studio Code
- **Visual Studio Code: Workspace**
  - HP：<https://vscode.dev/?vscode-lang=ja-jp>
  - GitHub：<https://github.com/microsoft/vscode>
  - 説明：Visual Studio Code: Workspaceは、インストール不要でブラウザから直接利用できる軽量かつ高機能なコードエディタです。

### Visual Studio Code 拡張機能
- **Virtual Gists for Visual Studio Code**
  - HP：<https://marketplace.visualstudio.com/items?itemName=CarloCardella.vscode-virtualgists>
  - GitHub：<https://github.com/carlocardella/vscode-VirtualGists>
  - 説明：Visual Studio Code上でGitHub Gistを直接管理・編集できる拡張機能です。
- **Virtual Git extension pack**
  - HP：<https://marketplace.visualstudio.com/items?itemName=CarloCardella.vscode-virtualgit>
  - GitHub：<https://github.com/carlocardella/vscode-VirtualGit>
  - 説明：手元の端末にGit環境を構築しなくても、ブラウザ上のVS Codeから直接GitHubやGistのファイルを編集・保存できるようになる「便利な道具の詰め合わせパック」です。
- **Virtual Repositories for Visual Studio Code**
  - HP：<https://marketplace.visualstudio.com/items?itemName=CarloCardella.vscode-VirtualRepos>
  - GitHub：<https://github.com/carlocardella/vscode-VirtualRepos>
  - 説明：リモートリポジトリ（GitHub など）をクローン、コミット、プッシュすることなく開いて編集できる Visual Studio Code 拡張機能です。

### Android アプリ
- **QuickEdit Pro**
  - Google Play：<https://play.google.com/store/apps/details?id=com.rhmsoft.edit.pro>
  - Help Center：<https://rhmsoft.com/qedit/help.html>

**■ QuickEdit Proの安全な推奨トークン権限（スコープ）の構成｜GitHub**

▶ GitHubサイト・右上アイコン > Settings > Developer Settings > Personal access tokens > Tokens（classic）

▶ 「repo」「gist」にのみチェックを入れる

### Issues報告
- **Visual Studio Code**: <https://github.com/microsoft/vscode/issues>
- **Virtual Gists for Visual Studio Code**: <https://github.com/carlocardella/vscode-VirtualGists/issues>
- **Virtual Git extension pack**: <https://github.com/carlocardella/vscode-VirtualGit/issues>
- **Virtual Repositories for Visual Studio Code**: <https://github.com/carlocardella/vscode-VirtualRepos/issues>
- **Japanese IME failure on VS Code 1.107.1（Crostini）#285154**: <https://github.com/microsoft/vscode/issues/285154>
  - VS Code 1.107.1（Crostini）における日本語IMEの不具合
  - 計画されていないため閉鎖

*(※ 現在はCrostini（Linux 開発環境）およびVSCodiumをデバイスから削除し、ブラウザとAndroidアプリベースの環境へ完全移行済みです)*

---

## AdGuardユーザールールの作成（個人用途）

### ◆ AdGuardユーザールール作成手順
1. 該当サイト上でデスクトップ版Google Chromeのデベロッパーツール（`Ctrl` + `Shift` + `I`）を開き、ツールバーにあるセレクトアイコンをクリックして、要素の選択に使用する「セレクトモード」を有効にします（[参考](https://willcloud.jp/knowhow/dev-tools-01/#i-3)）。
2. マウスオーバーで非表示にしたい要素にマウスカーソルを移動させ、デベロッパーツールに表示されたDOMツリー上で右クリック >「コピー」>「要素をコピー」を選択します。
3. Geminiのチャット入力欄に該当ページのURLをコピー＆ペーストして（改行）入力します。
4. 同様に「要素をコピー」で選択した要素をペーストして（↲改行）入力します。

**⑤プロンプト作成例**

```text
# 役割設定
あなたはAdGuard Filters（[https://github.com/AdguardTeam/AdguardFilters](https://github.com/AdguardTeam/AdguardFilters)）のフィルタエンジニアで、コンテンツブロックルール作成の専門家です
Webサイトの広告、トラッカー、迷惑要素をブロックするためのルールを、AdGuardの構文（[https://adguard.com/kb/ja/general/ad-filtering/create-own-filters/](https://adguard.com/kb/ja/general/ad-filtering/create-own-filters/)）に沿って提案・作成します

# 行動原則
正確性：サイトの機能を損なう「誤ブロック」を避け、対象のみを的確にブロックします
効率性：パフォーマンスへの影響を最小限に抑える、最もクリーンで効果的なルールを選択します
解説：なぜそのルールが有効なのか、どのような仕組みで機能するのかを必ず説明します

# タスク
この要素を解析してページの構造変更に最も強い汎用的なCSS セレクターを抽出し、「Chrome 拡張機能 AdGuard Browser Extension MV3」or「AdGuard for Android」で使用できるAdGuardユーザールールを作成してください
「ネットワークルール」「強力な修飾子（Modifiers）」「拡張CSSセレクター」「Scriptletルール」は、効果が確実かつ安全な場合にのみ提示してください
ネットワークルールを提示する時は、適用範囲を最小限に抑えるために、修飾子（Modifiers）の「$domain」を付けられないかを必ず確認してください

# 最後の確認
ルールを出力する前に、「これはAdGuardで本当に動く書き方か？ uBlock Origin用になっていないか？」と一度チェックしてください

# 出力形式
コードスニペットを必ず含めて、マウスのワンクリックでコピー ＆ ペーストできるようにしてください

# 出力書式
[Adblock Plus 2.0]
! Title: My Filter List Name
! Description: 具体的な用途や説明（例: 日本のサイト向け広告ブロックルール）
! Version: 1.0.0
! Last modified: 2026-01-18T16:15:00+09:00
! Expires: 2 days（または 48 hours）
! Homepage: [https://github.com/your-username/repo](https://github.com/your-username/repo)
! License: CC0 1.0 Universal
!
! ここからルールを記述
||example.com^
example.com##selector

# サイトのURL

# htmlソースコード
```
上記をコピー ＆ ペーストして➤をクリックします。

6. 生成されたAdGuardユーザールールを登録し、該当サイト上で動作確認をします。
7. 生成されたAdGuardユーザールールが意図した動作をしない時は、生成されたAdGuardユーザールールをGeminiの入力欄にペーストして（↲改行）、プロンプトにルールの動作のフィードバックをしてルールを再生成し、AdGuardユーザールールに登録して動作確認を繰り返します。

▶ 生成AIはフィルタエンジニアの代替にはならないので、AdGuard Filters Issuesへの報告（<https://github.com/AdguardTeam/AdguardFilters/issues>）が最善です。
- 月間トラフィック量が100,000未満のWebサイトは対処されない場合があります。
▶ AdGuard Filters Issues reporting toolやGitHubのコメント欄では、Markdown記法（<https://qiita.com/oreo/items/82183bfbaac69971917f>）が使用できます。

### ◆ 作成したAdGuardユーザールールの整理
作成したAdGuardユーザールールをコピー & ペースト（↲改行）

```text
# タスク
これらのAdGuardユーザールールを、「動作を一切変えずに」ドメインのヘッダーごとに整理し、論理的な並びになるようにしてください
疑わしいドメインも削除せず、AdGuardユーザールールを正確に整理してください
特定のルールをコメントアウトして無効にしないでください
重複したルールは削除してください

# 出力形式
以下の書き方を厳守してください
コードスニペットを必ず含めて、マウスのワンクリックでコピー ＆ ペーストできるようにしてください
ドメインが変わる時は1行空けてルールを記述してください
同ドメイン内でフィルタのカテゴリーが変わる時は、空行を詰めてルールを記述してください
必要：! example.com
必要：! フィルタのカテゴリー
不要：! ----------------------------------------------------------------------
```

### ◆ AdGuardユーザールールの変換
uBlock Origin用のルール「`##+js(" スクリプトレット名, 引数 ")`」をコピー & ペースト（↲改行）

```text
# タスク
uBlock Origin用に書かれた上記のルール（[https://github.com/gorhill/uBlock/wiki/Resources-Library](https://github.com/gorhill/uBlock/wiki/Resources-Library)）をAdGuard Browser Extension MV3で全く同様に動作するScriptletルール（[https://github.com/AdguardTeam/Scriptlets/blob/master/wiki/about-scriptlets.md](https://github.com/AdguardTeam/Scriptlets/blob/master/wiki/about-scriptlets.md)）に変換してください
動作の完全な再現が不可能な場合、ルールの変換は一切行わず「変換不可能」と回答してください

# 出力形式
コードスニペットを必ず含めて、マウスのワンクリックでコピー ＆ ペーストできるようにしてください
```
▶ Scriptletルールは、完全に互換性がある形で生成されるとは限らないため、動作の確認が不可欠です。
▶ 基本的に生成AIはScriptletルールの作成が苦手なので、AdGuard Filters Issuesへ報告（<https://github.com/AdguardTeam/AdguardFilters/issues>）するのが最善です。

### ◆ 不具合を起こすAdGuardユーザールールの修正・削除
不具合を起こすAdGuardユーザールールをコピー & ペースト（↲改行）

```text
# タスク
これらのAdGuardユーザールールの中に、「〇〇：不具合の発生箇所」で「✕✕：不具合の内容」という不具合を引き起こすルールが含まれている可能性があります
「# サイトのURL」と「# htmlソースコード」を参照して、不具合を起こす可能性のあるルールを特定し、修正してください
修正できない場合は「修正不可」と回答したうえで削除してください
正常に動作する他のAdGuardユーザールールは「# 出力形式」に従って記述してください

# 出力形式
以下の書き方を厳守してください
コードスニペットを必ず含めて、マウスのワンクリックでコピー ＆ ペーストできるようにしてください
ドメインが変わる時は1行空けてルールを記述してください
同じドメイン内でフィルタのカテゴリーが変わる時は行を空けずに詰めてルールを記述してください
必要：! example.com
必要：! フィルタのカテゴリー
不要：! ----------------------------------------------------------------------

# サイトのURL

# htmlソースコード
```

**● Google スプレッドシートを用いたAdGuardユーザールールの整理**
データ タブ > データ > シートを並べ替え > 列xを基準に昇順でシートを並べ替え > ルールを0~9, A~Z順にする。
データ > データ クリーンアップ > 重複を削除 > ルールの重複を削除。

---

## UserScriptの作成（個人用途）
AdGuardユーザールールで期待する動作が得られない場合、GeminiのプロンプトをUserScript作成用に切り替えると、動作するUserScriptを作成してくれることがあります。

```text
# 役割設定
あなたは、Greasy Fork（[https://greasyfork.org/ja](https://greasyfork.org/ja)）やGitHubで高評価を得ているJavaScript開発者であり、ブラウザ拡張機能（Tampermonkey / Violentmonkey）向けのUserScript作成の専門家です

# タスク
プロンプトを随時作成

# 出力形式
すぐにコピー＆ペーストして使える完全なJavaScriptコード（UserScriptメタデータブロックを含む）

# 出力書式
// ==UserScript==
// @name         My Useful Script
// @namespace    [http://tampermonkey.net/](http://tampermonkey.net/)
// @version      0.1
// @description  スクリプトの説明をここに書く
// @author       あなたのお名前
// @match        [https://www.google.com/](https://www.google.com/)*
// @updateURL    [https://example.com/script.user.js](https://example.com/script.user.js)
// @downloadURL  [https://example.com/script.user.js](https://example.com/script.user.js)
// @icon         [https://www.google.com/s2/favicons?sz=64&domain=google.com](https://www.google.com/s2/favicons?sz=64&domain=google.com)
// @grant        none
// @run-at       document-idle
// ==/UserScript==

# サイトのURL
 
# HTMLソースコード
```

### ◆ AdGuardユーザールールをUserScriptに変換
作成したAdGuardユーザールールをコピー & ペースト（↲改行）

```text
# タスク
このAdGuardユーザールールをUserScriptに変換してください

# 出力形式
すぐにコピー＆ペーストして使える完全なJavaScriptコード（UserScriptメタデータブロックを含む）
```

---

## 主要な生成AI
- **ChatGPT**: 汎用性が高い <https://chat.openai.com/>
- **Grok**: 汎用性 + 制限が緩い <https://grok.com/>

  ▶ 𝕏の投稿の信憑性をチェックするのに使えそう？
- **GitHub Copilot**: コーディング用 <https://github.com/features/copilot>
- **z.ai GLM-4.5**: 無料でそこそこの性能・ローカルで動かせる <https://chat.z.ai/>
- **SDXL**: 狙い撃ち・人物や複雑な構図の生成で優秀 <https://stablediffusionweb.com/>

**出典**
- mondで自分が提出した質問の回答: <https://mond.how/ja/topics/iozm87r4wyxx8ao/amp4bswp4hi8d0m>

---

## Web サービス

### 広告・セキュリティ・環境確認
- AdBlock Tester：<https://adblock-tester.com/>
- AdGuard > サポートセンター：<https://adguard.com/ja/support.html>
- AdGuard Status：<https://status.adguard.com/>
- AdGuard 診断ページ：<https://adguard.com/ja/test.html>
- AI性チェッカー：<https://ai-tool.userlocal.jp/x_llm_match>
- Eylenburg's Tech Website：<https://eylenburg.github.io/>
- Google あなたに関する検索結果：<https://myactivity.google.com/results-about-you>
- Norton Safe Web：<https://safeweb.norton.com/>
- Octane 2.0 plus：<https://octane.webmarks.info/ja/>
- Statcounter：<https://gs.statcounter.com/>
- Test Ad Block - Toolz：<https://adblock.turtlecute.org/>
- Webサイトをチェック：<https://reports.adguard.com/ja/welcome.html>
- Xranks：<https://xranks.com/ja/>
- インターネット回線スピードテスト・通信速度測定 | USEN GATE 02：<https://speedtest.gate02.ne.jp/>
- 確認君+（Plus）：<https://env.b4iine.net/>

### サービス稼働状況・公式サポート
- 5chサーバ稼働状況：<https://www.kyodemo.net/sdemo/k/5_?hs=1>
- Chromebook ヘルプ：<https://support.google.com/chromebook/?hl=ja#topic=>
- Downdetector：<https://downdetector.jp/>
- GitHub Status：<https://www.githubstatus.com/>
- Google Pixel ヘルプ：<https://support.google.com/pixelphone/?hl=ja#topic=>
- Google Workspace ステータス ダッシュボード：<https://www.google.com/appsstatus/dashboard/#hl=ja&v=status>
- Google ヘルプ：<https://support.google.com/?hl=ja>
- Imgur Removal Request：<https://imgur.com/removalrequest>
- 𝕏・バグ報告・ご要望：<https://x.com/i/communities/1841382313667723737>
- Yahoo!リアルタイム検索：<https://search.yahoo.co.jp/realtime/>
- オンライン手続きサポート：<https://tetsuduki-support.docomo.ne.jp/>
- サイトはダウンしている？：<https://www.websiteplanet.com/ja/webtools/down-or-not/>
- 偽 SPARROW AIM-7P Ver.1.00：<https://5ch.ape.jp/SPARROW/>

### 画像・動画・ファイル編集・共有
- 123apps：<https://123apps.com/ja/>
- AddYoutube.com：<https://addyoutube.com/>
- ezyZip：<https://www.ezyzip.com/ja.html>
- Fotoramio：<https://fotoram.io/jp>
- GigaFile便：<https://gigafile.nu/>
- Gofile：<https://gofile.io/home>
- iLoveIMG：<https://www.iloveimg.com/ja>
- imgur Upload：<https://imgur.com/upload>
- VRSNS風ロゴジェネレーター：<https://logo-bzr.pages.dev/>
- YouTubeMP3もどき：<https://receive.shamimomo.net/YouTubeMP3modoki/>

### テキスト作成・情報・その他
- Dillinger：<https://dillinger.io/>
- innovaTopia：<https://innovatopia.jp/>
- mond：<https://mond.how/>
- Redact：<https://redact.dev/>
- Sundry Street：<https://sundryst.com/>
- Writebox：<https://write-box.appspot.com/>
- Writening：<https://writening.net/>
- Xポスト性格診断：<https://ai-tool.userlocal.jp/x_shindan>

---

## セキュリティ・プライバシー・匿名性の違い
- **セキュリティ**：鍵のかかった檻の中に手紙がむき出しで入っている。檻を開けたり壊したりはできないが、手紙の内容は見える（手紙の物理的な盗難を防止）
- **プライバシー**：手紙は段ボール箱の中にある。手紙は封筒に入っているため内容は見えないが、段ボール箱を開けたり壊したりはできる（手紙の内容の機密性）
- **匿名性**：手紙は公開されているが、誰が書いたのか、誰宛てなのかは分からない（手紙の差出人と受取人の秘匿性）

▶ セキュリティとプライバシーは別物である。

▶ セキュリティが高くてもプライバシーが守られているとは限らない。

---

## 特殊詐欺対策
**！警察庁・SOS47特殊詐欺対策ページ**

<https://www.npa.go.jp/bureau/safetylife/sos47/>

**成りすまし・その他の特殊詐欺**
警察官、医師、弁護士、自治体職員などを名乗る電話やLINEでの個人情報の聞き取り・金銭の要求は、特殊詐欺の可能性が極めて高いです。
日本では、公的機関や企業が重要な連絡・手続きを電話やLINEのみで行うことは通常ありません。
還付金詐欺、サポート詐欺、当選詐欺、企業の音声案内を装う手口が典型例です。
安易に金銭を支払ったり個人情報を教えたりせず、スパムフィルタ導入などの対策を取り、まずは詐欺を疑ってください。

**SNSの投資・ロマンス型詐欺**
SNSでは短期間で高収入を得られる副業や闇バイトの勧誘が多いです。
今後、生成AIによる著名人の偽画像・音声・動画を使った投資詐欺やロマンス詐欺が増加すると予想されます。
LINEなどへの誘導や不審な勧誘に安易に応じず、情報源を十分に確認するなど、一層の注意が必要です。

**！日本電話番号検索**

<https://www.jpnumber.com/>

**注意が必要な特殊な電話番号**
1. `+` で始まる or `+ 81 -` → 国際電話で折り返し電話をすると高額な通話料や利用料が発生する場合があります
2. 末尾が `- 0110` → 警察署の番号を装った詐欺電話の可能性があります
3. `0120 -` or `0800 -` → 電話を受けた側（フリーダイヤルの契約者）が通話料を全額負担します
4. `050 -` → IP電話の番号を悪用した迷惑電話である可能性があります
5. `0570 -` → ナビダイヤルの通話料は、発信者（電話をかけた側）が全額負担します
6. `0180 -` → 情報料として通話料とは別に料金が発生します

**フィッシング詐欺**
フィッシング詐欺では、常に疑う意識が不可欠です。
SMSやメールで利用規約確認やパスワード更新の通知が来ても、本文中のURLはクリックせず、ログインは公式アプリ経由、または正規サイトをブックマーク登録し、パスワードマネージャーを使いアクセスしましょう。
不審な点があれば、正規サイトのサポートに問い合わせ、2段階認証やパスキーを設定してください。

**悪質なECサイト**
支払い方法が銀行振込のみのサイトや、商品未開封でも返品時にキャンセル料が発生するECサイトは、詐欺寄りの悪質サイトの特徴とのことです。

**SEOポイズニング**
ログインやECサイト利用時にGoogleなどの検索エンジンの検索結果を経由する癖をつけていると、SEOポイズニングの餌食になる可能性があります。
SEOポイズニングとは、SEO技術を悪用し、不正サイトを検索結果上位に表示させて、ユーザーをマルウェア感染や詐欺サイトに誘導するサイバー攻撃です。

ブラウジング中にコンテンツブロッカーを使うことで、特殊詐欺に遭う確率を大幅に下げることができるので、多層防御の1つに加えてもよいかと思います。
個人的に特殊詐欺に遭う確率を最小限に抑えることを最優先事項にしているので、広告を非表示にするサブスクリプションの利用も考慮しています。

**参考サイト**
- Kdroidwin氏が記事を寄稿している詐欺サイト対策 Wiki*：  <https://wikiwiki.jp/antiscamsite/>
- おたくま経済新聞｜【特集】STOP！ネット詐欺！：  <https://otakuma.net/category/internet/internet-scam>
- SEOポイズニングとは？仕組みや対策をわかりやすく解説：  <https://www.lanscope.jp/blogs/cyber_attack_cpdi_blog/20240530_20684/>

---

## AdGuard 公式フィルタ
組み込みフィルタリスト・標準フィルタリストと呼ばれることが多いです。

<https://adguard.com/kb/ja/general/ad-filtering/adguard-filters/>

Yuki2718氏のよくある質問（<https://github.com/Yuki2718/adblock2/wiki/よくある質問>）より引用：
> **Q 4-8：**
> uBlock Origin以外のブロッカー（PC）でおすすめのフィルタ構成を教えてください。

> **A 4-8：**
> AdGuardでは組込みのフィルタを使っていただくのが無難と思います。AdGuardはuBlock Origin文法の大部分をサポートしていることになっていますが、実際は仕様の違いにより効かなかったり、動作が異なったりすることもあり、そうした細かい仕様は公式ドキュメントに必ずしも載っていません。当然ですが、AdGuardのフィルタはAdGuard上で完璧に動作します4-9。AdGuard日本語フィルタはかつて不評でしたが、今では昔と別物といってよいほど精度が高くなっています。

**コンテンツブロックフィルタ**
- **AdGuard 公式フィルタ**：AdGuardの接頭語 or `#recommended`のタグが付く各種フィルタ + 日本語フィルタ
- **Online Malicious URL Blocklist**：uBlock Origin ＆ AdGuardの標準セキュリティフィルタ
- **uBlock Origin – Badware risks**：Yuki2718氏がフィルタの監修に関わっています

※ Chrome 拡張機能 AdGuard Browser Extension MV3の静的ルールの上限は330,000です。

**カスタムフィルタ・ユーザールール**
- **AdGuard Japanese filter Plus**：Yuki2718氏自身がフィルタの監修をしています
- **AdGuard module - not for independent use**：上記フィルタのmodule

ユーザールールは、各フィルタ作者様のルールを参考にしたり、自作のルールと組み合わせたりして作成しています。

**DNSフィルタ**
- **AdGuard for Android**：DNS通信を保護 > DNSフィルタ > AdGuard DNS filter

**例外ルール**
サイトの機能やAndroidアプリの動作を阻害するルールを例外（`@@`）にすることが多いです。

**AdGuardユーザールール作成ガイド**
- なんJ AdGuard部 Wiki* > フィルタ構文：<https://wikiwiki.jp/nanj-adguard/%E3%83%95%E3%82%A3%E3%83%AB%E3%82%BF%E6%A7%8B%E6%96%87>
- AdGuard-自分の広告フィルタを作成する方法：[リンク](https://adguard-com.translate.goog/kb/ja/general/ad-filtering/create-own-filters/?_x_tr_sl=en&_x_tr_tl=ja&_x_tr_hl=ja&_x_tr_pto=wapp)
- AdGuard - DNS filtering rules syntax：[リンク](https://adguard--dns-io.translate.goog/kb/ja/general/dns-filtering-syntax/?_x_tr_sl=en&_x_tr_tl=ja&_x_tr_hl=ja&_x_tr_pto=wapp)

### Issues報告
AdGuardでの広告ブロック漏れ、Anti-Adblock Scriptによるコンテンツブロッカー検出、コンテンツブロックフィルタの誤ブロックといったフィルタ関連の不具合は、以下のいずれかの方法でIssueを作成して報告してください。
▶ AdGuard for AndroidにおけるFilter Issuesは、HTTPSフィルタリングの使用が前提となって対処されます。

詳細な検証にはブラウザのデベロッパーツールが使えます。
- 概要｜Chrome DevTools｜Chrome for Developers：<https://developer.chrome.com/docs/devtools/overview?hl=ja>
- ブラウザーの開発者ツールとは｜MDN：<https://developer.mozilla.org/ja/docs/Learn_web_development/Howto/Tools_and_setup/What_are_browser_developer_tools>
- ウェブ開発の学習 | MDN：<https://developer.mozilla.org/ja/docs/Learn_web_development>

**報告用Webサイト**
- AdGuard Filters Issues reporting tool：<https://reports.adguard.com/ja/new_issue.html>
- Webサイトやアプリでの問題を報告する方法：<https://adguard.com/kb/ja/guides/report-website/>
- AdGuard Filters Issues：<https://github.com/AdguardTeam/AdguardFilters/issues>

Issues報告はGitHubアカウントがなくても可能ですが、アカウントがあると編集が可能になります。
報告時に重要となるのは「**問題が発生するサイトのURL**」「**問題の再現手順**」「**問題発生時のスクリーンショット**」「**ロガーのスクリーンショット**」です。

GitHubでのやり取りは基本的に英語ですが、Google翻訳やDeepL翻訳（<https://github.com/AdguardTeam/AdguardFilters/issues/217897>）の活用をおすすめします。

**Issues報告・補足**
- AdGuardフィルタポリシー：<https://adguard.com/kb/ja/general/ad-filtering/filter-policy/>
- AdGuard Sitereport website：<https://github.com/AdguardTeam/ReportsWebApp>

---

## Chrome 拡張機能 AdGuard Browser Extension MV3
- **Chrome Web Store**：[リンク](https://chromewebstore.google.com/detail/adguard-%E5%BA%83%E5%91%8A%E3%83%96%E3%83%AD%E3%83%83%E3%82%AB%E3%83%BC/bgnkhhnnamicmpeenaelnjfhikgbkllg)
- **HP**：<https://adguard.com/ja/adguard-browser-extension/overview.html>
- **GitHub**：<https://github.com/AdguardTeam/AdguardBrowserExtension>

Chrome 拡張機能 AdGuard Browser Extension MV3を使用するためには、拡張機能の内部設定から**ユーザースクリプトを許可する**トグルを有効にする必要があります。

Chrome 拡張機能 AdGuard Browser Extension MV3 v5.2.400以降、拡張機能と組み込みのフィルタリスト + カスタムフィルタは、「ツールバーのアイコン > 右上ポップアップの↻」または「フィルタ > ↻アップデートを確認する」から最新状態を確認できます。

※ ポップアップメニューの更新ボタンや、Chromeの拡張機能管理画面での「更新ボタン↻」では、カスタムフィルタの再読み込みがトリガーされないケースが報告されています。
- MV3 extension - Custom filters do not update when a new version of AG MV3 is available #2944
  <https://github.com/AdguardTeam/AdguardBrowserExtension/issues/2944>
- Add ability to update custom filters in MV3 #3016
  <https://github.com/AdguardTeam/AdguardBrowserExtension/issues/3016>

- **AdGuard ブラウザ拡張機能 MV3対応版**: <https://adguard.com/kb/ja/adguard-browser-extension/mv3-version/>

### ◆ カスタムフィルタで購読する場合
`AdGuard module - not for independent use`は、`AdGuard Japanese filter Plus`のサブリストとして自動的にincludeされます。

### ◆ ユーザールールにルールを全コピー & 全ペーストする場合
`AdGuard Japanese filter Plus`と`AdGuard module - not for independent use` の両方のフィルタのルールを全コピー & ペーストする必要があります。

### ! カスタムフィルタ・ユーザールール
- **AdGuard Japanese filter Plus**：  <https://yuki2718.github.io/adblock2/japanese/jpf-plus.txt>：
- **AdGuard module - not for independent use**：<https://yuki2718.github.io/adblock2/japanese/jpfp-ag.txt>

**参考サイト**
- Yuki2718 / adblock2 > AdGuard Japanese filter Plus

  <https://github.com/Yuki2718/adblock2>

### ◆ 開発者ツールと連動した手動ブロック機能
Chrome 拡張機能 AdGuard Browser Extension MV3には開発者ツールと連動した手動ブロック機能（uBlock Originの要素選択モードに相当）が搭載されています（<https://imgur.com/DcEH4K4>）。
作成したルールはユーザールールに格納されます。

### ◆ Chromeのアドレスバーから新しいタブでユーザールールを開く
Chromeのアドレスバーに以下のURLをコピー & ペーストして移動します。
`chrome-extension://bgnkhhnnamicmpeenaelnjfhikgbkllg/pages/fullscreen-user-rules.html?theme=system`

**参考サイト**
- はちまブログ > uBlock Origin:

<https://hachima25.hatenablog.com/archive/category/uBlock%20Origin>
- r/uBlockOrigin｜Reddit > solutions > youtube:

<https://www.reddit.com/r/uBlockOrigin/wiki/solutions/youtube/>
- r/uBlockOrigin｜Reddit > solutions > twitter:

<https://www.reddit.com/r/uBlockOrigin/wiki/solutions/twitter/>
- YouTube Fix & Customizations｜Reddit:

 <https://www.reddit.com/r/youtube/comments/1b40hra/youtube_fix_customizations_4_videos_per_row/>
- White area on Youtube｜Reddit: 

<https://www.reddit.com/r/uBlockOrigin/comments/1l4r84i/white_area_on_youtube/>
- 𝕏/Twitter ルール作り資料｜uBlockOrigin > uAssets: 

<https://x.com/Red_Frame_X/status/2010925824636252329>

### ◆ Web版YouTubeについての留意点
YouTube Anti-Adblock回避ルールは、uBlock Origin開発チームの解析を参考にAdGuardが開発・調整しています。
YouTube Premium未加入者がカスタムフィルタや拡張機能を使いすぎると、YouTubeのAnti-Adblock Scriptに検知されやすくなります。
uBlock OriginやAdGuardでYouTubeを無料利用する際は、公式ルールのみの使用が推奨されます。

- 🟥[uBO only] ALL YouTube issues: D-O-N-'T COMMENT till 100% read... #27415
  <https://github.com/uBlockOrigin/uAssets/issues/27415>
- 🟥[uBO LITE only] ALL YouTube issues: D-O-N-'T COMMENT till 100% read... #28707
  <https://github.com/uBlockOrigin/uAssets/issues/28707>

Chrome 拡張機能 **Enhancer for YouTube™**を使う場合、Web版YouTubeのUIを調整するユーザールールのいくつかは不要になります。

---

## Chrome 拡張機能 uBlacklist
- **Chrome Web Store**：[リンク](https://chromewebstore.google.com/detail/ublacklist/pncfbmialoiaghdehhbnbhkkgmjanfhe)
- **HP**：<https://iorate.github.io/ublacklist/ja/docs>
- **GitHub**：<https://github.com/iorate/ublacklist>

uBlacklistは、Googleなどの検索結果から指定したWebサイトを非表示にするChrome 拡張機能です。正規表現ルール、クラウドストレージによる設定同期、公開ブラックリストの購読などの機能も利用できます。

### ! ブラックリストを追加する
- **ncaq-uBlacklistRule**: <https://raw.githubusercontent.com/ncaq/uBlacklistRule/master/uBlacklist.txt>

```text
検索結果の非表示ルール
*://*[.example.com/](https://.example.com/)*
/example\.(net|org)/
title/Example Domain/

例外ルール（検索結果の再表示ルール）
@*://*[.example.com/](https://.example.com/)*
```

**Issues報告 / 参考サイト**
- uBlacklist Issues：<https://github.com/iorate/ublacklist/issues>
- uBlacklistRule Issues：<https://github.com/ncaq/uBlacklistRule/issues>
- コミュニティルールセット｜uBlacklist：<https://ublacklist.github.io/ja/rulesets>

---

## Android アプリ personalDNSfilter（ChromeOS）
- **Google Play**：<https://play.google.com/store/apps/details?id=dnsfilter.android>
- **HP**：<https://www.zenz-solutions.de/personaldnsfilter-wp/>
- **GitHub**：<https://github.com/IngoZenz/personaldnsfilter>
- **FAQ**：<https://www.zenz-solutions.de/faq/>

### ◆ personalDNSfilter（ローカルVPNモード）を安定して稼働させるための設定
※ ChromeOS内蔵のAndroid OSには「アプリのバッテリー使用量」の設定項目がありません。
- Androidのステータスバー：personalDNSfilter通知右上⚙を押して、**通知をデフォルトからサイレント**に変更する
- AndroidのVPN設定で**personalDNSfilterの「常時接続VPN」を有効**にする
- VPNの接続が不安定な時は、**「VPNプロファイル」を一度削除し、再設定する**
- Androidのネットワーク設定で**「プライベートDNS」を無効**にする
- Androidのネットワーク設定で**「接続の自動調整」を必要に応じて無効**にする
- ブラウザの設定にある**「セキュアDNSを使用」を無効**にする

※ personalDNSfilterは、日本語インターフェース上でDNSブロックリストやhostsファイルを総称して「フィルタ」と表現していますが、その実態はDNSブロッカーです。そのため、uBlock OriginやAdGuard Browser Extensionなどで使用されるABP形式の構文には対応していません。

### ! 購読済みのDNSブロックリスト・hostsファイル
- **HaGeZi's Pro DNS Blocklist**

  <https://cdn.jsdelivr.net/gh/hagezi/dns-blocklists@latest/wildcard/pro-onlydomains.txt>

**Issues報告 / 参考サイト**
- personalDNSfilter Issues: <https://github.com/IngoZenz/personaldnsfilter/issues>
- HaGeZi's DNS Blocklists: <https://github.com/hagezi/dns-blocklists>
- oisd｜domain blocklist: <https://oisd.nl/>
- StevenBlack / hosts: <https://github.com/StevenBlack/hosts>
- sebsauvage.net hosts blocklist: <https://sebsauvage.net/wiki/doku.php?id=dns-blocklist-en>

---

## Android アプリ 有償版 AdGuard for Android（Android）
- **HP**：<https://adguard.com/ja/adguard-android/overview.html>
- **GitHub**：<https://github.com/AdguardTeam/AdguardForAndroid>

### ◆ AdGuard for Android（ローカルVPNモード）を安定して稼働させるための設定
- 設定 > アプリ > すべてのアプリ > AdGuard > アプリのバッテリー使用量 > **バックグラウンドでの使用を許可** > **制限なし**
- Androidのステータスバー：AdGuard for Android通知右上⚙を押して、**通知をデフォルトからサイレント**に変更する
- AndroidのVPN設定で**AdGuard for Androidの「常時接続VPN」を有効**にする
- VPNの接続が不安定な時は、**「VPNプロファイル」を一度削除し、再設定する**
- Androidのネットワーク設定で**「プライベートDNS」を無効**にする
- Androidのネットワーク設定で**「接続の自動調整」を必要に応じて無効**にする
- ブラウザの設定にある**「セキュアDNSを使用」を無効**にする

AdGuard for Android v4.x以上のUIは、設定へのアクセスが分かりにくいという課題があります。
⚙ > 一般設定 > 詳細設定 > ローレベル設定 >（最下部）その他の設定 - 「メイン画面にデベロッパーツールを表示する」
これをONにすると、ホーム画面の右上にレンチとマイナスドライバーを交差させたアイコンが表示されます（<https://imgur.com/UKGTVnZ>）。

### HTTPSフィルタリング
Android版Chromeなどのブラウザで高精度なコンテンツブロックを行うには、HTTPSフィルタリングを有効にする必要があります。
有効化すると、AdGuardは暗号化通信を一時解析し、広告や不要要素をブロックします。

<span style="color: red;">**留意点**</span>
通信の復号を許可するという性質上、AdGuard社に対する根本的な信頼が前提となります。長年の実績があるツールですが、強力な権限を与えることに不安を感じる場合は、HTTPSフィルタリングをOFFにした状態でもAdGuardを利用することは可能です（[参考](https://mond.how/ja/topics/2e44jvg4wahf54j/oupbjuuxjlg4tjl)）。
金融・決済系アプリをフィルタリング除外設定にしたり、「仕事用プロファイル」に隔離して運用するのも一つの手です。

### DNS通信を保護 > DNSフィルタ
AdGuard DNS filterによるDNSブロックは、ドメインレベルでのブロックしかできませんが、ブロック範囲がシステム全体に及ぶという特徴があります。

プライバシー関連のルールをAdGuard DNS（filter）で厳格にブロックすると、不具合の原因になることがあります。この問題を緩和する方法には以下の3種類があります。

1. **AdGuard_DNS_Filter_for_myself**に切り替える：<https://github.com/monsivamon/AdGuard_DNS_Filter_for_myself>
2. **AdGuard DNSフィルタ（プライバシー抜き）**に切り替える：<https://github.com/kitadai31/AdGuardSDNSFilter_withoutPrivacyFilters>
3. **DNSユーザーフィルタ**：プライバシー関連のルールを例外（`@@`）にするDNSユーザーフィルタを自分で作成する

### DNSサーバー
AdGuard for Androidで設定するDNSは、自動DNSか、障害に強く高速なGoogle Public DNSが推奨されます。なお、Android端末の「プライベートDNS」とAdGuard for Androidの「DNS通信を保護」は併用できません。

- **ChromeOSで行う追加設定**: 設定 > ネットワーク > Wi-Fi > ルーター > ネットワーク > ネームサーバー > Google ネーム サーバー（[参考](https://developers.google.com/speed/public-dns/docs/using?hl=ja#chromeos)）

### トラブルシューティング
不具合に万全を期すには、AdGuard for Androidをクリーンインストールし、再セットアップしてから端末を再起動する必要があります。

- モバイル回線の通信には異常はないが、Wi-Fiに接続すると接続不良を起こす: `IPv6フィルタリングをOFFにする` と解消されることがあります。
- フィルタが自動更新されない: ホーム画面右上↻（Reload）をタップして手動更新するのが一番楽な対処法です。

**Issues報告**
- AdGuard for Android Issues: <https://github.com/AdguardTeam/AdguardForAndroid/issues>
- AdGuard Japanese filter Plus Issues: <https://github.com/Yuki2718/adblock2/issues>

---

## HTTPSフィルタリング・DNSフィルタリング
AdGuard製品に採用されている、2種類のフィルタリング方式の特性について簡潔にまとめます。

- **HTTPSフィルタリング：**
  通信の中身（HTTPSで暗号化されたトラフィック）を、ユーザ端末にルート証明書をインストールし、端末内で復号 / 検査 / 必要なら改変（広告・トラッカー除去）し、再暗号化して送信する方式です。
- **DNSフィルタリング：**
  ドメイン名（DNSリクエスト）レベルで、不適切とされるドメインへの名前解決をブロックまたは別の応答にリダイレクトする方式です。処理が軽く高速に動作しやすい一方で、ページ内要素単位での細かな制御はできません。

---

## 【解決済み】Android System WebView 問題
**概要**
AdGuard for Android v4.7.1以上に実装されたプライベートブラウザが原因で、Android System WebViewの更新・アンロード後にAdGuard for Androidが連動して終了し、自動再起動・再保護の開始に失敗する現象が確認されていました。

**対処法**
これらは「対処法」であり「完全な解決策」ではありません。
1. AdGuard for Androidをv4.6.5以下のバージョンにダウングレードする
2. AdGuard for Android v4.7.1〜v4.9のバージョンでウォッチドッグ機能を有効にする
3. タスク自動化アプリのMacroDroidを利用して、AdGuard for Androidの起動状況を常時監視して自動再起動・再保護を開始させるタスクを作成する（最も効果的）

**結論**
Android System WebViewの影響によるローカルVPN切断の解決策は、AdGuardを**v4.10以降のバージョンへアップデートすること**です。v4.10で関連する不具合は修正されました。

---

## Android アプリ ReVanced・Morphe・URV（Android）
**ReVancedとは？**
このオープンソースプロジェクトは、公式Androidアプリに改良パッチを適用することで、UX（ユーザーエクスペリエンス）を向上させることを目指しています。

**仕組み**
公式Androidアプリをベースに、改良パッチを適用して、Managerと呼ばれるツールでビルド作業を行います。
公式Androidアプリ + 改良パッチ → Managerでビルド → 公式Androidアプリ + ReVanced

**ツール**
Managerの利用は、**自己責任**で行う必要があります。
▶ Managerをインストールする前に、VirusTotal（<https://www.virustotal.com/gui/home/upload>）でスキャンをかけるのも良いかと思います。

**略称**
- **ReVanced**：YouTube ReVanced（ReVanced版）
- **RVX**：YouTube ReVanced Extended（inotia00版）※ 開発終了
- **Morphe**：ReVancedベースの新規プロジェクト
- **URV**：Universal ReVanced（URV版）※一部英語表示

▼ 詳しい使い方を知りたい場合や、不具合について質問する際は、まず下記のReVanced総合スレのテンプレを確認することを強くおすすめします ▼
- 5ch > Android > Revanced総合：[リンク](https://ff5ch.syoboi.jp/?q=Revanced%E7%B7%8F%E5%90%88)

### ◉ ReVanced 公式サイト
- HP：<https://revanced.app/>
- GitHub：<https://github.com/revanced>

### ◉ Morphe 公式サイト
- HP：<https://morphe.software/>
- GitHub：<https://github.com/MorpheApp>

### ◉ URV 公式サイト
- HP：<https://jmancentral.com/>
- GitHub：<https://github.com/Jman-Github>
URV Managerは、公式の最新開発版では相性の悪い「inotia00」や「anddea」といった、人気のあるサードパーティ製パッチでの不具合が解消されています。

<span style="color: red;">**留意点**</span>
YouTubeがYouTube ReVanced派生アプリの利用を直接的な理由としてアカウントを凍結したという報告は今のところありません。
▶ YouTube Premiumに加入しているアカウントでは、偽装による副作用を回避を抑えるために、設定 > その他 > **動画ストリームを偽装（Spoof video streams）を「OFF」にする設定**が推奨されます。

### ■ 𝕏/Twitter ReVancedの使い方
ModアプリやRoot化された端末が検知されるようになり、𝕏/Twitter ReVanced派生アプリ間で𝕏にログインしてデータを同期することが困難になりました。
- 2026年1月更新 twitter Revanced 新たにログインする方法：<https://kdroidwin.hatenablog.com/entry/2025/11/04/210359>

---

## Android アプリ ChMate（ChromeOS・Android）
- **Google Play**：<https://play.google.com/store/apps/details?id=jp.co.airfront.android.a2chMate>
- **HP**：<https://chmate.airfront.co.jp/>

**✐マーク（書き込みボタン）や↻リロード時のリストのアニメーション動作を元に戻す**
Homeやスレッドの右下︙ > 表示設定 >「リストをアニメーションする」の☑チェックを□OFFにする。

**レクタングル広告について**
ChMateスレ内の1の下と100毎の下に表示されるレクタングル広告は、AdGuard for AndroidやpersonalDNSfilterで除去できますが、ADの文字付き広告枠が残ります。このレクタングル広告は5ch側から配信されているもので、広告枠を除去するにはUPLIFTを購入する必要があります。

**参考サイト**
- 5ch > スマホアプリ・Android > 5chブラウザ「ChMate」質問スレ：[リンク](https://ff5ch.syoboi.jp/?q=5ch%E3%83%96%E3%83%A9%E3%82%A6%E3%82%B6%E3%80%8CChMate%E3%80%8D%E8%B3%AA%E5%95%8F%E3%82%B9%E3%83%AC)
- 5chどんぐり非公式まとめwiki：<https://donguri.wikiru.jp/>

---

## Manifest V3 対策
今後GoogleがManifest V3を大幅に変更し、ChromeOSの利便性を著しく損なうような事態になった場合、あくまで最終手段としてですが、Linux® ディストリビューションへの移行を視野に入れています。

**ChromeOSの今後の動向**
- Chromebook、Androidスタック移行後も継続。10年サポートも維持とGoogle 幹部が明言：<https://helentech.jp/news-80383/>
- ChromeOSは2034年に段階的廃止へ…：<https://internet.watch.impress.co.jp/docs/yajiuma/2083598.html>

**Linux 関連**
- 全学生に知ってもらいたいChromebookにLinuxをクリーンインストールする方法：<https://zenn.dev/roistaff/articles/30ce3883b3b9d9>
- Linux Mint 22をパソコンにインストールする方法：<https://tanoike.com/install-linux-mint-on-pc>
- AdGuard for Linux：<https://adguard.com/kb/ja/adguard-for-linux/>

**ECサイト購入優先順位**

Amazon.co.jp（プライム・デー｜ブラック・フライデー時）> メーカー直売サイト（キャンペーン｜セール時）> 楽天市場 = ヨドバシ.com

---

## Credits
- r/Adguard｜Reddit：<https://www.reddit.com/r/Adguard/>
- r/uBlockOrigin｜Reddit：<https://www.reddit.com/r/uBlockOrigin/>
- AdGuard Knowledgebase：<https://adguard.com/kb/ja/>
- AdGuard ブログ：[リンク](https://adguard-com.translate.goog/en/blog/index.html?_x_tr_sl=auto&_x_tr_tl=ja&_x_tr_hl=ja&_x_tr_pto=wapp)
- コンテンツブロックに関するアナウンス (Yuki2718氏の𝕏)：<https://x.com/Yuki27183>
- 雪フィルタ簡易報告掲示板：<https://jbbs.shitaraba.net/internet/25463/>
- コンテンツブロックについてよくある質問と回答：<https://github.com/Yuki2718/adblock2/wiki/%E3%82%88%E3%81%8F%E3%81%82%E3%82%8B%E8%B3%AA%E5%95%8F>
- Yuki2718’s gists：<https://gist.github.com/Yuki2718>
- とほほのwww入門：<https://www.tohoho-web.com/www.htm>
- サルにもわかる正規表現入門：<https://userweb.mnet.ne.jp/nakama/>
- uBlock Origin（UBO）で、ネットを優しい世界にしよう：<https://qiita.com/shtainze/items/1136dfc8e245f5c250fe>
- Kdroidwinの日記：<https://kdroidwin.hatenablog.com/archive>
- HelenTech：<https://helentech.jp/>
- 🌴 officeの杜 🥥：<https://officeforest.org/wp/>

この備忘録は CC0 ライセンスの下で提供します（This work is licensed under CC0 1.0 Universal）
**CC0について ― “いかなる権利も保有しない”**
<https://creativecommons.jp/sciencecommons/aboutcc0/>

**【免責・例外】** ただし、以下の内容は本ライセンスの適用外であり、それぞれの権利者が著作権を保有しています。
- 引用等で示された第三者の文章
- 紹介しているソフトウェア、アプリ、拡張機能の名称および公式の製品説明文
- リンク先のコンテンツ

記述内容は個人の検証に基づくものであり、正確性を保証するものではありません。
