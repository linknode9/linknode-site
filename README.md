# linknode.dev — Linknode ブランドのランディングページ
GitHub Pages で https://linknode.dev に公開する静的サイト。
Pages: Settings→Pages→Source=main/root。CNAMEで独自ドメイン自動設定。
DNS(apex→GitHub Pages) Aレコード: 185.199.108.153 / 185.199.109.153 / 185.199.110.153 / 185.199.111.153
注意: support@linknode.dev の MX は消さない。反映後 Enforce HTTPS をON。

## 学習ガイド（2026-09-17）

- 既存サイト内の `/guides/` に追加。最初はSPIの割合解説一本から始め、定期更新や記事の量産は前提にしない。
- 記事単体で考え方が分かる内容にし、末尾に関連アプリのストアリンクを置く。例題はオリジナルで作成する。
- 共通スタイルは `guides/guide.css`。静的HTMLと標準の `details` 要素を用い、JavaScriptなしでも読める。
- 新しい記事を公開するときは、一覧・トップの案内・`sitemap.xml` を必要に応じて更新する。
- 今回、アクセス解析やストア遷移の計測は導入していない。Search Consoleの接続状態も未確認。閲覧・ストア遷移・購入は区別し、計測できない成果は推定で補わない。
- 初回の見直しは公開から2〜3か月を目安とする。数字が少ない場合は効果を断定せず、記事を増やす前にテーマと導線を見直す。

## SPIアプリの案内（2026-10-29）

- `/spi3/` は、転職者向けSPI3-Gアプリの紹介・無料範囲・ストアへの入口。SNSのプロフィールや紹介先にはこのURLを使える。
- 両版に共通する学習内容・無料範囲・買い切り機能は、2026-11-05に各ストアの掲載情報で照合したもの。対応範囲の違いは各ストアの最新情報を優先する。
- トップのSPI紹介と割合記事の末尾から接続。SPI専用noteへのリンクも案内ページに置く。
- Appleの計測用provider tokenは未設定。iPhone版のリンクは通常のURLで、UTMだけでApp Storeの成果計測ができるとは扱わない。

## Android版への入口（2026-11-05）

- `/spi3/` のiPhone版・Android版ボタンを同じ見た目にし、どちらも無料体験への入口であることを明記した。短期プランなど買い切り機能の区別も近くに置く。
- SPIのGoogle Playリンクだけに、入口を区別するUTM sourceと共通campaignを付ける。sourceは `linknode_site_home`、`linknode_site_spi3`、`linknode_site_guide`。campaignは `spi_android_20261105`。
- UTMをURLパラメータに指定し、同じ値をPlay Install Referrer形式でも渡す。新しい解析SDK・Cookie・学習履歴送信は追加しない。
- Play Consoleのストア掲載情報で「広告と参照」「UTM source」「UTM campaign」を使って入口別の訪問・クリックを確認する。少数の場合は「その他」にまとまることがある。URLを付けただけでレポート反映・購入への貢献が確認できたとは扱わない。
- インストールボタンのクリック率（CTR）と実際のユーザー獲得・注文は別々に確認する。既存の検索流入と外部リンク経由も分け、同じ長さの期間で比較する。
