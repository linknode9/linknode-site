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
