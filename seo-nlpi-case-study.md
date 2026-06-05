# Felo Subtitles × NLPI 案例ページ SEO 優化建議

> ページ：https://ailisoncheng416.github.io/felo-landing/case-study-nlpi.html
> Canonical 予占：https://subtitles.felo.me/ja/case-study/nlpi
> 分析日：2026-06-05
> 製品：Felo Subtitles
> 市場：日本（JP）+ 国際公共図書館コミュニティ
> ページタイプ：D（Customer Case Study）

---

## 一、現状の SEO 健康度

| 項目 | 状態 | 評価 |
|---|---|---|
| `<title>` | ✅ 設定済（70 文字以内）| A |
| `<meta description>` | ✅ 設定済 | A |
| H1 | ✅ 存在（「8カ国・地域 14名の登壇者を、…」）| **B+**（製品名なし） |
| canonical | ✅ 予占済 | A |
| OG タグ | ✅ 完備（title/description/image/url/locale）| A |
| Twitter Card | ✅ 完備 | A |
| JSON-LD Article schema | ✅ + `about`/`mentions` | A |
| BreadcrumbList | ✅ | A |
| **FAQPage schema** | ❌ 無し | **C**（案例 page で機会損失） |
| **内部リンク（ブログへの誘導）** | ❌ 無し（5-8 本推奨）| **D**（最大の改善ポイント） |
| 画像 `width/height/loading/decoding` | ✅ 完備 | A |
| Hero 画像 `fetchpriority="high"` | ✅ | A |
| 案例 excerpt の crawlable 化 | ✅ 本文に出現 | A |
| アクセシビリティ alt | ✅ 記述的 | A |

**総合**：**B+（内部リンクと FAQ schema 追加で A になる）**

---

## 二、キーワード戦略

### 2.1 ターゲットキーワードマトリクス（手動分析）

| 優先度 | キーワード | 推定月検索量 | 意図 | 現在の埋め込み |
|---|---|---|---|---|
| **P0** | 国際会議 字幕 / 翻訳 | 200-500 | 商業 | 部分的（タイトル・本文）|
| **P0** | 多言語字幕 ツール | 100-300 | 商業 | ✅ 本文 |
| **P0** | リアルタイム翻訳 字幕 | 300-700 | 商業 | ✅ 本文 |
| P1 | 国際フォーラム 多言語化 | 30-80 | 情報 | ✅ Hero / H1 |
| P1 | AI同時通訳 | 200-400 | 商業 | ❌ 未掲載 |
| P1 | カンファレンス 字幕 | 50-150 | 商業 | △ 一部 |
| P2 | APPLFTW | <10 | ナビ（イベント名） | ✅ |
| P2 | 国立公共資訊図書館 | <20 | ナビ（顧客名） | ✅ |
| P2 | 法人 字幕 ツール / エンタープライズ | 50-100 | 商業 | ✅ |

### 2.2 H1 のキーワード密度評価

現在の H1：「8カ国・地域 14名の登壇者を、1日でリアルタイム多言語化。」

- ✅ **Outcome ファースト**（数字先頭、Helpfeel / さくらインターネット 慣例準拠）
- ✅ **「多言語化」** が含まれる（P0 関連語）
- ⚠️ **「Felo Subtitles」未出現** — SEO 上は title で補完されるが、ページ内のテキストフィールド充実度がやや弱い

**判断**：現 H1 は人間訴求と SEO のバランスが取れている。変更不要。**「Felo Subtitles」は本文 / sidebar / Stats 周辺で頻出するため Entity 認識は問題なし**。

---

## 三、必須修正（P0）

### 3.1 内部リンク追加（最大効果）

ブログ記事への内部リンク 5-8 本を本文内に自然に追加。すべて 200 OK 確認済み：

| # | 記事タイトル（想定）| URL | 推奨配置箇所 | アンカーテキスト案 |
|---|---|---|---|---|
| 1 | 多言語字幕の作成方法 | `subtitles.felo.me/blog/multilingual-subtitle-creation-method-2` | 「選定の決め手 ③ カスタム語彙表」段落 | **多言語字幕の作成方法** |
| 2 | オンラインセミナーの多言語対応 | `subtitles.felo.me/blog/online-seminar-multilingual-support-2` | 「論壇当日の成果」末尾 | **オンラインセミナーの多言語対応ガイド** |
| 3 | 多言語会議のコツ | `subtitles.felo.me/blog/multilingual-meeting-tips` | 「導入の背景」段落（課題説明箇所）| **多言語会議の運営ノウハウ** |
| 4 | Web 会議翻訳ツール比較 | `subtitles.felo.me/blog/video-conference-translation-comparison-2` | 「選定の決め手」イントロ | **Web会議翻訳ツールの比較** |
| 5 | 英語会議の字幕ガイド | `subtitles.felo.me/blog/english-meeting-subtitle-guide` | 「論壇当日の成果」中盤（Vicki McDonald 段落）| **英語キーノートを字幕化する方法** |
| 6 | Zoom AI 同時通訳 | `subtitles.felo.me/blog/zoom-simultaneous-interpretation-ai-2` | （オプション）「選定の決め手 ①」内 | **Zoom 等での AI 同時通訳活用** |

→ **6 本実装で目標達成**。原則「該当 section 内に自然に埋め込み、記述的アンカーテキスト」。

### 3.2 FAQPage Schema 追加

案例 page だが、「他社からの問い合わせ想定 Q&A」を可視 FAQ として末尾に追加し、FAQPage schema を仕込むことで rich result 機会を獲得：

```html
<section class="py-12 bg-gray-50">
  <div class="max-w-3xl mx-auto px-6">
    <h2 class="text-2xl font-bold mb-6 text-center">本案例についてよくあるご質問</h2>
    <details>
      <summary>NLPI と同規模の国際イベントで、Felo Subtitles はどう活用できますか？</summary>
      <p>NLPI 事例と同様、8 カ国・地域規模の論壇でもエンタープライズ法人契約により、運営チーム全員での多アカウント連携と並列セッション運用が可能です。</p>
    </details>
    <details>
      <summary>QR コード共有機能の使い方は？</summary>
      <p>会場の参加者は QR コードをスマートフォンで読み取るだけで、リアルタイム翻訳字幕を自分のデバイスで受け取れます。</p>
    </details>
    <details>
      <summary>カスタム語彙表で何ができますか？</summary>
      <p>業界固有の専門用語や固有名詞（例：APPLFTW・IFLA など）を事前登録することで、論壇の文脈に沿った安定した翻訳精度を維持できます。</p>
    </details>
  </div>
</section>
```

JSON-LD `FAQPage` schema を `<head>` の `</script>` 群に追加し、本文と完全一致させる。

---

## 四、推奨修正（P1）

### 4.1 画像 alt にキーワード補強

現在の alt：
- `applftw-hero.jpg` → 「2026 APPLFTW 会場 — 多数の参加者と主スクリーン・サブスクリーンに Felo Subtitles のリアルタイム字幕が表示」 ✅ すでに optimal
- `applftw-mcdonald-keynote.jpg` → 「元 IFLA 会長 Ms. Vicki McDonald 氏のキーノート — 画面下に Felo Subtitles の英中双方向リアルタイム字幕が表示されている様子」 ✅ optimal

**判断**：画像 alt は既に十分。変更不要。

### 4.2 関連事例リンク（オプション）

ページ末尾 / CTA 直前に「**関連事例**」セクションを設け、Fukuoka 案例へのカードリンクを置く：

```html
<a href="https://subtitles.felo.me/ja/showcase/fukuoka" class="case-card-link">
  <img src="..." alt="福岡 Felo Translator 導入事例">
  <span>福岡 — 20 言語観光案内 + ワーケーションカンファレンス</span>
</a>
```

→ 案例ページ間の内部リンク強化 + 「他案例も見たい」流入の確保。

---

## 五、任意改善（P2）

### 5.1 Article schema に `keywords` プロパティ追加

```json
"keywords": ["国際会議 字幕", "多言語字幕", "リアルタイム翻訳", "APPLFTW", "国立公共資訊図書館", "Felo Subtitles 導入事例"]
```

### 5.2 og:image を実画像に置換

現在：`og-image.jpg`（予占）→ 実際の applftw-hero.jpg にスイッチ（または `og-image.jpg` を別途生成）。

---

## 六、実装優先度

| 優先度 | アクション | 所要 | 効果 |
|---|---|---|---|
| **P0-1** | 内部リンク 6 本追加（本文内に自然配置）| 30 分 | SEO + 訪問者教育 |
| **P0-2** | FAQPage schema 追加 + 末尾 FAQ セクション | 20 分 | Rich result 機会 |
| P1 | 関連事例（Fukuoka）リンク追加 | 10 分 | 内部リンク強化 |
| P2 | Article schema `keywords` 追加 | 5 分 | Entity 認識補強 |
| P2 | og:image 実画像化 | 5 分 | SNS 共有時の見栄え |

---

## 七、予期される効果

| 指標 | 現在 | 目標（3-4 週間後）|
|---|---|---|
| 「国際会議 字幕」検索 | 未進入 | Top 20 |
| 「多言語字幕 ツール」検索 | 未進入 | Top 30 |
| 案例 page からブログへの flow | 0 | 5-10% CTR |
| 平均滞在時間 | 未測定 | + 30 秒（FAQ + 関連事例で延長） |
| 「APPLFTW」「NLPI 字幕」検索 | 未測定 | Top 5（specific entity）|

---

## 八、URL probe 結果（reference）

すべて **200 OK** 確認済み（実装前 verify 完了）：

```
200 https://subtitles.felo.me/blog/multilingual-subtitle-creation-method-2
200 https://subtitles.felo.me/blog/online-seminar-multilingual-support-2
200 https://subtitles.felo.me/blog/multilingual-meeting-tips
200 https://subtitles.felo.me/blog/video-conference-translation-comparison-2
200 https://subtitles.felo.me/blog/english-meeting-subtitle-guide
200 https://subtitles.felo.me/blog/zoom-simultaneous-interpretation-ai-2
200 https://subtitles.felo.me/blog/webex-realtime-translation-2
200 https://subtitles.felo.me/blog/zoom-bot-free-translation
```
