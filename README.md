# グロースＸ ビジネスOS編 / AI編 ── 無料トライアル LP（叩き台）

「ビジネスを伸ばせるAI力をつける グロースＸ ビジネスOS編／AI編」1コース無料トライアルの
**ランディングページ・Web広告バナー・訴求コピー**一式（叩き台 v0.1）。

- メインCTA: **無料説明会（キックオフ）予約**
- トーン&マナー: [grtx.jp](https://grtx.jp/) 系（白ベース＋ブランドイエロー #FFD300／黒、課題→解決→実績→CTA）
- 出典: `20260610_グロースＸ新ビジネスAI編サービス資料.pdf`

## 公開URL（GitHub Pages）

- LP: `https://<user>.github.io/<repo>/`
- バナー一覧: `https://<user>.github.io/<repo>/banners/`

> push 後に Settings → Pages を有効化すると数分で公開されます（手順は下記）。

## 構成

```
growthx-ai-lp/
├── index.html            # LP本体
├── styles.css            # LPスタイル（ブランドカラー定義あり）
├── banners/              # Web広告バナー（HTML5・単体で入稿テスト可）
│   ├── index.html        #   バナー一覧プレビュー（まずここを開く）
│   ├── banner.css        #   バナー共通スタイル
│   ├── 300x250.html / 336x280.html / 728x90.html / 970x250.html
│   ├── 160x600.html / 320x100.html / 320x50.html
├── docs/
│   ├── lp-copy.md        # LP全原稿（MD化・セクションごと）
│   └── messaging.md      # 訴求セット（コピー資産／A-Bテスト案／ペルソナ別）
└── assets/               # OGP画像など（差し替え用）
```

## ローカル確認

```bash
cd growthx-ai-lp
python3 -m http.server 8080
# → http://localhost:8080/            (LP)
# → http://localhost:8080/banners/    (バナー一覧)
```

## GitHub Pages 公開手順（このリポジトリ用）

```bash
# main ブランチを push 済みの前提
gh repo edit --enable-pages 2>/dev/null || true
# または Web UI: Settings → Pages → Source: "Deploy from a branch" → main / (root) → Save
```

公開後、数分で `https://<user>.github.io/<repo>/` に反映されます。

## 叩き台のTODO（本番化に向けて）

- [ ] **フォーム接続**: `index.html` の `<form action="https://formspree.io/f/REPLACE_ME">` を
      Formspree / HubSpot / 自社API のエンドポイントに差し替え（送信通知先メールも）。
- [ ] **独自ドメイン**: grtx.jp 配下（例 `grtx.jp/lp-ai` などのパス or サブドメイン）へ接続。
      Pages を使う場合は `CNAME` ファイルと DNS 設定が必要。
- [ ] **実ロゴ/導入企業ロゴ**: 現状はテキスト代替。公式ロゴ画像（SVG/PNG）に差し替え。
- [ ] **OGP画像**: `assets/ogp.png`（1200×630）を作成して配置。
- [ ] **アプリUIキャプチャ**: ヒーローのスマホモックを実画面のスクショに差し替え可。
- [ ] **計測タグ**: GA4 / 広告コンバージョンタグを設置。
- [ ] **コピーの最終確認**: 数字・参考価格・条件（4名以上等）を最新の正式値に合わせる。

## メモ

- すべて静的HTML/CSS（ビルド不要・依存なし）。フォントのみ Google Fonts の Noto Sans JP を読込。
- バナーは画像ではなくHTML5。スクショで画像入稿、またはそのままHTML5バナーとして利用可。
- 表記ルール・コピーの根拠は `docs/messaging.md` を参照。
