# LiveLogのテスト版を自動更新する

テスト端末向けの任意設定です。通常のAPKダウンロードにも引き続き対応します。

1. [Obtainium公式](https://obtainium.imranr.dev/)からObtainiumをインストール。
2. [LiveLogをObtainiumへ登録](https://apps.obtainium.imranr.dev/redirect?r=obtainium://app/%7B%22id%22%3A%22jp.livelog.android%22%2C%22url%22%3A%22https%3A%2F%2Fgithub.com%2Fyusuke982%2FLiveLog-releases%22%2C%22author%22%3A%22yusuke982%22%2C%22name%22%3A%22LiveLog%22%2C%22additionalSettings%22%3A%22%7B%5C%22includePrereleases%5C%22%3Atrue%2C%5C%22includeDrafts%5C%22%3Afalse%2C%5C%22apkFilterRegEx%5C%22%3A%5C%22%5ELiveLog%5C%5C%5C%5C.apk%24%5C%22%7D%22%7D)して内容を確認し追加。先行版を含む設定済みです。
3. Obtainiumの設定でバックグラウンドの更新確認を有効にします。Wi-Fi接続時のみの取得がおすすめです。更新は即時通知ではなく定期確認です。
4. インストールの確認操作も減らしたい場合は、以下のShizukuを設定します。

## Xiaomi 14TでShizukuを使う場合

1. [Shizuku公式](https://shizuku.rikka.app/)からShizukuをインストール。
2. 設定で開発者向けオプションを有効にし、Wi-Fiへ接続して「USBデバッグ」「ワイヤレスデバッグ」を有効にします。HyperOSの版で項目名・位置が異なる場合があります。
3. Shizukuの「ワイヤレスデバッグで開始」の手順に従い、Android側のペア設定コードをShizukuへ入力し、Shizukuを起動します。ペアリングと起動は別の操作です。
4. Obtainium側のShizuku連携を有効にし、Shizukuの許可画面でObtainiumを許可。バックグラウンドのサイレントインストール設定も確認します。
5. 更新が許可されない場合は「USBデバッグ（セキュリティ設定）」があるか確認してください。Shizuku公式ではMIUI系端末で追加許可が必要と案内されています。OSのセキュリティ機能を一括で無効化する必要はありません。
6. バックグラウンドで止まる場合だけ、Obtainium/Shizukuの電池制限やバックグラウンド実行許可を確認します。

スマホを再起動すると、通常はShizukuの起動操作をもう一度行います。ペアリングは原則初回のみです。自動インストールの成否はOS設定によるため、最初の更新で実際に確認してください。
録音テスト中に更新が入るとアプリが停止する場合があるため、長時間テスト中は自動インストールを一時停止できます。

## 登録リンクが開かない場合

Obtainiumの「アプリを追加」で https://github.com/yusuke982/LiveLog-releases を指定し、「プレリリースを含める」をオンにしてください。
GitHubアカウントやAPIキーは不要です。個人のGitHubトークンを登録用JSONに含めないでください。

## できること・確認が必要なこと

開発側のビルド・検査・GitHub配布は自動化済み。登録用設定を用意済みです。
スマホへの初回インストール/権限許可/Shizukuの起動は利用者側の操作が必要です。Xiaomi 14T実機での初回自動更新は未確認です。

参考: [Obtainiumの設定](https://wiki.obtainium.imranr.dev/ui_overview/) / [登録リンクの仕様](https://wiki.obtainium.imranr.dev/deep_links/) / [Shizuku公式手順](https://shizuku.rikka.app/guide/setup/)
