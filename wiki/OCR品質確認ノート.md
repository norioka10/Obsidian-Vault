---
type: operations
created: 2026-06-17
updated: 2026-06-29
tags: [OCR, Kindle, 第二の脳]
---

# OCR品質確認ノート

Kindle PDFを全文検索へ接続するための品質確認ページ。
原典PDFは変更せず、機械台帳と検索索引はローカル成果物として `Obsidian Vault/.second-brain/` に置く。

## 集計

| 分類 | 件数 |
| --- | ---: |
| `pdf-text-based` | 0 |
| `pdf-text-partial` | 0 |
| `ocr-needed` | 70 |
| `ocr-full-completed` | 70 |
| `ocr-full-failed` | 0 |

## 現在の状態

全70冊のOCR全文化は完了済み。OCR本文はローカル成果物として `Obsidian Vault/.second-brain/ocr-full/` に保存する。

| 成果物 | 状態 |
| --- | --- |
| OCR全文 | 70冊完了 |
| OCR失敗 | 0件 |
| 一時ファイル | 0件 |
| 検索索引 | `.second-brain/second_brain.sqlite` 更新済み |
| 索引対象 | Wiki本文、OCRサンプル、OCR全文 |

## 再確認候補

`public-info-based` の要約ページは、作成時点では公開情報が主根拠だった。現在は原典OCRがあるため、重要判断に使う前に検索して補強できる。

| 用途 | 次アクション |
| --- | --- |
| 公開情報ベースの要約を使う | 原典OCRを検索し、要点・概念・実務アクションを自分の言葉で補強 |
| OCR誤認識が疑われる | 該当PDFまたはOCR全文を確認し、要約本文へは丸写しせず要点化 |
| 新しいPDFを追加する | 少数ページOCRで品質確認してから `ocr-full` と索引更新を実行 |

## 運用

1. OCR済みテキストはWiki本文へ貼らず、検索索引用のローカル成果物として扱う。
2. 要約ページを更新する場合は、本文丸写しではなく要点・概念・実務アクションへ変換する。
3. `public-info-based` のページは、原典OCRで裏取りしてから重要判断に使う。
4. 新しいPDFを追加した場合は、まず少数ページでOCR品質を確認する。

## 関連

- [[Kindle PDF台帳]]
- [[問いインデックス]]
- [[wiki/hot]]
