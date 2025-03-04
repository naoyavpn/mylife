# mylife

## Gitセットアップ手順

1. GitHubでリポジトリを作成
- リポジトリ名：mylife
- 説明：私の人生を記録するリポジトリ
- README.mdファイルを含めて作成

2. ローカル環境での作業
```bash
# リポジトリのクローン
cd ~/Desktop/dev
git clone https://github.com/naoyavpn/mylife.git

# リポジトリに移動
cd mylife

# Gitの設定確認
git status
```

## 基本的なGitコマンド

1. 変更状態の確認
```bash
git status
```

2. 変更のステージング
```bash
git add ファイル名  # 特定のファイルを追加
git add .          # すべての変更を追加
```

3. 変更のコミット
```bash
git commit -m "コミットメッセージ"
```

4. リモートとの同期
```bash
git pull  # リモートの変更を取得
git push  # ローカルの変更をプッシュ
```

## 今後の予定
- 日々の記録
- 目標の設定と管理
- 進捗の記録
