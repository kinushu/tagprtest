# tagprtest

git-flow 検証
tagpr, git-pr-release 検証

https://github.com/kinushu/tagprtest/releases

## Git ブランチ運用検討

- git-flow ベース
- stagingブランチをバージョンタグ付加ブランチ,developからのマージブランチ, 検証バージョンとしていく。
- mainブランチをリリースブランチとする。 staging に追従する。

### 開発時

- developブランチからfeatureブランチ切る。
- featureブランチからdevelopへプルリクエスト、マージ。
- (git-pr-releaseにより、 developをstagingへマージ依頼するプルリクエスト自動生成。)

### リリース時

- リリース処理開始は、developをstagingへマージすることでスタート。(上記の自動生成プルリク使用。)
- staging ブランチ進行時に tagpr により、バージョン設定プルリク作成。
  - CHANGELOG.md の内容をプルリク内で調整。
- マージ後、タグ発行。
  - Release内容が自動生成される。
- タグ発行後、staging が develop にマージされる。

## Private repository での確認

GitHub Actions の設定確認。

https://github.com/kinushu/tagprtest/settings/actions

- Workflow permissions
  - Read and write permissions 指定
- Allow Github Actions to create and approve pull requests
  - チェックされている。
