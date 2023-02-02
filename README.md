# tagprtest

git-flow 検証
tagpr, git-pr-release 検証

## Git ブランチ運用検討

- git-flow ベース
- メインブランチは staging とし、 main は後追いとする。
- staging ブランチ進行時に tagpr により、バージョン設定プルリク作成、マージ後、タグ発行。
- タグ発行後、staging が develop にマージされる。

## private repo での確認

https://github.com/kinushu/tagprtest/settings/actions

Workflow permissions
Read and write permissions 指定

checked
Allow Github Actions to create and approve pull requests

