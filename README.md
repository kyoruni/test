# test
お試し用

## push

```bash
# 他の人が同じブランチに push してたら止める
git push --force-with-lease origin

# 問答無用で上書き
git push --force origin HEAD
```

## 最新のコードを取り込みたい

```bash
# hoge ブランチへ
git co hoge

# mainの先頭に hoge のコミットを載せ替える(マージコミットなし)
git rebase origin/main

## コンフリクトした場合は直してから 
 
# -A: 作業を丸ごとステージに登録
git add -A
git rebase --continue

# リモートを上書き
git push --force origin HEAD
```