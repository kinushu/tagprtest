# tagprtest

git-flow 検証
tagpr, git-pr-release 検証

## Git ブランチ運用検討

- git-flow のブランチ名を拝借する。
- リリースブランチは main
- develop ブランチにまとめ、バージョン、tagを付加していく。
- develop ブランチを、staging, main ブランチが追従する。

### 開発時

- develop ブランチから feature ブランチ切る。
- feature ブランチからdevelopへプルリクエスト、マージ。
- (tagprにより、 リリース用プルリクエスト自動生成。)

### リリース時

- リリース処理は、tagprプルリクで実施
- CHANGELOG整え、マージ後、タグ発行。
- タグ発行後、staging が タグ発行した箇所に進む。

## private repo での確認

https://github.com/kinushu/tagprtest/settings/actions

Workflow permissions
Read and write permissions 指定

checked
Allow Github Actions to create and approve pull requests

