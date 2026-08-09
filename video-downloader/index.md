---
title: Video Downloader
---

# Video Downloader

YouTube・Instagram・TikTok・X など約1,800サイト([yt-dlp](https://github.com/yt-dlp/yt-dlp) 対応サイト)から動画を高解像度でダウンロードできる、**ローカル実行**のWebアプリです。Whisperによる文字起こしにも対応しています。

📦 **ソースコード / インストール方法**: [github.com/selo-git/video-downloader](https://github.com/selo-git/video-downloader)

## 主な機能

- **高解像度ダウンロード** — 最高画質(自動)/ 2160p〜480p / 音声のみ(m4a・mp3・opus・wav)
- **複数URL・プレイリスト一括ダウンロード** — 1行に1URL。プレイリストは自動で個別ジョブに展開
- **同時ダウンロード(1〜5並列)とキャンセル** — 中断ファイルは自動削除
- **文字起こし(Whisper)** — 動画の音声をローカルAIでテキスト化(.txt / タイムスタンプ付き .srt)。言語(日本語・英語・混在・自動)に応じて最適モデルを自動選択 ※Apple Silicon Mac
- **字幕・サムネイル保存 / 区間指定ダウンロード / ダウンロード履歴**
- **ブラウザCookie連携** — ログインが必要なサイトにも対応
- **設定** — 保存先フォルダ・ファイル名テンプレートを自由に変更

## 動作環境

- macOS + Python 3.9+ + ffmpeg
- サーバーにデータを送らない完全ローカル動作(このサイト上では動作しません)

## セットアップ(3ステップ)

```bash
git clone https://github.com/selo-git/video-downloader.git
cd video-downloader
python3 -m venv .venv && .venv/bin/pip install -r requirements.txt
.venv/bin/python app.py   # → http://localhost:3456 を開く
```

## 注意事項

本ツールは、ご自身がアップロードした動画や、権利者がダウンロードを許可しているコンテンツの保存を目的としています。各サイトの利用規約と著作権法を遵守してご利用ください。

## ライセンス

[MIT License](https://github.com/selo-git/video-downloader/blob/main/LICENSE)
