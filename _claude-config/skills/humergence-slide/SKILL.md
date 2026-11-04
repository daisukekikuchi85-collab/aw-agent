---
name: humergence-slide
description: >
  DaisukeのHUMERGENCE／グローセンパートナーのブランドテンプレートに沿った.pptxスライドを生成するスキル。
  「スライドを作って」「プレゼン資料を作って」「提案資料にして」「アウトラインをスライド化して」
  「テンプレートに合わせてスライドを作って」と言われたら必ずこのスキルを使う。
  テーマ・トピックだけが渡された場合はモードA（自動構成）、アウトラインや箇条書きが渡された場合は
  モードB（構造化変換）で起動する。HUMERGENCEおよびグローセンパートナーの資料作成には
  必ずこのスキルを使うこと。
---

# HUMERGENCE Slide Skill

## ブランドデザイン仕様

### カラーパレット
| 役割 | 色名 | HEX |
|------|------|-----|
| プライマリ（タイトル・アクセント） | ブランドブルー | `#0078A8` |
| セカンダリ（ステップラベルなど） | ティール | `#007B8F` |
| アクセント1（強調ラベル） | オレンジ | `#E87722` |
| アクセント2（警告・否定ラベル） | レッド | `#CC2200` |
| ニュートラル（グレーラベル） | ミディアムグレー | `#7F7F7F` |
| 背景 | ホワイト | `#FFFFFF` |
| ボーダー/ライン | ライトグレー | `#CCCCCC` |
| セクション細ライン | ライトブルー | `#5BA3C9` |
| テキスト（本文） | ダークグレー | `#404040` |
| テキスト（見出し） | チャコール | `#333333` |

### タイポグラフィ
- **見出しフォント**: `BIZ UDPGothic`（環境になければ `Noto Sans CJK JP`、英語は `Calibri`）
- **本文フォント**: `BIZ UDPGothic`（同上）
- スライドタイトル: 28〜32pt、ブランドブルー（`#0078A8`）、太字
- セクション見出し: 20〜24pt、ホワイトまたはブランドブルー
- 本文: 14〜16pt、ダークグレー（`#404040`）
- キャプション/出典: 10〜11pt、グレー（`#7F7F7F`）

### スライドサイズ
- ワイド 16:9（960 × 540 pt）

### 共通フッター要素（全コンテンツスライド）
- 右下: `©Daisuke Kikuchi  All rights reserved.`（10pt、グレー）
- 右下角にHUMERGENCEロゴ（右上に配置する場合あり）
- ページ番号: 右下端（10pt、グレー）

---

## スライドタイプ別仕様

### タイプ1：表紙スライド (Cover)
- タイトル: ライン直上・左寄り（y≒2.0〜3.5）
- 水平区切りライン: スライド**真ん中** y=3.75、**左端x=0から全幅**（ブランドブルー、高さ0.05"）
- 下半分: 白
- 右下: HUMERGENCEロゴ（"The Unity of Human Nature"テキスト付き）
- フッターなし

### タイプ2：セクション区切りスライド (Section Divider)
- セクション名は**スライド縦中央**付近（y≒3.0）、24pt、ダークグレー
- セクション名の直下に二重ライン:
  - 上ライン（太）: ブランドブルー、幅≒27%
  - 下ライン（細）: **ライトブルー `#5BA3C9`**、幅≒95%
- コンテンツなし（シンプル）

### タイプ3：標準コンテンツスライド (Content)
- 左上: スライドタイトル（28pt、ブランドブルー）
- 右上: ロゴ（小）
- コンテンツエリア: タイトル下から80%の領域
- フッター: `©Daisuke Kikuchi  All rights reserved.` + ページ番号

### タイプ4：テーブルスライド (Table)
- ヘッダー行: ブランドブルー背景（`#0078A8`）、ホワイトテキスト、太字、14pt
  - 実装: `addTable` の各ヘッダーセルに `fill: { color: BRAND.blue }` を **per-cell** で指定（行レベルのfillは効かないため必ずセル単位で指定すること）
- データ行: 白背景、ダークグレーテキスト、12〜13pt
- 外枠: ブランドブルー（1.5pt）
- 内側罫線: ライトグレー（0.75pt）

### タイプ5：ラベル付きリストスライド (Labeled List)
- 左カラム: ラベルボックス（ブランドカラー背景、ホワイトテキスト、**角丸なし四角形**）
- 右カラム: 箇条書き（黒丸・ブランドブルー、本文テキスト）
- ラベルの色バリエーション:
  - アクティブ/強調: ブランドブルー（`#0078A8`）
  - ニュートラル: グレー（`#7F7F7F`）
  - 警告/否定: レッド（`#CC2200`）
  - アクション: オレンジ（`#E87722`）
- ラベルは矢印型（pentagon shape）でステップ感を出す場合あり
- 下部サマリーボックス: ライトグレー背景、13pt、ボーダーあり

### タイプ6：フロー図スライド (Flow Diagram)
- ボックス: ブランドブルーまたはオレンジのボーダー（1.5pt）、白背景
- 矢印: ブランドブルーまたはオレンジ塗りつぶし
- ボックスラベル（上部）: ブランドブルーテキスト、太字
- ボックスコンテンツ: ダークグレー、12pt
- 左右2カラム構造が多い（比較・対比）
- カラム下部サマリー: ライトグレー背景ボックス

### タイプ7：図解スライド (Diagram)
- ベン図・マトリクスなど概念図
- 円の色: ブランドパレット（半透明）
- ラベル: ダークグレー、14〜16pt、太字
- 補助ラベルボックス: ブランドカラーボーダー

---

## モード別ワークフロー

### モードA：テーマ/トピック → 自動スライド構成

**トリガー**: テーマ・キーワードのみが渡された場合

**ステップ:**
1. テーマからスライド構成案（5〜12枚）を提示し、Daisukeに確認
2. 承認後、各スライドのタイプと内容を決定
3. pptxgenJSで生成（`pptxgenjs.md`を参照）
4. QAを実施しファイルを出力

**構成の定番パターン（HUMERGENCEコンテンツ向け）:**
```
1. 表紙
2. セクション区切り（背景・問題提起）
3〜4. 現状・課題スライド（ラベル付きリスト or フロー）
5. セクション区切り（フレームワーク紹介）
6〜8. コンセプト説明（図解 or コンテンツ）
9. まとめ（テーブル or リスト）
10. 表紙（エンドスライド）
```

### モードB：アウトライン/箇条書き → スライド化

**トリガー**: 構造化されたアウトライン・箇条書き・メモが渡された場合

**ステップ:**
1. 渡された内容を解析し、各スライドにマッピング
2. スライドタイプを自動判定（テーブル→タイプ4、ステップ→タイプ5、比較→タイプ6など）
3. pptxgenJSで生成
4. QAを実施しファイルを出力

---

## 実装ガイド（pptxgenJS）

pptxgenJSを使用する。詳細は pptxスキル（document-skills の pptx）の pptxgenjs の説明を参照。

### 基本セットアップ
```javascript
const pptx = new PptxGenJS();
pptx.layout = 'LAYOUT_WIDE'; // 16:9

// ブランドカラー定数
const BRAND = {
  blue: '0078A8',
  teal: '007B8F',
  orange: 'E87722',
  red: 'CC2200',
  gray: '7F7F7F',
  darkGray: '404040',
  charcoal: '333333',
  lightGray: 'CCCCCC',
  white: 'FFFFFF',
};

const FONT_JP = 'BIZ UDPGothic'; // フォールバック: 'Noto Sans CJK JP'
const FONT_EN = 'Calibri';
```

### 共通フッター追加ヘルパー
```javascript
function addFooter(slide, pageNum) {
  slide.addText('©Daisuke Kikuchi  All rights reserved.', {
    x: 0.3, y: 7.0, w: 8.0, h: 0.25,
    fontSize: 9, color: BRAND.gray, fontFace: FONT.en,
  });
  slide.addText(String(pageNum), {
    x: 9.2, y: 7.0, w: 0.5, h: 0.25,
    fontSize: 9, color: BRAND.gray, align: 'right', fontFace: FONT.en,
  });
}
```

### セクション区切りスライドヘルパー
```javascript
function addSectionSlide(pptx, title) {
  const slide = pptx.addSlide();
  // セクションタイトル（左下寄り）
  slide.addText(title, {
    x: 0.4, y: 2.8, w: 8.0, h: 0.6,
    fontSize: 24, color: BRAND.charcoal, fontFace: FONT.jp,
  });
  // 太ライン（ブランドブルー）
  slide.addShape(pptx.ShapeType.rect, {
    x: 0.4, y: 3.45, w: 3.5, h: 0.06,
    fill: { color: BRAND.blue }, line: { type: 'none' },
  });
  // 細ライン（ライトグレー）
  slide.addShape(pptx.ShapeType.rect, {
    x: 0.4, y: 3.52, w: 9.0, h: 0.03,
    fill: { color: BRAND.lightGray }, line: { type: 'none' },
  });
  return slide;
}
```

### ラベル付きリスト（ステップ型）ヘルパー
```javascript
// labelColor: 'blue' | 'gray' | 'red' | 'orange'
function addLabeledRow(slide, label, bullets, yPos, labelColor = 'blue') {
  const colorMap = {
    blue: BRAND.blue, gray: BRAND.gray,
    red: BRAND.red, orange: BRAND.orange,
  };
  slide.addShape(pptx.ShapeType.rect, {
    x: 0.4, y: yPos, w: 1.8, h: 0.65,
    fill: { color: colorMap[labelColor] },
    line: { type: 'none' },
  });
  slide.addText(label, {
    x: 0.4, y: yPos, w: 1.8, h: 0.65,
    fontSize: 13, color: BRAND.white, bold: true,
    align: 'center', valign: 'middle', fontFace: FONT.jp,
  });
  const bulletText = bullets.map(b => ({ text: b, options: { bullet: { type: 'bullet', code: '25CF', color: BRAND.blue } } }));
  slide.addText(bulletText, {
    x: 2.4, y: yPos, w: 7.0, h: 0.65,
    fontSize: 13, color: BRAND.darkGray, fontFace: FONT.jp,
    valign: 'middle',
  });
}
```

---

## QAチェックリスト

生成後に必ず確認する:

- [ ] タイトルはブランドブルー（`#0078A8`）になっているか
- [ ] フッターに `©Daisuke Kikuchi  All rights reserved.` とページ番号が入っているか
- [ ] フォントは游ゴシック（または Calibri）か
- [ ] ラベルボックスのテキストが溢れていないか
- [ ] セクション区切りスライドに不要なフッターが入っていないか
- [ ] 表紙スライドにページ番号が入っていないか
- [ ] テキストがスライド端に切れていないか（最低 0.3" マージン）

詳細QA手順は pptxスキル（document-skills の pptx）の QAセクションを参照。

---

## 出力

- ファイル名: `[テーマ]_slide_YYYYMMDD.pptx` 形式
- 保存先: `outputs/` フォルダ
- 生成後、保存したパスをオーナーに伝える

## 注記

このスキルで生成したファイルは **PowerPointでの微調整を前提としたたたき台**です。
カラー・フォント・レイアウト構造は再現されますが、以下はPowerPoint側での手作業を推奨します：
- ロゴ画像の配置
- フォントレンダリングの微調整
- 図解・アイコン類の追加
