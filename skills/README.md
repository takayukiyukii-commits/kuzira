# KUZIRA Skills — Claude Code / Codex 用スキル集

KUZIRA を「AIの目と手足」として使うためのスキルです。
インストールすると、Claude Code に **`/コマンド` として能力が増えます**。

## 収録スキル

| スキル | できること |
|---|---|
| [`x-pulse`](./x-pulse/SKILL.md) | 発信・広告の訴求軸を、推測ではなく **X上の実測エンゲージメント**で決める。訴求案とターゲティング用キーワードまで出力し、調査自体を魚拓＋Obsidian互換ノートで資産化する |

（順次追加していきます）

## 必要なもの

1. **KUZIRA**（無料・Windows / Mac） → https://kuzira.uni-core.jp
2. **Claude Code**（または Codex / Gemini CLI）

## インストール（1分）

### 1. スキルを置く

`SKILL.md` をスキルフォルダにコピーします。

**Claude Code の場合**

```bash
# Windows (PowerShell)
mkdir "$env:USERPROFILE\.claude\skills\x-pulse"
# ダウンロードした SKILL.md を上のフォルダに入れる

# Mac / Linux
mkdir -p ~/.claude/skills/x-pulse
cp SKILL.md ~/.claude/skills/x-pulse/
```

### 2. KUZIRA を Claude Code に接続する

KUZIRA は MCP サーバーを内蔵しています（起動中は常に開いています）。

```bash
claude mcp add --scope user --transport http kuzira http://127.0.0.1:8377/mcp
```

接続確認：Claude Code を再起動して「KUZIRAで開いているタブを教えて」と聞いてみてください。

> MCP登録をしなくても動きます（スキル内でHTTPを直接叩くフォールバックを持っています）が、
> 登録した方が安定して速いです。

### 3. 使う

KUZIRA を起動した状態で、Claude Code にこう言うだけです。

```
/x-pulse 自分の製品名やテーマ
```

## よくある質問

**Q. KUZIRAなしでは使えませんか？**
A. `x-pulse` は使えません。X（旧Twitter）はログインなしではページが描画されず、公式APIの検索は有料枠のため、「ログイン済みブラウザをAIが直接読む」経路が実質的に唯一の手段だからです。KUZIRA は無料なので、ダウンロードだけしておけば動きます。

**Q. 自分のXアカウントは安全ですか？**
A. スキルは**閲覧しかしません**（投稿・フォロー・DMは一切しません）。KUZIRA はプロファイル（own / rival / persona）でセッションを分離できるので、調査用に別プロファイルを使うこともできます。

**Q. Xの規約に触れませんか？**
A. 公開情報を通常の閲覧範囲で読むだけの設計です。スキル内でクエリ数の上限（10以内）を定めており、大量スクレイピングや高頻度アクセスは行いません。

**Q. Claude Code 以外でも使えますか？**
A. Codex / Gemini CLI でも、SKILL.md の内容をそのまま指示として渡せば同じ手順が実行できます（KUZIRA は CLI 経由でも操作できます）。

## ライセンス

自由に使い、改変し、社内で共有していただいて構いません。
改善案や「こういうスキルが欲しい」は歓迎します → https://kuzira.uni-core.jp

---
提供：ZUBOLAND株式会社（[UNIシリーズ](https://zuboland.jp/products)）
