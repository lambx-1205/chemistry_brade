# CHEMISTRY BRADE

化学構造式をブレードにして対戦する、ブラウザゲームのプロトタイプです。

## 現在の内容

- `index.html`: トップページ。レスポンシブ対応、3Dベンゼン模型のプレビュー、コンセプト紹介、分子候補カードを含みます。
- `.github/workflows/pages.yml`: `main` への push 時に GitHub Pages へデプロイするワークフローです。

現在の3Dプレビューはトップページ用の演出です。分子名からの構造取得、任意の構造式エディタ、対戦用の物理演算は今後の実装項目です。分子候補カードの図は簡略イラストであり、正式な構造式表示ではありません。

## GitHub Pages の初回設定

1. リポジトリの **Settings → Pages** を開きます。
2. **Build and deployment → Source** で **GitHub Actions** を選択します。
3. **Actions** タブで `Deploy static site to GitHub Pages` の実行結果を確認します。

設定済みなら、以降は `main` への push で自動デプロイされます。

## 技術メモ

トップページは静的な HTML / CSS / JavaScript です。3Dプレビューには Three.js を CDN から読み込みます。CDN や WebGL が利用できない環境では、SVG のフォールバック表示になります。
