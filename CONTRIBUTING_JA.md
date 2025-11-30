# VeritasChain Protocol への貢献ガイド

VeritasChain Protocol（VCP）への貢献に興味をお持ちいただき、ありがとうございます！このドキュメントでは、貢献のためのガイドラインと手順を説明します。

## 目次

- [行動規範](#行動規範)
- [貢献の方法](#貢献の方法)
- [はじめに](#はじめに)
- [開発ワークフロー](#開発ワークフロー)
- [スタイルガイドライン](#スタイルガイドライン)
- [コミットメッセージ](#コミットメッセージ)
- [プルリクエストのプロセス](#プルリクエストのプロセス)
- [コミュニティ](#コミュニティ)

## 行動規範

このプロジェクトとすべての参加者は、[行動規範](CODE_OF_CONDUCT_JA.md)に従います。参加することにより、この規範を遵守することが求められます。容認できない行動は info@veritaschain.org までご報告ください。

## 貢献の方法

### バグの報告

バグ報告を作成する前に、重複を避けるために既存のIssueを確認してください。バグ報告を作成する際は、できるだけ多くの詳細を含めてください：

- **明確で説明的なタイトルを使用する**
- **問題を再現する正確な手順を説明する**
- **具体的な例を提供する**（コードスニペット、設定ファイル）
- **観察した動作と期待した動作を説明する**
- **関連するログとエラーメッセージを含める**

### 機能の提案

機能の提案を歓迎します！以下を提供してください：

- **明確で説明的なタイトル**
- **提案された機能の詳細な説明**
- **この機能がなぜ有用かを説明する**
- **検討した代替案をリストする**

### コードの貢献

コードの貢献を歓迎します！貢献できる分野：

- **バグ修正** - 報告された問題の修正
- **ドキュメント** - ドキュメントの改善または翻訳
- **テスト** - テストカバレッジの追加または改善
- **機能** - 新機能の実装（事前に相談してください）

### ドキュメントの改善

ドキュメントの改善は常に歓迎します：

- タイポや文法的な誤りの修正
- 欠落している情報の追加
- 明確さと読みやすさの向上
- ドキュメントの翻訳（EN、JA、ZH対応）

## はじめに

### 前提条件

リポジトリによって、以下が必要になる場合があります：

- **Node.js 18+** と npm（TypeScriptプロジェクト用）
- **Python 3.9+**（Pythonプロジェクト用）
- **MetaTrader 5**（MQL5プロジェクト用）
- **Git** バージョン管理用

### フォークとクローン

1. GitHubでリポジトリをフォーク
2. フォークをローカルにクローン：
   ```bash
   git clone https://github.com/あなたのユーザー名/リポジトリ名.git
   cd リポジトリ名
   ```
3. upstreamリモートを追加：
   ```bash
   git remote add upstream https://github.com/veritaschain/リポジトリ名.git
   ```

### 依存関係のインストール

```bash
# Node.jsプロジェクトの場合
npm install

# Pythonプロジェクトの場合
pip install -r requirements.txt
```

## 開発ワークフロー

### ブランチの作成

変更用のブランチを作成します：

```bash
git checkout -b feature/機能名
# または
git checkout -b fix/問題の説明
```

ブランチ命名規則：
- `feature/` - 新機能
- `fix/` - バグ修正
- `docs/` - ドキュメント変更
- `refactor/` - コードリファクタリング
- `test/` - テストの追加または修正

### 変更の作成

1. ブランチで変更を行う
2. 必要に応じてテストを作成または更新
3. すべてのテストが合格することを確認
4. 必要に応じてドキュメントを更新

### テスト

```bash
# TypeScriptプロジェクト
npm run lint
npm run type-check
npm run test

# Pythonプロジェクト
python -m pytest
```

## スタイルガイドライン

### TypeScript/JavaScript

- フォーマットに**ESLint**と**Prettier**を使用
- TypeScript strictモードを使用
- `let`より`const`を優先
- 意味のある変数名と関数名を使用
- パブリックAPIにはJSDocコメントを追加

```typescript
/**
 * 指定されたパラメータで新しいVCPイベントを作成します。
 * @param eventType - イベントタイプ（SIG、ORD、EXEなど）
 * @param payload - イベントペイロード
 * @returns 作成されたVCPイベント
 */
export function createEvent(eventType: EventType, payload: Payload): VcpEvent {
  // 実装
}
```

### Python

- **PEP 8**スタイルガイドに従う
- フォーマットに**Black**を使用
- 関数シグネチャに**型ヒント**を使用
- パブリック関数にdocstringを追加

```python
def create_event(event_type: str, payload: dict) -> VcpEvent:
    """
    指定されたパラメータで新しいVCPイベントを作成します。

    Args:
        event_type: イベントタイプ（SIG、ORD、EXEなど）
        payload: イベントペイロード

    Returns:
        作成されたVCPイベント
    """
    # 実装
```

### MQL5

- 説明的な変数名を使用
- 複雑なロジックにコメントを追加
- MetaQuotesコーディング標準に従う

### ドキュメント

- ドキュメントには**Markdown**を使用
- 行の長さは適度に保つ（≤120文字）
- ヘッダーを使用してコンテンツを整理
- 役立つ場所にコード例を含める

## コミットメッセージ

[Conventional Commits](https://www.conventionalcommits.org/)仕様に従います：

```
<type>(<scope>): <description>

[optional body]

[optional footer]
```

### タイプ

- `feat` - 新機能
- `fix` - バグ修正
- `docs` - ドキュメント変更
- `style` - コードスタイル変更（フォーマットなど）
- `refactor` - コードリファクタリング
- `test` - テストの追加または修正
- `chore` - メンテナンスタスク
- `ci` - CI/CD変更

### 例

```
feat(sdk): VCPイベントロギング用Python SDKを追加

fix(explorer): Merkle proof検証エラーを解決

docs(readme): 日本語でQuick Startセクションを追加

ci: 自動テスト用GitHub Actionsワークフローを追加
```

## プルリクエストのプロセス

### 送信前

1. **最新のupstream変更でブランチを更新**：
   ```bash
   git fetch upstream
   git rebase upstream/main
   ```

2. **すべてのチェックが合格することを確認**：
   - すべてのテストが合格
   - コードがスタイルガイドラインに従っている
   - ドキュメントが更新されている

3. **明確なPR説明を書く**：
   - どのような変更が行われたか
   - なぜこれらの変更が行われたか
   - 関連するIssue（`Fixes #123`で自動クローズ）

### レビュープロセス

1. メンテナがPRをレビュー
2. 要求された変更に対応
3. 承認されたら、メンテナがPRをマージ

### マージ後

- フィーチャーブランチを削除
- upstreamから最新の変更をプル

## コミュニティ

### ヘルプの取得

- **GitHub Issues** - バグと機能リクエスト用
- **GitHub Discussions** - 質問と一般的な議論用
- **Email** - info@veritaschain.org

### 繋がりを保つ

- **ウェブサイト**: https://veritaschain.org
- **GitHub**: https://github.com/veritaschain
- **LinkedIn**: https://linkedin.com/company/110199945

---

## 謝辞

貢献者はリリースノートとウェブサイトで紹介されます。VCPをより良くするためにご協力いただきありがとうございます！

---

<p align="center">
  <strong>VeritasChain Standards Organization</strong><br/>
  <em>"Verify, Don't Trust"</em>
</p>
