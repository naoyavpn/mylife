# mylife

## Git環境構築の完全ガイド（Mac）

1. GitHubアカウントの作成
- [GitHub](https://github.com)にアクセス
- 「Sign up」をクリック
- ユーザー名、メールアドレス、パスワードを入力
- アカウントの認証を完了

2. Homebrewのインストール
```bash
# Homebrewをインストール
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Homebrewのパスを通す（zshの場合）
echo 'eval "$(/opt/homebrew/bin/brew shellenv)"' >> ~/.zshrc
source ~/.zshrc
```

3. Gitのインストール
```bash
# Gitをインストール
brew install git

# バージョン確認
git --version
```

4. Gitの初期設定
```bash
# ユーザー名とメールアドレスの設定
git config --global user.name "あなたの名前"
git config --global user.email "あなたのメールアドレス"

# 設定の確認
git config --list
```

5. SSHキーの設定（推奨）
```bash
# SSHキーの生成
ssh-keygen -t ed25519 -C "あなたのメールアドレス"

# SSHエージェントの起動
eval "$(ssh-agent -s)"

# SSHキーの追加
ssh-add ~/.ssh/id_ed25519

# 公開キーの表示（これをGitHubに登録）
cat ~/.ssh/id_ed25519.pub
```
- GitHubの[SSH and GPG keys](https://github.com/settings/keys)設定ページで公開キーを追加

## リポジトリのセットアップ

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
