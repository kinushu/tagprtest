# tagprtest

git-flow 検証
tagpr, git-pr-release 検証

## Git ブランチ運用検討

git-flow ベースに、メインブランチは staging とし、 main は後追いとする。

staging ブランチ進行後、 develop にマージされる。

## private repo での確認

https://github.com/kinushu/tagprtest/settings/actions

Workflow permissions
Read and write permissions 指定

checked
Allow Github Actions to create and approve pull requests

