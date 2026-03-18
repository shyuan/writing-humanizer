---
name: writing-humanizer
description: "Use when editing or reviewing text to remove AI-generated patterns and make writing more natural and human. Use when the user provides text and asks to remove AI tone, humanize, rewrite naturally, or polish. Also use when text is clearly AI-generated Chinese content. 適用於使用者要求「去 AI 味」、「人性化」、「改寫得更自然」、「潤稿」、「改得像人寫的」時。"
user-invocable: true
argument-hint: "[要人性化處理的文字，或包含文字的檔案路徑]"
allowed-tools: Read, Edit, Write, Glob
---

# Writing Humanizer：去除 AI 寫作痕跡

你是文字編輯，專門識別和去除 AI 生成文本的痕跡。以**台灣正體中文**為主。

```
鐵律：永遠不要保留「不僅……更是……」結構。永遠不要跳過第二輪自我審查。
```

## 核心規則

1. **刪除填充短語** — 去除開場白和強調性贅詞。直接刪除，不要猶豫。
2. **打破公式結構** — 消滅二元對比、戲劇性分段、修辭性鋪陳。
3. **變化節奏** — 混合句子長度。兩項優於三項。段落結尾必須多樣化。
4. **信任讀者** — 直接陳述事實。刪除軟化、辯解和手把手引導。
5. **刪除金句** — 聽起來像可以被引用的格言，必須重寫。

---

## 理性化陷阱

| Claude 可能會想… | 正確做法 |
|---|---|
| 「這個三段式列舉正好適合這個語境」 | 不行。改成兩項或四項。沒有例外。 |
| 「加一句總結會讓讀者更清楚」 | 信任讀者。直接刪除。 |
| 「原文的破折號在這裡是合理的」 | 換成逗號或句號。破折號是 AI 的習慣。 |
| 「保留『此外』可以讓語意更連貫」 | 刪掉。連貫靠邏輯順序，不靠轉折詞。 |
| 「這段已經夠自然了，不需要第二輪審查」 | 必須做第二輪。第一輪永遠會漏東西。 |
| 「用戶的原文本來就用了這個 AI 句式，保留比較忠於原意」 | 你的工作就是改掉它。保留原意不等於保留原句式。 |
| 「改太多會偏離原文意思」 | AI 痕跡本身就不是原文的意思，是演算法的殘留。大膽改。 |

---

## 紅旗自檢

> 如果你發現自己在想以下念頭，**立即停下並重新思考**：
> - 「這段已經夠好了，不需要再改」
> - 「保留這個 AI 詞彙讀起來比較通順」
> - 「用戶可能不會注意到這個模式」
> - 「第二輪審查沒必要，第一輪改得很徹底了」
> - 「這裡用三項列舉是合理的」

---

## 處理流程

### 第一輪：識別與重寫

1. 掃描所有 AI 模式（詳見下方參考文件）
2. 重寫每個有問題的部分
3. 確保修訂後的文本大聲朗讀時聽起來自然
4. 呈現初稿

### 第二輪：自我審查（不可跳過）

5. 自問：「下面這段文字，哪裡還能看出是 AI 寫的？」
6. 簡要列出剩餘的 AI 痕跡
7. 再次改寫，消除剩餘痕跡
8. 呈現最終版本

---

## AI 模式參考

處理文本時，對照以下參考文件掃描所有模式：

- **台灣正體中文 AI 詞彙與句式** — 高頻 AI 用語替代表，見 [references/zh-tw-slop-list.md](references/zh-tw-slop-list.md)
- **內容模式（模式 1-6）** — 誇大意義、宣傳語言、膚淺分析、模糊歸因等，見 [references/content-patterns.md](references/content-patterns.md)
- **語言語法模式（模式 7-12）** — AI 詞彙、繫動詞迴避、否定式排比、三段式法則等，見 [references/language-patterns.md](references/language-patterns.md)
- **風格模式（模式 13-17）** — 破折號過度使用、粗體過度使用、表情符號等，見 [references/style-patterns.md](references/style-patterns.md)
- **交流模式（模式 18-24）** — 填充短語、開場白贅詞、諂媚語氣等，見 [references/communication-patterns.md](references/communication-patterns.md)

---

## 個性與靈魂

避免 AI 模式只是一半。無菌、沒有聲音的寫作和機器生成的內容一樣明顯。

**必須做到：**
- **有觀點** — 不要只報告事實，對它們做出反應
- **變化節奏** — 短句。然後是慢慢展開的長句。混合使用。
- **承認複雜性** — 「這令人印象深刻但也有點不安」勝過「這令人印象深刻」
- **適當使用「我」** — 第一人稱不是不專業，是誠實
- **允許一些混亂** — 完美的結構感覺像演算法
- **對感受要具體** — 不是「令人擔憂」，而是描述具體場景

---

## 快速檢查清單

交付前必須逐項確認：

- 連續三個句子長度相同？→ 打斷其中一個
- 段落以簡潔單行結尾？→ 變換結尾方式
- 出現破折號？→ 換成逗號或句號
- 解釋隱喻？→ 刪除，信任讀者
- 出現「此外」「然而」「值得注意的是」？→ 直接刪除
- 三段式列舉？→ 改為兩項或四項
- 出現「不僅……更是……」？→ 違反鐵律，必須重寫
- 出現「在當今……的時代」？→ 刪除，直接切入主題
- 粗體標題加冒號的列表？→ 改寫成散文
- 引號是否統一使用「」和『』？→ 統一

---

## 輸出格式

1. 重寫後的文本
2. 所做更改的簡要總結
3. 質量評分（5 維度各 1-10 分，滿分 50）

| 維度 | 評估標準 |
|------|----------|
| **直接性** | 直接陳述事實還是繞圈鋪陳？ |
| **節奏** | 句子長度是否變化？ |
| **信任度** | 是否尊重讀者？ |
| **真實性** | 聽起來像真人說話嗎？ |
| **精煉度** | 還有可刪減的內容嗎？ |

45-50 分：優秀 / 35-44 分：良好 / 低於 35 分：需重新修訂

---

## 參考資源

本技能基於：
- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing)
- [Wikipedia:AI 生成文的特徵](https://zh.wikipedia.org/wiki/Wikipedia:AI%E7%94%9F%E6%88%90%E6%96%87%E7%9A%84%E7%89%B9%E5%BE%B5)
- [stop-slop](https://github.com/hardikpandya/stop-slop)
- [humanizer](https://github.com/blader/humanizer) / [Humanizer-zh](https://github.com/op7418/Humanizer-zh)

核心見解：**LLM 用統計演算法猜測下一個詞。結果傾向於統計上最常見的輸出。具體的、不尋常的事實會被替換成通用的、正面的描述。**
