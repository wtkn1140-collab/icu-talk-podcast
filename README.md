# ICUトーク 音声版

YouTube「ICU Talk」（小林宏維・小谷祐樹）の新着を音声化し、Apple Podcasts で聴けるようにする仕組み。
構成は `~/claude/tsundoku-podcast` と同じ（取得は Mac、配信は GitHub Pages）。

## スマホで聴く
- フィード: https://wtkn1140-collab.github.io/icu-talk-podcast/feed.xml
  （Apple Podcasts → ライブラリ →「…」→「URLで番組をフォロー」）
- プレーヤー: https://wtkn1140-collab.github.io/icu-talk-podcast/

## Mac 側
- 自動実行: `~/Library/LaunchAgents/com.icutalk.podcast.plist` → `run.sh`（2時間ごと）
- ログ: `logs/update.log`
- 手動で今すぐ取得: `./run.sh`
- 自動実行を止める: `launchctl bootout gui/$(id -u) ~/Library/LaunchAgents/com.icutalk.podcast.plist`
- 音声は `audio-site/`（リポジトリ icu-talk-podcast-audio）に置かれ、最新15話を残す
