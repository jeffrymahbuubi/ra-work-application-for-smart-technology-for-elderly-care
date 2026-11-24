# AI-Based Traffic-Light Risk Classification System for Older Adults

[繁體中文](#ai-高齡者風險紅黃綠燈分級系統)

The first group chose **Technology 2** from its older adult care proposal. The project explores how home care supervisors in Taiwan could use recent changes in a case, reported incidents, and service records to decide which cases to review first.

## What the supervisor sees

| Indicator | Meaning |
| --- | --- |
| Green · Routine review | The available information suggests the case is relatively stable. |
| Yellow · Monitor | A reported change needs continued monitoring. |
| Red · Review promptly | The case needs priority review by a supervisor. |
| Incomplete · Needs information | Some information needed to classify the case is missing. |

Each result shows the reason in plain language. The supervisor checks the underlying information and decides what follow-up is needed. This classroom prototype uses fictional cases to demonstrate review priority. Clinical decisions require professional judgment, and emergencies follow established response procedures.

## First classroom prototype

Start with a single browser page and two fictional inputs. Use rules that produce the same result for the same inputs so the group can check every result by hand. Later, students can compare an AI-assisted approach against this version and look at where their results differ.

1. Open this folder in Codex or Claude Code. Paste the prompt below into the chat.

   > Read `AGENTS.md` and the sample cases in `README.md`. Create a single `index.html` file that opens directly in a browser. Add two fields, “Recent change reported” and “Prompt supervisor review requested,” each with a blank, Yes, and No option. Add a “Check priority” button. Apply the first matching rule in this order. If prompt review is requested, show Red. If either field is blank, show Incomplete. If a recent change was reported, show Yellow. Otherwise, show Green. Show the result as text as well as color, with one sentence explaining the result. Use fictional data and tell me how to open and try the page.

2. Open the generated `index.html` in a browser. Enter each sample case, click **Check priority**, and compare the result and explanation with the table.
3. Ask the agent for one improvement based on what you observe. For example, if the Incomplete message is too vague, ask it to name the missing field. Then repeat the case with that field blank.

| Recent change reported | Prompt supervisor review requested | Expected result and reason |
| --- | --- | --- |
| No | No | Green · Neither a recent change nor a prompt review was reported. |
| Yes | No | Yellow · A recent change was reported. |
| No | Yes | Red · Prompt supervisor review was requested. |
| Blank | No | Incomplete · The recent change field is missing. |
| Blank | Yes | Red · The request for prompt review takes priority. |

As a group, decide which information a supervisor needs to understand each result and what an AI-assisted version would have to explain before you could compare it with the rules.

## AI 高齡者風險紅黃綠燈分級系統

[English](#ai-based-traffic-light-risk-classification-system-for-older-adults)

第一組選擇長照提案中的**技術二**。本專題探討臺灣的居家服務督導如何參考個案近期變化、事件通報與服務紀錄，判斷哪些個案需要優先檢視。

### 督導會看到什麼

| 指標 | 意義 |
| --- | --- |
| 綠燈（例行檢視） | 目前資料顯示個案狀況相對穩定。 |
| 黃燈（持續觀察） | 已通報的變化需要持續追蹤。 |
| 紅燈（優先檢視） | 需要由督導優先檢視。 |
| 資料不完整（待補資料） | 缺少判斷優先順序所需的資料。 |

每項結果會用簡單的文字說明原因。督導會核對相關資料，再決定如何追蹤。本課堂原型使用虛構個案示範檢視的優先順序。臨床決策須由專業人員判斷，緊急狀況依既有通報與應變流程處理。

### 第一版課堂原型

先做一個可開啟的網頁，用兩個欄位輸入虛構個案的資訊。相同的輸入應得到相同的結果，這樣全組就能逐一核對。之後可以試做 AI 輔助版本，比較兩個版本在哪些情況下會得出不同結果。

1. 在 Codex 或 Claude Code 開啟這個資料夾，將下方提示詞貼到對話框。

   > 請先閱讀 `AGENTS.md` 和 `README.md` 的範例個案。建立一個可直接用瀏覽器開啟的 `index.html`。加入「是否通報近期變化」和「是否請督導優先檢視」兩個欄位，每欄可選空白、是或否。加入「查看優先順序」按鈕。依序判斷，遇到第一個符合的條件就顯示結果。若已請督導優先檢視，顯示紅燈。若任一欄空白，顯示資料不完整。若已通報近期變化，顯示黃燈。其餘情況顯示綠燈。用文字和顏色呈現結果，並用一句話解釋原因。請使用虛構資料，並告訴我怎麼開啟並試用網頁。

2. 用瀏覽器開啟產生的 `index.html`。依序輸入每筆範例，按下**查看優先順序**，再對照表格確認結果與原因。
3. 根據試用結果，請 AI 助手做一項改進。例如，如果「資料不完整」的訊息太籠統，就請它指出缺少哪個欄位。改完後，再用同一筆留白的範例測試一次。

| 是否通報近期變化 | 是否請督導優先檢視 | 預期結果與原因 |
| --- | --- | --- |
| 否 | 否 | 綠燈（未通報近期變化，也未請督導優先檢視。） |
| 是 | 否 | 黃燈（已通報近期變化。） |
| 否 | 是 | 紅燈（已請督導優先檢視。） |
| 空白 | 否 | 資料不完整（未填寫「是否通報近期變化」。） |
| 空白 | 是 | 紅燈（優先處理督導檢視的請求。） |

請全組討論督導需要哪些資訊才能理解每項結果，以及 AI 輔助版本需要解釋哪些判斷依據，才能和規則版本比較。
