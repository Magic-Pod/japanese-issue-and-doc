## バージョン0.76.0(2021/4/11)

### 全般

- `New` UI要素の属性の、確認/待機/変数保存/条件分岐コマンドを追加しました。([#268](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/268))
- `Fix` 「画面キャプチャを取得」コマンドがネットワークエラーなどで画面キャプチャを取得できないことがある問題を改善しました。([#295](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/295))
- `Fix` magic_pod_config.jsonの値が不正だとサーバーエラーになることがあったので修正しました。
- `Fix` 対象となるテストが1つもないと、テストの一括実行がいつまでも終了しない不具合を修正しました。([#278](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/278))
- `Fix` Magic PodのWebサーバが重くなることがある問題に対する改善を実施しました。

### モバイルアプリテスト

- `New` [SauceLabsの新しいAPIを使ったテスト](https://www.trident-qa.com/magic-pod-saucelabs-batch-run/)に対応しました。
- `New` SauceLabsの新しいAPIを使った場合に、テスト結果画面にAppiumログが表示されるようになりました。([#238](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/238))
- `New` 利用しているAppiumのバージョンを更新しました。
  - Remote TestKit: Androidを[1.20.2](https://github.com/appium/appium/releases/tag/v1.20.2)に更新しました。
  - Remote TestKit(オンプレミス): [1.20.2](https://github.com/appium/appium/releases/tag/v1.20.2)に更新しました。
- `Fix` Androidのテストにて、テスト中に他のアプリに遷移する場合に、要素を見つけられないことがあったので修正しました。

### ブラウザテスト

- `New` SauceLabsのテスト結果画面にSeleniumログが表示されるようになりました。([#238](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/238))
- `New` 「モバイルエミュレーション」のテスト実行設定にて、「端末の向き」を指定可能になりました。([#270](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/270))
- `Fix` 「クライアント証明書」を指定してテスト実行していると、画面キャプチャの取得に失敗することがあったので修正しました。
- `Fix` 「クラウド」環境で、ブラウザ起動時に正しいURLが開かないことがあったので修正しました。
- `Fix` ime-mode属性がactiveの要素に対するテキスト入力がInternet Explorerでうまく動作しないことがあったので修正しました。

## バージョン0.75.0(2021/3/28)

### 全般

- `New` テストケース画面とテスト結果一覧画面の読み込み速度を改善しました。
- `Fix` テスト失敗時の自動修復に失敗することがある不具合を修正しました。
- `Fix` Magic PodのWebサーバに接続できなくなっていたので修正しました。

### モバイルアプリテスト

- `New` 「アプリをフォアグラウンド化」コマンドを追加しました。([#283](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/283))
- `New` テスト対象アプリを「クラウドアップロード」にした場合に、常に最後にアップロードしたファイルを使うよう指定可能になりました。([#252](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/252))
- `New` Androidのクラウド端末のストレージ容量を増やしました。
- `New` クラウド端末の安定性を強化しました。

### ブラウザテスト

- `New` テスト編集画面で環境「クラウド」を指定した場合も、端末の種類に「モバイルエミュレーション」を指定可能になりました。
- `New` テスト編集画面で環境「クラウド」を指定した場合も、「5秒後にキャプチャ」「ページ全体をキャプチャ」を指定可能になりました。
- `New` 「タイトルを保存」「URLを保存」コマンドを追加しました。([#292](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/292))

## バージョン0.74.0(2021/3/13)

### 下位互換性のない変更

- `Fix` モバイルアプリの「スワイプ」コマンドの移動方向が指定した方向と少しずれることがあったので修正しました。

### 全般

- `New` テスト結果画面にて、テストが未完了でも実行したところまでの「実行ログ」を確認できるようになりました。
- `New` テスト編集エリア両端の無駄な余白を減らしました。
- `Fix` 環境「クラウド」「外部クラウドサービス」でのテスト実行時に「日付計算」でエラーが出ることがあったので修正しました。
- `Fix` UIのスキャンや自動修復に失敗することがあったので修正しました。

### モバイルアプリテスト

- `New` 「クリップボードに値をセット」コマンドを追加しました。
- `New` 「キーボードキー入力」コマンドでテキストを指定できるようになりました。
  - 現在フォーカスのある要素にテキストを送信できます。
- `New` クラウド端末の安定性を強化しました。
- `Fix` 「アプリをバックグラウンド化」や「ホーム」の「システムボタンを押す」で、タイムエラーが発生することがあったので修正しました。

### ブラウザテスト

- `New` テスト編集画面でも環境に「クラウド」を指定できるようになりました。
  - クラウドのブラウザを利用して、テストの作成と単体実行が行えます。

## バージョン0.73.0(2021/2/27)

### 下位互換性のない変更

- `Fix` モバイルアプリの「フリック」コマンドのフリック量の計算が正しくないことがあったので修正しました。

### 全般

- `New` ロケータ生成の際に優先利用しないようにランダム生成文字列として、より多くのパターンを判定できるようになりました。
- `New` テスト一括実行画面の読み込み時に、前回最後に選択した一括実行設定が初期表示されるようになりました。
- `Fix` 各種画面のUIの細かい修正を行いました。([#232](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/232))

### モバイルアプリテスト

- `New` 利用しているAppiumのバージョンを更新しました。
  - BrowserStack: [1.20.2](https://github.com/appium/appium/releases/tag/v1.20.2)に更新しました。
  - SauceLabs: iOSは[1.20.1](https://github.com/appium/appium/releases/tag/v1.20.1)、Androidは[1.19.0](https://github.com/appium/appium/releases/tag/v1.19.0)に更新しました。
- `New` 1台のクラウド端末の最大連続利用可能時間を、有料プランの場合は3時間から10時間にしました。
- `New` クラウド端末の安定性を強化しました。
- `Fix` 「アプリを終了」コマンドの実行後に、条件によっては「ホーム」に対する「システムボタンを押す」コマンドでエラーが出るようになっていたので修正しました。

### ブラウザテスト

- `New` Local/Session Storageの「値セット」「クリア」「値保存」コマンドを追加しました。([#282](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/282))
- `Fix` optgroup要素の下にあるoption要素を「プルダウン選択」で選択できない問題を修正しました。
- `Fix` 条件によってはテスト編集画面で環境として「クラウド」を選択できるようになっていたので修正しました。
- `Fix` 条件によっては「クラウド」環境の「モバイルエミュレーション」テスト実行が失敗するようになっていたので修正しました。
- `Fix` 画面からの「ローカルPC」環境のInternet Explorerに対するテストが実行できなくなっていたので修正しました。

## バージョン0.72.0(2021/2/13)

### 下位互換性のない変更

- `Fix` 「クラウド」環境のブラウザが「ベースURL」を利用できない不具合を修正しました。

### 全般

- `New` テストケース中で利用しているUI要素は、テスト編集画面のUI上でできるだけ他の要素に隠されないようにしました。
  - 同じ要素を何回も使う場合に、毎回「この要素を一時的に隠す」操作をしなくてもよくなります。
- `New` 「ローカルPC」テストにて、「追加のルート証明書」を指定できるようになりました。
  - 「Web APIコール」コマンドでのみ有効になります。ブラウザでサイトにアクセスする際に追加のルート証明書が必要な場合は、ブラウザにルート証明書を登録してください。
- `New` 要素のid属性などがUUIDを含む場合には、含まない部分だけを優先度の高いロケータとして利用するようにしました。
- `New` UIスキャンの速度を改善しました。
- `New` テスト編集画面での行削除・切り取り後に、削除・切り取り行の1つ上ではなく下の行が選択されるようになりました。
- `New` UI一覧を分割して新しいセクションを作る場合に、分割位置より前ではなく後ろのUIを元に新しいセクションが作られるようになりました。([#262](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/262))
- `New` 各種画面のUIの細かい改善を行いました。
- `Fix` テストケースが1行も無い場合に、コピーした別のテストケースを貼り付けできない不具合を修正しました。
- `Fix` 「Web APIコール」コマンドのURLの先頭で変数を利用できない不具合を修正しました。
- `Fix` テスト失敗時の自動修復に失敗することがある不具合を修正しました。
- `Fix` Mac版Magic Pod Desktop.appのupdateコマンドが動作しなくなっていたので修正しました。

### モバイルアプリテスト

- `Fix` iOSで、「アプリを閉じる」コマンドを実行した後に画面操作がエラーになる問題を修正しました。([#264](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/264))
  - 「クラウド」「ローカルPC」のテストでのみ修正されています。
- `Fix` AndroidのWebview要素を見つけられずエラーになることがあったので修正しました。

## バージョン0.71.0(2021/1/30)

### 下位互換性のない変更

- `New` iOSモバイルアプリの「accessbility id」ロケータは、従来はname、label、value属性を利用していましたが、name属性のみを見るように変わりました。
  - Appiumの仕様変更によるものです。
  - 影響を受ける可能性があった既存テストについては、問題が起きないよう、できる限りアップデートを実施済みです。

### 全般

- `New` 条件分岐コマンドもコピー・切り取り可能になりました。([#235](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/235))
  - ただし条件分岐の始まりと終わりの対応が取れてない部分をコピー・切り取りすることはできません。
- `New` BrowserStack上のテストで、「ネットワークログ」を取得するかどうかを指定可能になりました。([#258](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/258))
  - BrowserStackモバイルアプリテストで取得していた「ネットワークログ」はデフォルトでは取得されなくなったので、取得する必要がある場合はテスト一括実行設定で指定してください。
- `New` 特に要素数が多い画面に対する、UI解析の速度を大きく改善しました。
- `New` 要素のid属性などがUUIDの場合には、その属性を使ったロケータの候補内での順位を下げました。
- `New` 自動修復の挙動を改善しました。
- `New` ネットワークエラーなどが原因でテスト実行結果のサーバへの保存に失敗した場合に、何回かリトライするようにしました。
- `Fix` PCにNode.jsがインストールされているとローカルPCでのテスト実行が正しく動作しないことがあったので修正しました。

### モバイルアプリテスト

- `New` 利用しているAppiumのバージョンを[1.20.2](https://github.com/appium/appium/releases/tag/v1.20.2)にしました。
  - これにより、ローカルPCテストにXcode12.3/12.4、iOS14.3/14.4を利用可能になりました。
- `Fix` モバイルSafariの画面を「HTMLをWebViewとしてキャプチャする」のオプションでキャプチャすると、要素の座標がずれる不具合を修正しました。(iOS13.4以降のみ修正)
- `Fix` 「秒間待つ」コマンドで長時間待機した後にセッションエラーが出ることがあったので修正しました。

### ブラウザテスト

- `Fix` 「クリックしてファイルアップロード」コマンドが正しく動作しないケースがあったので修正しました。

## バージョン0.70.0(2021/1/16)

### 全般

- `New` 「二段階認証用のパスコードを生成して保存」コマンドを追加しました。
- `New` ブラウザからMagic Pod Desktopを起動した場合に、ログイン処理が自動で行われるようになりました。([#216](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/216), [#134](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/134), [#79](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/79))
- `New` 自動修復の挙動を改善しました。
- `New` GitHubログインの初回画面のデザインを改善しました。
- `Fix` プロジェクトの「更新」権限が無いと共有ステップを複製できない不具合を修正しました。
- `Fix` 画面キャプチャのサイズが大きいとAIロケータによる要素検索が失敗することがあったので修正しました。
- `Fix` テスト一括実行画面からの、複数端末/ブラウザパターンのテスト実行でサーバエラーになることがあったので修正しました。
- `Fix` HTMLが名前空間つきのタグや属性を含んでいると画面スキャンに失敗することがあったので修正しました。
- `Fix` UI上で前面にあるべき要素が背面に隠れてしまう問題に対する改善を実施しました。

### モバイルアプリテスト

- `New` 画面上の回転ボタンを使い、テスト作成中にクラウド端末を横向きにできるようになりました。([#148](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/148))
  - 横長固定のアプリの画面キャプチャがクラウド端末で取得できない問題も解消されています。
- `New` 利用しているAppiumのバージョンを更新しました。
  - BrowserStack: [1.19.1](https://github.com/appium/appium/releases/tag/v1.19.1)に更新しました。
  - SauceLabs: [1.19.0](https://github.com/appium/appium/releases/tag/v1.19.0)に更新しました。
- `New` Remote TestKitクライアントから起動したAndroid端末を使って、FLAG_SECUREなアプリの画面キャプチャを取得可能になりました。
  - 仮想adbを有効化し、画像転送モードを「標準モード」にする必要があります。
- `New` 「スワイプ」コマンドのパラメータの初期値を、「X:50%、Y:50%、方向:0°」にしました。([#224](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/224))
- `Fix` WebViewをHTMLとしてスキャンしている画面でテスト失敗した場合に、テスト結果画面で失敗時UIツリーを表示できないことがあったので修正しました。
- `Fix` 「指定位置タップ」で対象要素の領域外をタップした際にエラーになることがあったので修正しました。

### ブラウザテスト

- `New` 特別な変数として「BASE_URL」を利用可能になりました。([#257](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/257))
- `New` 「クラウド」と「ローカルPC」(現在Mac上のみ)のChromeテスト作成・実行時に、サイトに接続するための「クライアント証明書」を指定可能になりました。([#253](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/253))
- `New` 「クリックしてファイルアップロード」の対象にinput要素以外を指定しても、付近のinput要素を探して適切にアップロード処理を行うようになりました。([#255](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/255))

## バージョン0.69.0(2020/12/26)

### 全般

- `New` 共有ステップを複製できるようになりました。([#251](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/251))
- `New` 各テスト一括実行結果のページで、テスト結果サマリーが見られるようになりました。([#222](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/222))
- `New` 「指定位置クリック」「指定位置タップ」で、「座標」を指定できるようになりました。([#195](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/195))
- `New` 操作対象の要素の状態が不正でStaleElementReferenceエラーが出た場合に、何回かリトライするようにしました。
- `Fix` 含まれるUIの数が多いUIセクションの削除に失敗することがあったので修正しました。
- `Fix` UI解析の結果において、他の要素の上側にあるべき要素が下側に隠れてしまうことがあったので修正しました。
- `Fix` 「四則演算」コマンドの値が間違ったものになることがあったので修正しました。
- `Fix` 一部の環境でデータパターンのCSVアップロードに失敗する不具合を修正しました。
- `Fix` GitHubアカウントを使った新規ユーザー登録ができなくなっていたので修正しました。
- `Fix` テストの0行目を実行中にテストを中止しても中止されなくなっていたので修正しました。

### モバイルアプリテスト

- `New` 利用するAppiumのバージョンを[1.19.1](https://github.com/appium/appium/releases/tag/v1.19.1)にしました。
- `Fix` 「クラウドアップロード」のアプリのアップロードに失敗することがあったので修正しました。
- `Fix` BrowserStackの動作が変わったことに伴い、「クラウドアップロード」のアプリでBrowserStackテスト実行できなくなっていたので修正しました。

### ブラウザテスト

- `New` 「クラウド」環境でブラウザテストを実行可能になりました。([#170](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/170))
  - 現在「デスクトップChrome」と「モバイルエミュレーション」に対応しています。
  - スタンダードプランでは同時2並列、エンタープライズプランでは同時6並列まで利用できます。
- `New` ファイルアップロード操作が可能な、「クリックしてアップロード」のコマンドを追加しました。
  - アップロード対象のファイルをMagic Pod上に保管できます。
  - クラウド、外部クラウドサービス、ローカルPC、全ての環境で実行可能です。
- `New` 「クラウド」環境において、テスト対象サイトにアクセスする際の「クライアント証明書」を指定可能になりました。([#253](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/253))
- `New` Chrome88とEdge88に対応しました。
- `Fix` iframe内の要素がUI解析で検出されない場合があったので修正しました。
- `Fix` iframe内の要素の操作に失敗するようになっていたケースがあったので修正しました。

## バージョン0.68.0(2020/12/13)

### 全般

- `New` [SAMLによるシングルサインオン](https://www.trident-qa.com/saml-auth-setting/)でMagic Podにログインできるようになりました。(エンタープライズプランのみ)([#229](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/229))
- `New` プロジェクト複製時に、多言語データパターンも複製されるようになりました。(有料プランのみ)
- `New` 自動修復の各種精度改善と不具合修正を実施しました。
- `Fix` 失敗したテスト一括実行結果の書き込みに失敗することがあったので修正しました。
- `Fix` スタンダードプランの料金の一部が契約当月でなく翌月に引き落とされるようになっていたので修正しました。
- `Fix` 「テスト一括実行」のスケジュール設定が誤って有効化されてしまうことがあったので修正しました。
- `Fix` ローカルPCのテスト一括実行時に、同じ組織の他の起動中のMagic Pod Desktopでもテストが実行されるようになっていたので修正しました。
  - 権限のないユーザーがテストを参照・実行できるなどのセキュリティ上の問題はありません。

### モバイルアプリテスト

- `New` 全ての無料プラン組織で、外部クラウドサービスを使ったテスト一括実行はできなくなりました。
  - 従来は、2019年11月以前に作成した組織であれば、無料プランでも外部クラウドサービスを使ったテスト一括実行が可能でした。
- `Fix` タイムゾーン指定するとテスト編集画面からのAndroidクラウド端末起動に失敗する不具合を修正しました。

### ブラウザテスト

- `New` ある要素が別の要素に覆われていてクリック等のコマンドがエラーになる場合に、何回かリトライするようにしました。
- `Fix` スクロールされた位置にある要素に対する「指定位置クリック」が正しく動作しない不具合を修正しました。

## バージョン0.67.1(2020/12/2)

### 全般

- `Fix` 自動修復が発生した後続のテスト結果のステータスが正しく表示されなくなっていたので修正しました。
- `Fix` 一部のケースでテストケースの複製や順番変更ができなくなっていたので修正しました。
- `Fix` 一部のケースでMagic Pod Desktopを起動できなくなっていたので修正しました。

### モバイルアプリテスト

- `Fix` ローカルPCのAndroidテストにおける、「アプリ情報を取得」ボタンが動作しなくなっていたので修正しました。

## バージョン0.67.0(2020/11/28)

### 全般

- `New` 自動修復を実施した後続ステップでエラーになったテストの結果画面において、自動修復の内容を強制承認できるようになりました。
- `New` 自動修復の精度を改善しました。
- `New` 「プルダウン選択」のコマンドが空白差異を無視してテキストを選択するようになりました。
- `Fix` 「秒間待つ」コマンドの待機時間が長いとテスト実行がエラーになることがあったので修正しました。
- `Fix` 「ローカルPC」の一括テスト実行の設定によっては、「テストを一括実行」のボタンを押してもMagic Pod Desktopが起動しない不具合を修正しました。

### モバイルアプリテスト

- `New` ローカルPCのiOSシミュレータに、Xcode12.2、iOS14.2を利用可能になりました。
- `Fix` 「他のアプリを起動」コマンドのパラメータに指定された変数が変数として認識されない不具合を修正しました。

## バージョン0.66.0(2020/11/14)

### 全般

- `New` テスト編集画面にて、複数のUIを別セクションに一括で移動できるようになりました。([#101](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/101)、[#201](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/201))
- `New` magic_pod_config.jsonのlanguageで、Magic Pod Desktopコマンドライン実行時の表示言語を指定可能になりました。
- `New` 自動修復の各種精度改善を行いました。

### モバイルアプリテスト

- `New` ローカルPCのiOSシミュレータテストで、「iPhone 12」シリーズなどの新しい端末を指定可能になりました。
- `Fix` Xcode12を使ったローカルPCのiOSテストで「-ios class chain」ロケータがうまく動作しないケースがあったので、 この場合xpathを使うようにしました。
- `Fix` WebViewをHTMLとしてスキャンしているテストの失敗時UIツリーが開けないことがある問題を改善しました。
- `Fix` 一括実行の端末パターン/ブラウザパターンに日本語が含まれていると、SauceLabsのモバイル実機テストがエラーになっていたので修正しました。

## バージョン0.65.0(2020/11/1)

### 下位互換性のない変更

- cross-batch-runのWeb APIが、複数(端末/ブラウザ)パターンを集約した結果を返すようになりました。

### 全般

- `New` 複数(端末/ブラウザ)パターンの一括実行結果の各種改善を行いました。([#103](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/103))
  - 全パターンの結果を1つの結果ページで見られる様になりました。
  - screenshotsのWeb APIとmagic-pod-api-clientのget-screenshotsコマンドが、全パターンの画面キャプチャをダウンロードするようになりました。
  - batch-runsのWeb APIが、全パターンを集約した結果を返すようになりました。
  - テスト結果メールの書式を改善しました。
  - 今回の修正に伴いテスト結果の進捗表記の数字が不正になるため、magic-pod-api-clientのバージョンを[0.65.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.65.0.1)にしてご利用ください。
- `New` 組織、プロジェクト、テストケースの一覧に、説明の内容を表示するようにしました。([#207](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/207))
- `New` 組織の表示名、プロジェクトの表示名、テストケース名、共有ステップ名に使える文字種類の制約が無くなりました。([#233](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/233))
- `New` 自動修復の各種精度改善と不具合修正を行いました。
- `New` テストごとの実行結果一覧ページの読み込み速度を改善しました。
- `New` フリーメールアドレス等でのユーザー新規登録はできなくなりました。
- `Fix` OSユーザー名に日本語が入っているとWindows版MagicPodDesktop.exeのインストールに失敗する不具合を修正しました。

### モバイルアプリテスト

- `New` ローカルPCのiOSシミュレータに、Xcode12.1、iOS14.1を利用可能になりました。
- `New` iOSクラウド端末の安定性を強化しました。
- `New` [driverExecutablePath](https://www.trident-qa.com/magic-pod-webview/#sec6)の設定で、ローカルPCのAndroid WebViewテストに利用するChrome Driverのバージョンを指定可能になりました。
- `Fix` ローカルPCテストで画面キャプチャ取得ボタンを連続して押すとUIスキャンに失敗することがあったので修正しました。
- `Fix` サイズの大きいアプリのアップロードに失敗することがあったので修正しました。

### ブラウザテスト

- `New` 「指定位置クリック」のコマンドを追加しました。([#206](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/206))
- `New` 組織の設定画面から、スタンダードプランをクレジットカード申し込み可能になりました。
- `New` Chrome87とEdge87に対応しました。
- `Fix` ローカルPCのChromeテスト実行がバージョン判定エラーで失敗することがあったので修正しました。

## バージョン0.64.0(2020/10/18)

### 全般

- `New` UI一覧の各種改善を行いました。(複数UIの一括削除、空のセクション追加等)([#101](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/101))
- `New` 一括実行結果のテスト一覧画面の各種改善を行いました。
- `New` 自動修復の各種精度改善と不具合修正を行いました。
- `New` 一括実行設定の「テストケース番号」で、1*10のような記法で同じ番号のテストを何度も繰り返し実行可能になりました。([#220](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/220))
- `New` 次回リリースの準備としてmagic-pod-api-clientを0.63.0.1に更新しました。
  - magic-pod-api-clientで複数端末・ブラウザパターンを使った一括実行をしている場合、次回リリース(10/31)までに[0.63.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.63.0.1)に更新してください。更新しないと返り値を正しく取得できなくなります。
- `Fix` 「日付計算」コマンドがWindowsで動作しない不具合を修正しました。
- `Fix` テスト一括実行結果画面キャプチャのZipファイルが、Windows標準の解凍コマンドで解凍できないことがあったので修正しました。

### モバイルアプリテスト

- `New` iOSのUI要素に対し、[UIツリーから検索](https://www.trident-qa.com/magic-pod-locator-parameter/#magic_pod_locator)方式のロケータを追加できるようになりました。
   - 通常のAppiumロケータでは見つけられない要素が、この方式だと見つけられる場合があります。
- `Fix` 「値を保存」コマンドがiOSでうまく動作しないケースがあったので修正しました。
- `Fix` 「WebView要素をHTMLとしてスキャンする」にチェックをつけた時のスキャンがAndroidで失敗するケースがあったので修正しました。

### ブラウザテスト

- `New` ブラウザテストプランの現在の内容確認とトライアル申し込みが、組織の設定画面から可能になりました。

## バージョン0.63.0(2020/10/4)

### 全般

- `New` [BrowserStack Local](https://www.trident-qa.com/magic-pod-local-server-access/#browserstack)を使い、プライベート環境のサーバに対するBrowserStackテストが可能になりました。
- `New` 自動修復の精度を改善しました。
- `Fix` Magic PodのWebサーバが重くなることがある問題に対する各種改善を実施しました。
- `Fix` 「四則演算」コマンドに0を指定するとうまく動作しない不具合を修正しました。
- `Fix` 共有ステップを含むテスト結果画面キャプチャのダウンロードに失敗することがある不具合を修正しました。
- `Fix` Web APIからのテスト実行時に関するエラーメッセージが正しく出ないことがあったので修正しました。

### モバイルアプリテスト

- `New` 「クリップボードの値を保存」コマンドを追加しました。([#217](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/217))
  - iOS実機には未対応です。
- `New` Androidクラウドシミュレータのバージョンに「11.0」を指定可能になりました。
- `New` クラウド端末とローカルPCで利用するAppiumのバージョンを[1.18.2](https://github.com/appium/appium/releases/tag/v1.18.2)にしました。
  - Xcode12が正しく動作しない問題などが解消されています。
- `Fix` クラウド端末の表示と動作に関する細かい問題を修正しました。

### ブラウザテスト

- `Fix` UIスキャンがうまく動作しないことがある不具合を修正しました。

## バージョン0.62.0(2020/9/23)

### 全般

- `New` UI要素/変数の値の、数値比較結果の確認/待機/条件分岐コマンドを追加しました。([#181](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/181))
- `New` テスト失敗をAIによって自動修復して欲しいと思った時に、テスト結果画面からAIの改善要望を送信できるようになりました。
- `New` テスト編集画面の表示を改善しました。(デザイン改善、テスト編集エリア下部の無駄な余白の削除、等)
- `New` Magic Pod Desktopログイン失敗時のメッセージを改善しました。([#120](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/120))
- `New` テスト結果画面と組織のメンバー一覧の表示を改善しました。([#172](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/172))
- `New` 自動修復の精度を改善しました。
- `Fix` Magic PodのWebサーバが重くなることがある問題に対する各種改善を実施しました。
- `Fix` データ量が多い組織やプロジェクトを削除するとエラーが出る不具合を修正しました。
- `Fix` UI上で前面にあるべき要素が背面に隠れてしまう問題に対する改善を実施しました。
- `Fix` プロジェクトの「更新」権限がないと共有ステップを削除できない不具合を修正しました。

### モバイルアプリテスト

- `New` クラウド端末がテスト編集画面と同じブラウザウィンドウで利用可能になりました。
- `New` クラウド端末の各種表示を改善しました。([#96](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/96))
- `New` クラウド端末が外部に接続する際に利用するIPの範囲を207.254.20.32/27にしました。
- `Fix` 複数のWebViewを含むAndroidアプリのUIスキャンがうまくいかないことがある問題を修正しました。
- `Fix` AndroidのChromeがバージョン85の場合にWebViewのUIスキャン/テスト実行に失敗することがある問題を修正しました。
- `Fix` iOS実機にMagic Pod Desktopで接続した際にWARNINGメッセージが出ることがあったので修正しました。

### ブラウザテスト

- `New` Chrome86とEdge86に対応しました。

## バージョン0.61.0(2020/9/5)

### 下位互換性のない変更

- `Fix` ほとんど同じ画面なのに、テスト結果画面キャプチャのサイズが毎回変わってしまうことがある問題を解消しました。
  - これにより、テスト結果画面キャプチャのサイズが従来と変わることがあります。

### 全般

- `New` 「テキスト入力」コマンドで、複数行のテキストを入力できるようになりました。([#208](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/208))
- `New` テスト結果に関する問い合わせに、テスト作成時の画面キャプチャとUIツリーを添付できるようになりました。
- `New` プロジェクト複製時にテストのラベルと一括実行設定が、テスト複製時にテストのラベルが複製されるようになりました。
  - 一括実行設定については、共有設定と自分自身の設定のみ複製されます。
- `Fix` 改行文字を含むロケータが動作しない不具合を修正しました。([#109](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/109))
- `Fix` 同時に多数のUIスキャンが実行されるとエラーになることがあったので修正しました。
- `Fix` テスト名が長いとテスト一覧の表示が崩れる問題を修正しました。
- `Fix` 誤ったxpathロケータが生成されることがあったので修正しました。
- `Fix` Magic Pod Desktopのバージョンアップ確認ダイアログからダウンロードページを開けなくなっていたので修正しました。

### モバイルアプリテスト

- `New` 「画面中央をマルチタッチ操作」コマンドを追加しました。([#204](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/204))
- `New` 「システムボタンを押す」コマンドのパラメータで長押しするかを選択可能になりました。([#203](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/203))
- `New` 英数字と記号以外の文字をファイル名に含むアプリもテストできるようになりました。
- `New` 利用しているAppiumのバージョンを更新しました。
  - クラウド、ローカルPC、SauceLabs: [1.18.1](https://github.com/appium/appium/releases/tag/v1.18.1)に更新しました。
  - BrowserStack: iOSを[1.18.0](https://github.com/appium/appium/releases/tag/v1.18.0)に更新しました。
- `New` ローカルPCのiOSシミュレータに、Xcode11.6、Xcode12(ベータ)、iOS13.7、iOS14.0(ベータ)を利用可能になりました。

### ブラウザテスト

- `Fix` HTMLの属性名に「;」「?」が含まれているとUIスキャンがエラーになる不具合を修正しました。

## バージョン0.60.0(2020/8/22)

### 全般

- `New` テストケースに「ラベル」を付与できるようになりました。([#121](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/121))
- `New` 一括実行の際に、特定のラベルを持つテストだけを対象にしたり、特定のラベルを持つテストを対象から除外したりできるようになりました。([#121](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/121))
- `New` 「正規表現に一致した部分を保存」コマンドを追加しました。([#205](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/205))
- `Fix` プランページからスタンダードプランを申し込んでも有効にならなくなっていたので修正しました。

### ブラウザテスト

- `New` Chrome85に対応しました。

## バージョン0.59.0(2020/8/8)

### 全般

- `New` ユーザーの「メール設定」で、テスト結果メールを受け取るかどうか設定可能になりました。([#202](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/202))
- `New` 「テキスト入力」コマンドの引数に「最大リトライ回数」を指定できるようになりました。テキスト入力が不安定になる箇所で利用できます。
- `New` テスト結果一覧画面の結果件数が多い場合には、2ページ目以降に表示されるようにしました。
- `New` テスト結果一覧画面の読み込み速度を改善しました。
- `New` UIスキャンの速度を改善しました。

### モバイルアプリテスト

- `New` Remotet TestKitのテスト実行中に、テスト結果画面で「リアルタイム動画」を確認できるようになりました。

### ブラウザテスト

- `New` 「ショートカットキー入力」コマンドを追加しました。([#194](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/194))
- `New` 特別な変数として、「OS」「DEVICE_TYPE」を利用可能になりました。
- `New` Windows版Magic Pod Desktopインストール時の、OSの警告メッセージが出なくなりました。([#136](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/136))
- `Fix` 画面キャプチャ範囲「HTML」の画面キャプチャがWindows上のChromeでうまくとれないことがあったので修正しました。

## バージョン0.58.0(2020/7/24)

### 下位互換性のない変更

- `New` Windows上のMagicPodDesktop.exeを使ったコマンドライン実行において、OSのプロキシ設定を利用しないようにしました。
  - この処理が原因でテストがいつまでも終了しないことがあるためです。
  - Windows上のMagicPodDesktop.exeコマンドライン実行でプロキシサーバを利用する必要がある場合は、[magic_pod_config.jsonで直接指定](https://www.trident-qa.com/magic-pod-proxy/)してください。
- `Fix` iOSアプリの「表示されるまでスワイプ」が長時間続いたり、間違った方向にスワイプされたりする問題を修正しました。
  - 今回の修正により、「表示されるまでスワイプ」の動きが変わるケースがあります。

### 全般

- `New` 「日時計算」コマンドの「言語設定」で「中国語」を選択可能になりました。
- `Fix` 「四則演算」コマンドのパラメータに変数を指定できない不具合を修正しました。

### モバイルアプリテスト

- `New` 「シェイク」コマンドを追加しました。([#168](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/168))
  - 「エミュレータ」「シミュレータ」で利用できます。
- `New` 「長押し & 移動」コマンドを追加しました。([#158](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/158))
- `New` テスト対象指定パネルで「アプリのタイムゾーン」を指定可能になりました。([#180](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/180))
- `New` テスト対象指定パネルの「端末の言語」で「中国語」を選択可能になりました。([#182](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/182))
- `New` 「WebView要素をHTMLとしてスキャンする」をオフにしてスキャンしたUIをオンで再アップロードした場合の挙動を改善しました。([#174](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/174))
- `New` Remote TestKitを使ったテスト一括実行の画面キャプチャが、FLAG_SECUREが有効なAndroidアプリでも取得可能になりました。
- `New` ローカルPCのiOSシミュレータに、Xcode11.6、iOS13.6を利用可能になりました。
- `New` Remote TestKitのAndroidテストで使用するAppiumのバージョンを[1.17.1](https://github.com/appium/appium/releases/tag/v1.17.1)にしました。
- `New` テストのタイムアウトエラーが出にくいようにしました。
- `New` サポート対象バージョンであるJava8以外を使っている場合でも、Magic Pod Desktopがエラーを出さない様にしました。
- `New` Appファイルのクラウドアップロードにおいて、.zipファイル内の.appファイル名が英数字以外でもアップロード可能になりました。
- `Fix` WebView関連のコマンドの速度が遅くなっていたので修正しました。

### ブラウザテスト

- `New` デスクトップChromeのモバイルエミュレーション機能を使い、モバイルWebサイトのテスト作成・実行が可能になりました。([#151](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/151))
- `Fix` 全角文字を含む属性名が含まれるWebページのUIスキャンがエラーになる不具合を修正しました。

## バージョン0.57.0(2020/7/11)

### 全般

- `New` テストごとのテスト結果一覧画面にも、テストを実行した端末名・iOSバージョン・ブラウザなどのラベルが表示されるようになりました。
- `New` テスト一括実行結果一覧のラベルで、「環境」と「ブラウザバージョン」の情報が表示されるようになりました。
- `New` 「画面キャプチャを取得」コマンドの引数に画面キャプチャ名を指定可能になりました。
- `New` テスト一括実行結果取得のWeb APIに、パラメータmin_batch_run_numberとmax_batch_run_number、返り値started_atとfinished_atを追加しました。
- `New` 画面キャプチャダウンロードのWeb APIにパラメータfile_name_body_type、mask_dynamically_changed_areaを追加しました。
- `New` [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)の[0.57.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.57.0.1)で、get-screenshotsにパラメータfile_index_type、file_name_body_type、download_type、mask_dynamically_changed_areaを追加しました。
- `New` 共有ステップのパラメータ関連の表示を改善しました。

### モバイルアプリテスト

- `New` 1回のスキャンで複数のWebViewが見つかった場合にも、「Web要素をHTMLとしてスキャンする」が正しく動作するようになりました。
- `New` 「スワイプ」コマンドの座標指定方法が、絶対値指定から「%」指定になりました。([#81](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/81))
- `Fix` 「他のアプリを起動(Android)」のコマンドがエラーになることがあったので修正しました。

### ブラウザテスト

- `New` BrowserStack/SauceLabsを使ったテストが、Internet Explorerでも可能になりました。

## バージョン0.56.0(2020/6/28)

### 全般

- `New` [四則演算](https://github.com/Magic-Pod/japanese-issue-and-doc/wiki/%E3%82%B3%E3%83%9E%E3%83%B3%E3%83%89%E4%B8%80%E8%A6%A7)コマンドを追加しました。([#164](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/164))
- `New` SauceLabs/BrowserStack側のテスト結果ページで、対応するMagic Podのプロジェクト名/一括実行番号/テスト名を確認できるようになりました。
- `New` 特別な変数として、現在の実行環境を表す[ENVIRONMENT](https://www.trident-qa.com/magic-pod-variable/#sepcial_vars)が利用可能になりました。 
- `New` UI解析の速度を改善しました。
- `New` magic_pod_config.json上で、Magic Pod Desktopが利用する[プロキシ情報](https://www.trident-qa.com/magic-pod-proxy/)を指定可能になりました。
  - proxyServerUrl、proxyServerAuthType、proxyServerAuthUser、proxyServerAuthPasswordが指定できます。
- `New` 「日時保存」コマンドのコマンド名を「日付計算」に変更し、「システム」のタブに移動しました。
- `New` ユーザー新規登録の際に、モバイルアプリテストのスタンダードプラン1ヶ月無料トライアルが申し込み可能になりました。
- `New` 組織のプランページにて、テストケース数150を選択可能になりました。
- `Fix` テスト失敗時の自動修復に失敗することがある不具合を修正しました。
- `Fix` テスト対象指定パネルで制御文字等を入力すると、パネルが開けなくなることがあったので修正しました。
- `Fix` 環境変数HTTP_PROXY、HTTPS_PROXY、NO_PROXYが指定されているとMagic Pod Desktopが正常に動作しない不具合を修正しました。

### ブラウザテスト

- `New` [BrowserStack](https://www.trident-qa.com/magic-pod-browserstack-batch-run-browser/)/[SauceLabs](https://www.trident-qa.com/magic-pod-saucelabs-batch-run-browser/)を使った、画面からの一括テスト実行/Web API実行/スケジュール実行が可能になりました。([#170](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/170))
- `New` Chromium Edgeを使ったテストが可能になりました。([#150](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/150))
  - Windows版とMac版の両方に対応しています。
- `New` magic_pod_config.jsonに[driverExecutableDir](https://www.trident-qa.com/magic-pod-web-test-advanced/#old_browser)を設定することで、Magic Pod Desktopで通常サポートされていないバージョンのブラウザでもテストが可能になりました。

## バージョン0.55.0(2020/6/13)

### 全般

- `New` 有料プランの支払いに利用するカードの複数登録・変更・削除が可能になりました。
- `New` テスト結果画面のAppium/Seleniumログを見やすくしました。
- `New` テスト結果画面のAppium/Seleniumログをクリップボードにコピーできるようになりました。
- `New` 直近のテスト結果をWeb APIで取得可能になりました。
- `New` [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョン[0.55.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.55.0.1)で、最新の一括テスト実行番号取得と画面キャプチャのダウンロードが可能になりました。
- `Fix` テスト失敗時の自動修復に失敗することがある不具合を修正しました。

### モバイルアプリテスト

- `New` リニューアルされた新しいBitriseステップ「Magic Pod」をリリースしました。
  - テスト設定番号でMagic Pod側の設定を参照、またはWeb APIに近い形式で設定値をBitriseステップ側に保持できます。
  - 従来のBitriseステップでは未対応だった様々なテスト一括実行パラメータを指定できます。
  - テスト終了時・成功時にアプリを削除できます。
  - 従来の「Magic Pod UI test」ステップは今後非推奨になります。
- `New` iOSクラウドシミュレータのバージョンに「11.4」を追加しました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))
- `New` 「他のアプリを起動」コマンドを追加しました。(外部クラウドサービス上でのiOSテストには未対応です)([#177](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/177))
- `New` Android5、6のクラウドエミュレータでもWebViewのテストが動作するようになりました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))
- `New` モバイルアプリテストの無料プランで利用できるクラウド端末の初月利用時間を10時間に増やしました。
- `New` SauceLabsで使用するAppiumのバージョンを[1.17.1](https://github.com/appium/appium/releases/tag/v1.17.1)にしました。

### ブラウザテスト

- `New` Safariを使ったローカルPCテストが可能になりました。([#129](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/129))
- `New` Chrome84に対応しました。

## バージョン0.54.2(2020/6/7)

### 全般

- `Fix` 条件によっては、Magic Pod Desktopを使った画面キャプチャ取得に失敗するようになっていたので修正しました。

## バージョン0.54.1(2020/6/3)

### モバイルアプリテスト

- `Fix` 条件によっては、Magic Pod Desktopを使ったAndroidの画面キャプチャ取得に失敗するようになっていたので修正しました。

## バージョン0.54.0(2020/5/30)

### 全般

- `New` UI一覧のリスト形式表示を使いやすく改善しました。(一度にたくさんのUIを確認できる、UIのプレビューが見られる、UI名が見切れない、等)([#161](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/161))
- `New` UI解析の細かい改善を行いました。
- `Fix` Chrome バージョン83で画面レイアウトが崩れてしまう問題を修正しました。

### モバイルアプリテスト

- `New` 「アプリを起動」のオプションに「端末リセット」を追加しました。([#175](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/175))
  - 「クラウド端末」「SauceLabs」「BrowserStack」で利用できます。
- `New` ローカルPCのiOSシミュレータのバージョンに13.5を指定可能になりました。
- `New` Remote TestKit(オンプレミス)で使用するAppiumのバージョンを[1.16.0](https://github.com/appium/appium/releases/tag/v1.16.0)にしました。
- `Fix` BrowserStackでAndroidのAppiumログを取得できない不具合を修正しました。
- `Fix` マシン負荷が高いとiOSクラウド端末でのWebViewテストに失敗することがある不具合を修正しました。
- `Fix` Androidで「ピッカー値入力」が動作しなくなっていたので修正しました。
- `Fix` Androidクラウド端末の動作が不安性になっていたので修正しました。

### ブラウザテスト

- `New` URLが「一致するか」「一致しないか」「含むか」「含まないか」の「確認」コマンドを追加しました。
- `New` タイトルが「含むか」「含まないか」の「確認」コマンドを追加しました。
- `Fix` 「マウスオーバー」のコマンドが動作しないことがあったので修正しました。

## バージョン0.53.0(2020/5/17)

### 下位互換性のない変更(モバイルアプリテスト)

- `Fix` 「アプリを起動」のオプションに「プロセス再起動」を指定した場合に、iOSクラウドシミュレータにてアプリの再インストールが行われる不具合を修正しました。

### 全般

- `New` テスト編集画面で「コメント」と「空行」を指定可能になりました。([#19](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/19))
- `New` Web APIのcross-batch-runと[magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のbatch-runで、テスト設定の番号を指定してテスト実行可能になりました。
  - Web APIから実行する設定を画面側で管理できます。
  - test settings numberとtest settingsの両方を指定すれば、番号の設定を利用しつつ、さらにその一部だけを変更して実行することもできます。
  - [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョンは[0.53.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.53.0.1)を利用してください。
- `New` [ヘルプページ](https://www.trident-qa.com/magic-pod-help/)の読み込み速度を大幅に改善しました。
- `New` テスト結果画面の表示を改善しました。([#172](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/172))
- `New` テスト編集画面の表示を改善しました。([#165](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/165))
- `Fix` プロジェクト内に同じ名前のUIが複数あると、テスト一括実行が失敗することがあったので修正しました。
- `Fix` 共有変数の値に「&」が含まれているとMagic Pod Desktopのエラーが発生する不具合を修正しました。
- `Fix` テスト結果に関する問い合わせが失敗するようになっていたケースがあったので修正しました。

### モバイルアプリテスト

- `New` Androidクラウドシミュレータのバージョンに「9.0」「８.1」「8.0」「7.1」「7.0」「6.0」「5.1」「5.0」を指定可能になりました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))
- `New` Androidクラウドエミュレータで、カメラアプリやカメラを使ったアプリが動作するようになりました。
  - 撮影できるのはエミュレータが表示している初期画像です。
- `New` iOSクラウドシミュレータの高速起動する端末が「13.4」の「iPhone 8」になりました。
- `New` 利用しているAppiumのバージョンを[1.17.1](https://github.com/appium/appium/releases/tag/v1.17.1)にしました。
  - iOS13.4でHTMLとしてスキャンしたWebViewのテストが動作しない問題などが解消されています。
- `New` ローカルPCのiOSシミュレータテストで「iPhone SE (2nd generation)」「iPad Pro (12.9-inch) (4th generation)」「iPad Pro (11-inch) (2nd generation)」を指定できるようになりました。
- `New` 「WebView要素をHTMLとしてスキャンする」を有効にしている場合にも、スキャン結果にAIロケータが含まれるようになりました。
- `New` 「WebView要素をHTMLとしてスキャンする」を指定した場合のUIスキャンの速度を改善しました。
- `Fix` 外部クラウドサービスのレスポンスが遅くタイムアウトエラーが発生することがあったので修正しました。
- `Fix` Remote TestKit環境の問題で発生する各種エラーが起きにくいようにしました。

### ブラウザテスト

- `New` ユーザー登録の際に「ブラウザテスト機能」の無料トライアルをリクエストできるようになりました。

## バージョン0.52.0(2020/4/26)

### 機能追加

- iOSクラウド端末のテスト作成時にも機種を選べるようになりました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))(モバイルアプリテスト)
- iOSクラウド端末でバージョン13.4と12.4を選べるようになりました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))(モバイルアプリテスト)　
- Androidクラウド端末で選べる機種が増えました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))(モバイルアプリテスト)
  - 高速起動する機種は「Pixel 3」になりました。
- テスト結果画面からテスト結果について問い合わせる場合に、Appium/Seleniumログ、失敗時画面キャプチャ、失敗時UIツリーの添付内容を確認・上書き・削除できるようになりました。
- テスト結果画面の細かい改善を行いました。([#145](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/145))
- 自動修復の各種精度改善を行いました。
- 利用しているAppiumのバージョンを更新しました。(モバイルアプリテスト)
  - BrowserStack: Androidを[1.17.0](https://github.com/appium/appium/releases/tag/v1.17.0)に更新しました。
  - RemoteTestKit: Androidを[1.16.0](https://github.com/appium/appium/releases/tag/v1.16.0)に更新しました。
  - SaucewLabs: [1.17.0](https://github.com/appium/appium/releases/tag/v1.17.0)に更新しました。

### 不具合修正

- ブラウザの「戻る」ボタンを使ってテスト・共有ステップ編集画面に戻ると、古いテストケースが表示される問題を修正しました。([#145](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/145))
- テスト実行中に組織・プロジェクト名を変更するとテストが終了しなくなる不具合を修正しました。([#171](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/171))
- iOSの特定の画面でUIアップロードに失敗する不具合を修正しました。([#159](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/159))(モバイルアプリテスト)
- iPhone専用のiOSアプリに対するテストをiPad上で実行すると、一部のコマンドが正常に動作しない不具合を修正しました。(モバイルアプリテスト)
- SauceLabs上でのテスト実行が動作しなくなっていたので修正しました。(モバイルアプリテスト)
  - SauceLabsの不具合が原因です。

## バージョン0.51.0(2020/4/12)

### 機能追加

- テスト一括実行を画面からスケジュール指定して実行可能になりました。好きな時間と曜日で定期実行できます。
  - 現在モバイルアプリテストでのみ利用可能です。
- 「日時を保存」コマンドを追加しました。([#156](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/156), [#147](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/147))
  - 現在、ヶ月前/後、日前/後などの様々な日時を、年、月、日、時間、エポック秒、エポックミリ秒、日付書式指定など様々な形式で取得して変数に保存できます。
- テストとプロジェクトの複製はバックグラウンドで実施され、完了したら通知が来るようになりました。
  - 複製に時間がかかると画面表示がサーバーエラーになる不具合も合わせ修正されています。
- テスト失敗時のロケータ自動修復において、その要素が使われている全てのテストの動作を確認できていない場合には、注意を促すメッセージを出すようにしました。
- 自動修復の各種精度改善を行いました。
- [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョン[0.50.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.50.0.1)で、HTTPヘッダを指定する「--http_headers」オプションを指定可能になりました。
- 多言語データパターンとデータパターンのCSVの推奨エンコードはUTF-8になりました。
- テスト実行後に、そのテストに使用したクラウドアップロードアプリを削除しても、テスト結果画面では引き続きアプリの情報が見られるようになりました。(モバイルアプリテスト)([#169](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/169))
- WebViewテストに関連した各種メッセージを改善しました。(モバイルアプリテスト)
- 「表示されるまでUI要素をスクロール」のコマンドを追加しました。ページ全体でなく、特定のスクロールボックスをスクロールできます。(ブラウザテスト)

### 不具合修正

- 多言語データパターンでCSV出力したファイルをExcelで開くと文字化けする不具合を修正しました。
- 多言語データパターンCSV取込やデータパターンCSVアップロードにおいて、ファイルのエンコードによってはエラーや文字化けが起きる不具合を修正しました。
- テストケースの複製が失敗することがあったので修正しました。
- テストの実行中にテストケースを削除すると、テスト結果が書き込まれない不具合を修正しました。
- 「画面全体の描画が終わるまで待つ」コマンドによる待機中に端末やブラウザのウィンドウサイズが変わるとエラーになる不具合を修正しました。
- iOSで、要素が存在するにも関わらず、その要素を見つけられずにエラーになることがあったので修正しました。(モバイルアプリテスト)
- 「テキスト入力」コマンドが半角カナを入力できない不具合を修正しました。(ブラウザテスト)
- 「ブラウザを開く」コマンドの「Cookieをクリア」のオプションが動作しなくなっていたので修正しました。(ブラウザテスト)

## バージョン0.50.0(2020/3/28)

### 下位互換性のない機能追加

- 様々なtypeのinput要素に「テキスト入力」で正しく値をセットできるようになりました。(ブラウザテスト)
- 様々なtypeのinput要素の値を正しく取得できるようになりました。(ブラウザテスト)

### 機能追加

- Androidのクラウドエミュレータで、Google APIやGooleアカウントに依存したアプリが動作するようになりました。
- Androidのクラウドエミュレータで利用できる初期アプリの種類が増えました
- 自動修復結果の確認ダイアログで、修復前と後のUIツリーの内容を確認できるようになりました。
- 自動修復の各種精度改善を行いました。
- テスト編集画面におけるUI一覧の読み込みを高速化しました。
- BrowserStackテスト実行時のAppiumログをテスト結果画面で確認できるようになりました。
- 利用するAppiumのバージョンを[1.17.0](https://github.com/appium/appium/releases/tag/v1.17.0)にしました。
  - iOSのWebViewに対するテストがクラッシュすることがある不具合などが解消されています。
- ローカルPCのiOSシミュレータに、Xcode11.4、iOS13.4を利用可能になりました。
- テスト結果画面キャプチャの画質を改善しました。(ブラウザテスト)
- Firefoxに対しても、非表示のtypeがfileのinput要素に対して「テキスト入力」コマンドでファイルパスを指定することで、ファイルアップロードが可能になりました。(ブラウザテスト)

### 不具合修正

- テスト結果画面でWebViewを含むエラー時のUIツリーを表示するとエラーになることがあったので修正しました。
- パラメータにUI要素を持つ共有ステップをプロジェクト複製すると、複製先でパラメータが消えている不具合を修正しました。
- フレーム内のコンテンツが別ドメインから読み込まれたものの場合に、UIアップロードに失敗する不具合を修正しました。
- テストの単体実行を中断すると、同じユーザーの一括テスト実行も中断されてしまう不具合を修正しました。
- 画面によってはUIのアップロードに失敗することがある不具合を修正しました。
- テスト開始時や実行中にサーバエラーになることがあったので修正しました。
- テスト実行中にタイムアウトエラーが起きることがあったので修正しました。
- UI数が多いプロジェクトの一括テスト実行や複製の際にサーバエラーになることがあったので修正しました。

## バージョン0.49.0(2020/3/14)

### 下位互換性のない機能追加

- 各種「変数」コマンドと「Web APIコール」コマンドで、変数の値としてbooleanや数字をセットしても、文字列として扱われるようになりました。
- 変数(多言語データパターン、共有変数、データパターン含む)の名前が空白文字だったり、両端にスペースを含む場合に、エラーとするようになりました。
- typeがfileのinput要素の値を取得すると、セットされたファイルパスが返るようになりました。(ブラウザテスト)

### 機能追加

- テスト設定ポップアップおよびWeb APIで、「共有変数」を指定できるようになりました。([#38](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/38))
  - Web APIの「credentials」パラメータは非推奨となったので、「shared_variables」を利用してください。
- テスト実行中でも、完了したステップまでの画面キャプチャをテスト結果画面で確認できるようになりました。
  - ページのリロードは自動では行われません。
- 要素が見つからない場合の自動修復が、iframeとWebView内の要素に対しても行われるようになりました。
- テスト実行ログに、セットされた変数の値が表示されるようになりました。
- 「キーボードキー入力」のコマンドで、数字を送信できるようになりました。
  - 「テスト入力」コマンドでうまく数字をセットできない要素に対して有効な場合があります。
- データ駆動テストの値が${...}で共有変数や多言語データパターンの値を参照できるようになりました。([#118](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/118))
- appファイルをzip圧縮してアップロードする場合に、zipファイル内のappファイル名が英数字以外だとエラーが出るようになりました。
- 一部のケースでUI解析の速度を改善しました。
- typeがfileのinput要素に対して「テキスト入力」コマンドでファイルパスを指定することで、ファイルアップロードが可能になりました。(ブラウザテスト)
  - input要素が非表示要素の場合には、現在Chromeのみ対応しています。

### 不具合修正

- クラウド端末を再起動しても、再起動前の画像が表示され続けることがある不具合を修正しました。
- testOnlyフラグが有効になっているAndroidアプリのテストがエラーになる不具合を修正しました。
- BrowserStackのテスト実行を複数端末並列で実施すると、アプリに途中でアクセスできなくなることがある不具合を修正しました。
- 要素が見つからない場合の自動修復が予期せぬエラーで失敗することがあったので修正しました。
- WebViewが背面にある場合にポップアップがスキャンできない不具合を修正しました。
- 制御文字が画面ツリー上に含まれているとスキャンがうまくいかない不具合を修正しました。
- テストケース複製で作成したテストケースの順序を画面上でうまく変更できない不具合を修正しました。
- スキャンで生成されたxpathロケータが不正なケースがあったので修正しました。
- UI要素の名前を変更しても、そのUIの自動修復を承認すると変更前の名前に戻ってしまう不具合を修正しました。
- 複数端末パターンの一括実行において、「1つずつ実行」がうまくいかないことがあったので修正しました。
- 「スイッチ操作」のコマンドが、変更する値と現在の値が同じ場合にエラーになっていたので修正しました。
- 一部のケースで多言語データパターン、データパターンの値をうまく参照できなくなっていたので修正しました。

## バージョン0.48.0(2020/2/29)

### 下位互換性のない機能追加

- [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョン[0.47.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.47.0.1)で、自動修復が発生した場合に返り値2を返すようになりました。

### 機能追加

- テスト実行時に要素が見つからない場合に、可能な時には要素のロケータの自動修復が行われるようになりました。
  - 現在は、テスト一括実行をした場合に限り発動します。
  - テスト結果画面で修復内容を承認することで、ロケータの変更内容が保存されます。
  - [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョンは[0.47.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.47.0.1)を利用してください。
- テスト編集画面の右クリックメニューから、行の途中にコマンドを追加できるようになりました。([#44](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/44))
- テスト編集画面の要素/UIのドラッグ&ドロップやUI一覧エリアの使い勝手を改善しました。
- テスト編集画面で追加したロケータが、UIの上書きアップロードをした後も引き継がれるようになりました。
- プロジェクトやテストの複製機能の速度を改善しました。
- BrowserStackのAndroidテストで使用するAppiumのバージョンを[1.16.0](https://github.com/appium/appium/releases/tag/v1.16.0)にしました。
- 「テストケース番号」がBitrise Step側からも指定可能になりました。
  - Bitrise Stepの指定バージョンを0.47.1以上にする必要があります。
- 「アプリを起動」のオプションで、「初回のみプロセス再起動」を選べるようになりました。([#141](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/141))
  - BrowserStack以外の環境で利用できます。

### 不具合修正

- iOS実機上で、「WebView要素をHTMLとしてスキャンする」が動作しない不具合を修正しました。
- コピーされたコマンドを含むテストがあるプロジェクトを複製するとエラーになるケースの修正が不十分だったので、追加で修正しました。
- アプリのアップロードを同時に行うと不正なデータが作成されることがあったので修正しました。
- 「プロジェクト作成」の権限がないユーザーが、本来可能なはずのいくつかの操作ができない不具合を修正しました。
- WebView要素をHTMLとしてスキャンするとエラーになることがあったので修正しました。
- Magic Pod Desktopからテストを実行した場合に、[特別な変数](https://www.trident-qa.com/magic-pod-variable/#sepcial_vars)を利用できない不具合を修正しました。
- 一部のプランで設定されているプロジェクト数上限制限がうまく動作していない不具合を修正しました。
- ファイルサイズが大きなアプリのアップロードに失敗するようになっていたので修正しました。
- magic_pod_config.jsonでexternalAppiumをtrueにすると、iOSのテストで要素が何も見つからなくなっていたので修正しました。

## バージョン0.47.0(2020/2/15)

### 機能追加

- 「変数の値」が「一致するか」「一致しないか」「含むか」「含まないか」の「確認」「場合」コマンドを追加しました。([#130](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/130))
- テストケースの複製機能を追加しました。([#124](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/124))
- 「固定値を保存」のコマンドの値に、別の変数を含められるようになりました。
- [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)にdelete-appのコマンドを追加しました。
  - [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)のバージョン[0.46.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.46.0.1)をインストールする必要があります。
- テスト編集画面でUI要素に追加したロケータが、すぐに自動的に使用されるようになりました。
- 1つのテストがタイムアウトするまでの時間が、テストの長さに応じて変わるようになりました。
- テスト編集画面の各種改善を行いました。
- UI要素関連の「確認」「待機」「条件分岐」のコマンド名を、変数系のコマンドと区別するために「UI要素が...」のように変更しました。
- アプリを起動のパラメータ名を、「(プロセス再起動)」「(プロセス再起動)(アプリ情報クリア)」に変更しました。

### 不具合修正

- テストのステップ数が多いと、テスト結果の書き込み、テスト結果の表示、画面キャプチャのダウンロードが失敗する不具合を修正しました。
- upload-fileのWeb APIのfileパラメータが無いとサーバエラーになる不具合を修正しました。
- Remote TestKit上のWebViewテストでCSSロケータが動作しない不具合を修正しました。
- クラウド端末を終了してすぐに次の端末を起動すると、いつまでも起動しないことがある不具合を修正しました。
- Android WebViewの「ダブルタップ」コマンドが正常に動作しない不具合を修正しました。
- Web APIドキュメントにおける、delete-fileコマンドのdataパラメータの型が間違っていたので修正しました。
- テスト一括実行の時間が実際より長く表示されてしまう場合があったので修正しました。
- UI一覧画面の細かい不具合を修正しました。
- プロジェクトの複製が失敗するようになっていたので修正しました。
- テスト/プロジェクトの削除処理が遅くなっていたので修正しました。

## バージョン0.46.0(2020/2/1)

### 機能追加

- iOSクラウド端末を使った一括実行の際に、機種を選べるようになりました。([#139](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/139))
- 端末やブラウザの情報を取得する特別な変数として${OS}、${VERSION}、${MODEL}、${DEVICE_TYPE}、${DEVICE_REGION}、${DEVICE_LANGUAGE}、${BROWSER}が利用可能になりました。([#131](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/131))
- 「アサート」「チェック」のコマンド名を、より分かりやすい「確認」に変更しました。
- 「WebView要素をHTMLとしてスキャンする」設定が、ローカルPCのiOS実機と外部クラウドサービスでも利用可能になりました。
- Androidのクラウド端末で、「初期アプリ」「Androidデモアプリ」を選択可能になりました。
- 無料プランでも、クラウド端末を作成2台、一括実行2台まで同時に利用できるようにしました。
- Remote TestKitのiOSテスト結果画面でAppiumログを確認できるようになりました。
- 利用しているAppiumのバージョンを更新しました。
  - クラウド/ローカルPC: [1.16.0](https://github.com/appium/appium/releases/tag/v1.16.0)に更新しました。
  - BrowserStack: iOSは[1.16.0](https://github.com/appium/appium/releases/tag/v1.16.0)、Androidは[1.15.0](https://github.com/appium/appium/releases/tag/v1.15.0)に更新しました。
  - RemoteTestKit: Androidを[1.15.1](https://github.com/appium/appium/releases/tag/v1.15.1)に更新しました。
- 組織にアクセス可能な接続元IPを組織の設定画面で指定できるようになりました。(エンタープライズプランのみ)
- ブラウザテスト周りの各種改善を行いました。
  - テスト編集画面で、テスト対象のウィンドウサイズを指定可能になりました。
  - テスト編集画面で「画面キャプチャ範囲」を「ウィンドウ」にした場合に、外部ディスプレイでテストを実行していると画面キャプチャがうまくとれないことがある問題を修正しました。(Windowsのみ修正)

### 不具合修正

- magic_pod_config.jsonの不正な設定値が原因でMagic Pod Desktopがサーバ接続/ログインできなくなる場合があったので修正しました。
- 「ピッカー値入力」のコマンドがエラーになることがあったので修正しました。
- 一括テスト実行を同時に複数開始するとエラーになることがあったので修正しました。
- JavaScriptのダイアログが表示されている場合に、WebViewの画面キャプチャ取得やテスト実行が長時間フリーズする不具合を修正しました。
- 共有ステップ画面を開いていると、クラウド端末の画面キャプチャがうまく取得できない不具合を修正しました。
- プロジェクトの削除、テストの削除がエラーになることがあったので修正しました。
- 「外部クラウドサービス」のテストにおいて「ログレベル」の設定がうまく効いていなかったので修正しました。
- テスト一括実行設定の「テスト結果をメール通知」チェックを外してもメール通知されてしまうことがあったので修正しました。

## バージョン0.45.0(2020/1/15)

### 機能追加

- 「テスト一括実行」の設定を、ブラウザ上でなくサーバ上に保存するようになりました。
  - 別PCでログインしたり、ブラウザのキャッシュをクリアしても、設定が消えることがなくなります。
- 「テスト一括実行」の設定を、プロジェクト全体で共有可能になりました。
- 「テスト一括実行」設定の、「外部クラウドサービス」の「アクセスキー」「アクセストークン」「TestObject APIキー」の値が保存されるようになりました。
  - 暗号化して保存されます。
- 「テスト一括実行」の設定にて、「クラウド」の環境に対しても「端末パターンを追加」が可能になりました。
- [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)から複数端末パターンを使った一括実行を行えるようになりました。
  - [magic-pod-api-client](https://github.com/Magic-Pod/magic-pod-api-client)の[バージョン0.45.0.1](https://github.com/Magic-Pod/magic-pod-api-client/releases/tag/0.45.0.1)をインストールする必要があります。
- cross-batch-runのWeb APIの返り値として各種テスト情報が返るようになりました。
- iOS12シミュレータでも「WebView要素をHTMLとしてスキャンする」設定が利用可能になりました。
- 「クラウド」の環境でもAndroidの「WebView要素をHTMLとしてスキャンする」設定が利用可能になりました。
- 新規作成されたテストのテスト対象設定のデフォルト値として、1つ前のテストのテスト対象設定の値を利用するようになりました。([#41](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/41))
- appファイルを含まないzipファイルをテスト対象アプリとしてクラウドアップロードすると、エラーになるようにしました。([#140](https://github.com/Magic-Pod/japanese-issue-and-doc/issues/140))
- iOSクラウド端末のサンプルアプリを、UIカタログデモアプリから、より安定して使えるVodQAサンプルアプリに変更しました。
- クラウド端末の起動/接続時の挙動を改善しました。
- テスト結果ページの細かい表示を改善しました。
- 初回登録ページの細かい表示を改善しました。

### 不具合修正

- テスト編集ページから別ページに遷移をすると、クラウド端末の画面キャプチャ取得に失敗することがあったので修正しました。
- プロジェクトを複製した際に「端末に画像を追加」コマンドの画像が複製されない不具合を修正しました。

[もっと古いCHANGELOGを見る](https://github.com/Magic-Pod/japanese-issue-and-doc/blob/master/CHANGELOG_OLD.md)
