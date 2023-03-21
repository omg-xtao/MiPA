# Change Log

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/)
and this project adheres to [Semantic Versioning](http://semver.org/).

## [Unreleased]



## [0.2.1] 2023-03-22

### Changed

- 使用するMiPACのバージョンを`0.4.2`に

## [0.2.0] 2023-03-20

### Added

- `setup_hook` イベントが追加されました
  - `load_extension` 等はこのイベントで行うことを推奨します
- `ExtensionNotLoaded` 例外が追加されました

### Changed

- **BREAKING CHANGES** 以下のメソッドが非同期になります
  - Cogs内の `setup` 関数
  - `add_cog`
  - `remove_cog`
  - `load_extension`

### Fixed

- `tasks.loop` をクラス内で使用すると `self` が受け取れない

## [0.1.2] 2023-03-14

### Added

- ✨ added event `on_achievement_earned`.
- ✨ added `disconnect` method to `Client` class.

### Fixed

- incorrect URL for streaming API #16, #17

### Changed

- 使用するMiPACのバージョンを`0.4.1`に

## [0.1.1] 2023-01-18

### Added

- ✨ feat: support all notifications #MA-11
  - `on_user_follow` when you follow a user
  - `on_user_unfollow` when you unfollow a user
  - `on_user_followed` when someone follows you
  - `on_mention` when someone mentions you
  - `on_reply` when someone replies to your note
  - `on_renote` when someone renote your note
  - `on_quote` when someone quote your note
  - `on_reaction` when someone react to your note
  - `on_poll_vote` when someone vote to your poll
  - `on_poll_end` when a poll is ended
  - `on_follow_request` when someone send you a follow request
  - `on_follow_request_accept` when someone accept your follow request

### Changed

- 使用するMiPACのバージョンを`0.4.0`に

### Fixed

- 🐛 fix: ws reconnect
- 🐛 fix: Separate unread chat message

## [0.1.0] 2022-12-24

### Added

- ✨ feat: add .flake8 config.
- ✨ feat: To be able to capture notes.
- ✨ added event `on_note_deleted`.
- ✨ added event `on_reacted`.
- ✨ added event `on_unreacted`.
- ✨ added `router` property a `Client` class attributes.
    - 💡 Direct instantiation of the `Router` class is deprecated.
- [@omg-xtao](https://github.com/omg-xtao) ✨ feat: added `hybridTimeline` channel [#9](https://github.com/yupix/MiPA/pull/9).


### Changed

- ⬆️ feat(deps): update mipac update mipac version.
- ✨ chore: Changed `parse_` lineage functions to asynchronous.
- 💥 feat: **BREAKING CHANGE** Change event name `on_message` from `on_note`.
- 💥 feat: **BREAKING CHANGE** Required Python version is 3.11.

### Fixed

- 🐛 fix: not working command Framework.
- 🐛 fix: Chat related stuff is flowing `on_message`.
    - 💡 Please use `on_chat` in the future!
