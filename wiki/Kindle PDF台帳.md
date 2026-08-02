---
type: operations
created: 2026-06-17
updated: 2026-07-31
tags: [書籍, Kindle, 台帳, 第二の脳]
---

# Kindle PDF台帳

Kindle PDFと読書Wikiを「第二の脳」として運用するための管理ページ。
全PDFの整理状況は [[Kindle本PDF未整理リスト]] を母艦にし、このページでは信頼度・次アクション・問いへの接続を管理する。

## 現状

| 項目 | 状態 |
| --- | --- |
| Kindle PDF | 76件 |
| 要約＆概念マップ | 全PDF分作成済み |
| 主要入口 | [[wiki/index]], [[wiki/hot]], [[問いインデックス]] |
| 概念入口 | [[概念/概念インデックス]] |
| ローカル索引 | `.second-brain/second_brain.sqlite`（OCR全文込みで更新済み） |
| 機械台帳 | `.second-brain/kindle_pdf_inventory.csv` |
| OCR全文 | 76冊完了、失敗0件 |
| OCR品質確認 | [[OCR品質確認ノート]] |
| 次の重点 | `public-info-based` ページの原典OCR再確認、概念ハブの拡張 |

## 信頼度ラベル

| ラベル | 意味 | 扱い |
| --- | --- | --- |
| `highlight-based` | Kindle Highlights 等の抜粋・メモを主根拠に作成 | 回答根拠として使いやすい |
| `pdf-text-based` | PDF本文のテキスト層を主根拠に作成 | 回答根拠として使いやすい |
| `ocr-based` | 画像PDFをOCRして作成 | OCR誤認識に注意して使う |
| `public-info-based` | 目次・概要など公開情報を主根拠に作成 | 仮説メモとして扱う。現在は原典OCRで再確認可能 |
| `unknown` | 根拠の種類が未確認 | 次回メンテで確認 |

## 低信頼度・再確認候補

下記は既存メモ上で「画像スキャンPDF」「Kindle Highlightsなし」「公開情報をもとに作成」と記録されているため、第二の脳の回答では信頼度を明示する。全件OCR完了後は、必要に応じて原典OCRを検索して補強できる。

| 書籍ページ | 現ラベル | 次アクション |
| --- | --- | --- |
| [[イノベーションの競争戦略 要約＆概念マップ]] | `public-info-based` | 原典OCRで競争戦略の要点を再確認 |
| [[なぜ「できる人」の言うことを聞いてしまうのか 要約＆概念マップ]] | `public-info-based` | 原典OCRで認知バイアス・権威性の要点を再確認 |
| [[魏武注孫子 要約＆概念マップ]] | `public-info-based` | 原典OCRで兵法・戦略概念を再確認 |
| [[やさしいMCP入門 要約＆概念マップ]] | `public-info-based` | 原典OCRで技術要点を再確認 |
| [[AIを使って考えるための全技術 要約＆概念マップ]] | `public-info-based` | 原典OCRで実践手順を再確認 |
| [[データサイエンス超入門 要約＆概念マップ]] | `public-info-based` | 原典OCRで用語定義を再確認 |
| [[物流がわかる 要約＆概念マップ]] | `public-info-based` | 原典OCRで物流概念を再確認 |
| [[新しい「物流」の教科書 要約＆概念マップ]] | `public-info-based` | 原典OCRで実務アクションを再確認 |
| [[論文の教室 要約＆概念マップ]] | `public-info-based` | 原典OCRで論文作法を再確認 |
| [[ベストセラーコード 要約＆概念マップ]] | `public-info-based` | 原典OCRで分析観点を再確認 |

## 高優先で使える入口

| 用途 | 入口 |
| --- | --- |
| 蔵書全体から答えを探す | [[問いインデックス]] |
| 書籍単位で探す | [[wiki/index]] |
| 最近の関心から探す | [[wiki/hot]] |
| 概念横断で探す | [[概念/概念インデックス]] |
| 未整理・追加分を確認する | [[Kindle本PDF未整理リスト]] |
| OCR候補を確認する | [[OCR品質確認ノート]] |

## 本格案のローカル成果物

| 成果物 | 場所 | 用途 |
| --- | --- | --- |
| 機械台帳CSV | `.second-brain/kindle_pdf_inventory.csv` | PDFごとの対応Wiki・抽出可否を確認 |
| 機械台帳JSON | `.second-brain/kindle_pdf_inventory.json` | 自動処理・再生成用 |
| 全文検索SQLite | `.second-brain/second_brain.sqlite` | Wiki本文・OCRサンプル・OCR全文のローカル検索 |
| OCRサンプル | `.second-brain/ocr-samples/` | 少数ページOCRの品質確認 |
| OCR全文 | `.second-brain/ocr-full/` | 76冊分のOCRテキストと処理サマリー |

検索例:

```sh
python3 scripts/wiki-ops/kindle-second-brain.py search 物流 --limit 5
```

## 運用ルール

1. 新しいPDFを追加したら [[Kindle本PDF未整理リスト]] に登録する。
2. 要約ページを作成したら、この台帳の信頼度ラベルも確認する。
3. `public-info-based` のページを使って重要判断をする場合は、原典OCRまたはハイライトで補強する。
4. 同じ概念が3冊以上に出たら [[概念/概念インデックス]] へ追加を検討する。
5. よく使う問いが出たら [[問いインデックス]] に追加する。
6. OCRは全件実行前に [[OCR品質確認ノート]] のサンプル品質を確認する。

## 関連

- [[Kindle本PDF未整理リスト]]
- [[問いインデックス]]
- [[OCR品質確認ノート]]
- [[wiki/index]]
- [[wiki/hot]]
- [[概念/概念インデックス]]

#Kindle #読書 #第二の脳
