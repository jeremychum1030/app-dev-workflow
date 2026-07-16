---
name: app-dev-workflow
description: 通用 App 開發工作鏈模板 — 從商業模式到上線的全流程。載入後自動引導當前階段，含來自 Medic Agent/Posture AI/Micro-Log 的真實商業模式庫。
version: 3.2.0
---

# App 開發工作鏈 v2

> `/skill app-dev-workflow` → 顯示當前進度 + 下一步行動
> 適用: Flutter / React / Vue / SwiftUI / HTML 任何 App

---

## 7 階段總覽

```
💰 Phase 0: 商業模式  📋 Phase 1: 策略     🎨 Phase 2: 設計
     ↓                     ↓                     ↓
 定價模型選擇          用戶 Jobs 地圖      Design System
 收入預測              競品分析矩陣        品牌語言
 用戶粘性設計          MVP 範圍定義        組件庫
     ↓                     ↓                     ↓
===================================================
🏗️ Phase 3: 架構     🔨 Phase 4: 構建     ✨ Phase 5: 打磨
     ↓                     ↓                     ↓
技術棧選定            逐功能 TDD 開發       視覺 QA
架構模式              代碼+設計審查迴圈      無障礙+效能
資料流設計                                   
     ↓                     ↓                     ↓
===================================================
🚀 Phase 6: 上線
     ↓
測試+安全+發布
```

---

## Phase 0: 商業模式與營收設計

> **先想清楚怎麼賺錢，再開始寫代碼。**
> 以下全部來自 5 個真實開發上線的 App 實戰經驗。

### 自動載入 Skills
`thinking-inversion` `thinking-first-principles`

---

### 📊 五大真實 App 商業模式對照

| App | 類型 | 定價 | 免費限制 | 核心變現邏輯 |
|-----|------|------|---------|-------------|
| **Posture AI** | AI 姿勢矯正 | HK$10/月 | 基礎掃描 | 百日火苗 Streak → 不想斷 |
| **Micro-Log** | 語音健康日誌 | HK$10/月 | 3次免費 | 數字保險庫 → 數據越多越離不開 |
| **Oasis Mind** | AI 心理陪伴 | Pro 會員 (HK$58/月) | 10次AI對話/週、5點/次 | 心靈植物養成 → 情感綁定 |
| **VIM** | 健身競賽 | HK$58/月 | 10次AI飲食/月 | 積分排行榜 + 沙盒挑戰 → 競技心理 |
| **Medic Agent** | 醫療健康平台 | 銀58/金108/白金208/鑽石388 | 基礎自查 | 人頭制 VIP → 鼓勵家庭共享 |

---

### 💰 六種定價模式（選擇最適合你的）

#### 模式 1: 低價微訂閱
```
定價: HK$8-15/月
試用: 3次免費 → 付費解鎖
心理: 「每日不到 0.3 元」→ 衝動消費友好
來源: Posture AI、Micro-Log
適合: 工具型 App、高頻使用、無網絡效應
```

#### 模式 2: 中價全功能會員
```
定價: HK$58/月
免費: 核心功能受限（10次/月 or 10次/週）
會員: 無限使用 + 獨享功能（競賽/排行榜/報告）
加購: AI報告 HK$28/次、全解鎖 HK$68
來源: VIM、Oasis Mind
適合: 有明確「免費→付費」升級路徑的 App
```

#### 模式 3: 分級 VIP 人頭制
```
銀 HK$58/月  → 僅本人
金 HK$108/月 → 共享 2 人
白金 HK$208/月 → 共享 3 人
鑽石 HK$388/月 → 共享 6 人
關鍵: 人頭制（非人均），長者70+免費、兒童半價
來源: Medic Agent
適合: 家庭/團隊型產品，有網絡效應
```

#### 模式 4: 虛擬貨幣/點數制
```
免費: 註冊送 20 點
消耗: 每次 AI 對話 5 點（非會員）
儲值: 購買點數包
VIP: 無限次對話，不需消耗點數
來源: Oasis Mind (心靈點數)、VIM (積分)
適合: AI 密集型產品，按用量計費
```

#### 模式 5: 積分經濟系統
```
賺取: 沙盒冠軍+60pts、月活躍+5pts、邀請朋友+20pts
兌換: 免費續會 580pts、AI報告 280pts、商城折價券 200pts
設計: 積分永不過期、不可轉讓、不可兌現
來源: VIM
適合: 有競賽/排行榜/社交屬性的 App
```

#### 模式 6: Freemium + 單次解鎖
```
免費核心功能 → HK$XX 永久解鎖 Pro
適合: 一次性工具、計算器類
```

---

### 🔥 用戶粘性工具箱（11 種實戰機制）

#### 🎮 遊戲化進度
| 機制 | 案例 | 心理原理 |
|------|------|---------|
| Streak 計數器 | Posture AI「百日火苗 Day 17」、Oasis Mind 連續簽到 | 連續不中斷的承諾 |
| 個人化指標 | Posture AI「脊椎年齡 22 歲」 | 想改善的數字 = 每日回來看 |
| 進度條+成就 | 「今日處方進度 2/3」、VIM 沙盒冠軍徽章 | 完成感 + 可視化進步 |
| 虛擬養成 | Oasis Mind「心靈植物」澆水成長 | 情感綁定、不想讓植物枯萎 |

#### 🔒 數據鎖定
| 機制 | 案例 | 心理原理 |
|------|------|---------|
| 數字保險庫 | Micro-Log「永久封存加密健康大數據」 | 數據越多越離不開 |
| 匯出價值 | Micro-Log「AI 生成門診 PDF」、Oasis Mind 週度情緒報告 | 看得見的產出 |
| 歷史累積 | Medic Agent 病歷記錄、VIM 歷史競賽成績 | 轉換成本高 |

#### ✨ 驚喜時刻
| 機制 | 案例 | 心理原理 |
|------|------|---------|
| AI 魔法動效 | Micro-Log「AI 煉金術」粒子爆散 | 等待=期待的魔法 |
| 個性化回饋 | Posture AI「本機 AI 為您深度調配」 | 偽定制感=低成本高感知 |
| 首次驚喜 | Oasis Mind「註冊送 20 心靈點數」 | 即時正反饋 |

#### 🛡️ 信任建立
| 機制 | 案例 | 心理原理 |
|------|------|---------|
| 隱私優先 | Posture AI「100% 地端 AI·影像不留存」 | 安全感=付費意願 |
| 本地 AI 標籤 | 「⬡ Medcore Local AI Core」 | 技術信任 |

---

### 📈 收入預測速算

```
月收入 = 總用戶 × 轉換率 × ARPU × (1 - 平台抽成)

轉換率基準:
- 工具型 App: 2-3%（Posture AI / Micro-Log）
- 內容/社交型: 3-5%（Oasis Mind / VIM）
- 平台型: 1-2%（Medic Agent）

ARPU 基準:
- 低價訂閱: HK$8-15（平台抽成 15%）
- 中價會員: HK$58（平台抽成 15-30%）
- 分級 VIP: 加權平均 HK$80-120

盈虧平衡點:
- Posture AI / Micro-Log: ~387 會員/月
- VIM: 387 會員首月即盈利（成本僅 API+雲端+法律+支付）
- Oasis Mind: ~500 會員（含 DeepSeek API 成本）
```

### 交付物
- [ ] 定價模式選定（6 選 1，或組合）
- [ ] 3 個用戶粘性機制設計
- [ ] 收入預測速算（轉換率 × ARPU）
- [ ] 付費牆位置設計（哪個功能觸發付費？）
- [ ] 免費用戶→付費用戶轉化路徑

✅ **完成條件:** 商業模式清晰 → Phase 1

---

## Phase 1: 策略 → 「為誰做？解決什麼？不做什麼？」

**載入 Skills:** `thinking-first-principles` `thinking-jobs-to-be-done` `steve-jobs-perspective` `thinking-inversion`

**交付物:**
- [ ] JTBD 用戶工作地圖（5 個核心 Jobs）
- [ ] MVP 功能清單（最多 8 個屏幕/頁面）
- [ ] 不做清單
- [ ] 競品差異化矩陣

✅ **完成條件:** MVP 範圍鎖定 → Phase 2

---

## Phase 2: 設計 → Design System + 組件庫

**載入 Skills:** `design-system` `design-taste-frontend` `brandkit` `minimalist-ui` `high-end-visual-design` `loop-design-check`

**設計 Token 模板:**
```
品牌色: #XXXXXX | 背景: #FFFFFF | 卡片: #F5F7FA
字體: Inter | 字級: 大標24/標題18/正文15/輔文13/小字11
圓角: 卡片12px/按鈕8px | 間距: 屏幕16px/元素12px/區塊24px
```

**核心組件:** Card / Chip / Button / Input / Banner / Accordion / BottomNav / EmptyState

**交付物:**
- [ ] Design Token 文件
- [ ] 8 個核心組件
- [ ] 主頁原型

✅ **完成條件:** 組件庫 + 原型完成 → Phase 3

---

## Phase 3: 架構 → 技術棧 + 目錄結構

**載入 Skills:** `dart-flutter-patterns` / `react-patterns` / `swiftui-patterns`（選對應框架）

**架構決策模板:**
```yaml
框架: Flutter/React/Vue/SwiftUI
狀態管理: Provider/Riverpod/Redux/Zustand
路由: GoRouter/React Router
資料層: Service → Repository → Model
主題: 全局 ThemeData 統一管理
```

**交付物:**
- [ ] 技術棧選定
- [ ] 架構模式確定
- [ ] 目錄結構建立
- [ ] 資料模型定義

✅ **完成條件:** 架構搭建完成 → Phase 4

---

## Phase 4: 構建 → 逐功能 TDD 開發

**載入 Skills:** `orch-build-mvp` `tdd-workflow` `loop-design-check` + 框架 code review skill

**構建順序:** 🔴P0（必須）→ 🟡P1（核心）→ 🟢P2（錦上添花）

**每個功能的閉環:**
```
測試(TDD) → Model → Service → Provider → Screen → 設計審查 → 代碼審查 → ✅
```

**交付物:**
- [ ] P0-1: _______
- [ ] P0-2: _______
- [ ] P1-1: _______
- [ ] P1-2: _______
- [ ] P2-1: _______

✅ **完成條件:** P0+P1 完成 → Phase 5

---

## Phase 5: 打磨 → 視覺 QA + 效能

**載入 Skills:** `high-end-visual-design` `frontend-a11y` `thinking-pre-mortem`

**檢查清單:**
- [ ] 視覺一致：間距/字級/顏色統一
- [ ] 無 overflow：所有文字正常顯示
- [ ] TextScaler 1.2x 測試
- [ ] 無障礙：對比度/標籤
- [ ] 空狀態/錯誤狀態/Loading 狀態齊全
- [ ] 首頁載入 < 1 秒
- [ ] 驚喜時刻動效流暢（如有）

✅ **完成條件:** 所有檢查通過 → Phase 6

---

## Phase 6: 上線 → 測試 + 安全 + 發布

**載入 Skills:** `security-review` `production-audit`

**檢查清單:**
- [ ] 單元/Widget/E2E 測試通過
- [ ] API 密鑰安全檢查
- [ ] 隱私政策 + 權限說明
- [ ] App Store 截圖 + 描述 + 關鍵詞
- [ ] 崩潰監控 + 用戶行為分析接入
- [ ] 付費系統測試（Sandbox 完整走通）

✅ **完成條件:** 正式上架

---

## 使用方法

| 指令 | 效果 |
|------|------|
| `/skill app-dev-workflow` | 顯示進度 + 下一步 |
| 「繼續開發」 | 載入當前 Phase Skills |
| 「審查設計」 | `loop-design-check` |
| 「下一階段」 | 標記完成，下一 Phase |
| 「進度」 | 完整進度總覽 |

## Jeremy 通用規則

- PPT 白底強制，暗色禁止
- UI 不加背景色，透明
- 折疊式佈局優先
- 返回鍵統一左上角
- 繼續=直接執行不總結
- 不追問 bug，自己查
- replace_all 禁用 >500 行

---

## 🗺️ 完整技能地圖（~65 個 App 開發技能）

> 載入 `app-dev-workflow` 時，根據當前 Phase 自動調用對應技能組。

### 🏗️ 框架核心

| 平台 | 技能 | Phase |
|------|------|:---:|
| Flutter/Dart | `dart-flutter-patterns` `flutter-dart-code-review` `flutter-overflow-prevention` | 3,4 |
| Swift/iOS | `swiftui-patterns` `swiftui-pro` `swiftui-debugging` `swift-concurrency-6-2` `swift-actor-persistence` `ios-icon-gen` | 3,4,5 |
| React Native | `react-native-patterns` | 3,4 |
| Kotlin | `compose-multiplatform-patterns` `android-clean-architecture` | 3,4 |

### 🎨 設計系統

| 類別 | 技能 | Phase |
|------|------|:---:|
| Design System | `design-system` `theme-factory` `ui-ux-pro-max` `design` `ui-styling` | 2 |
| Brand | `brandkit` `brand-guidelines` `brand-voice` `brand-voice-consistency` `brand-discovery` `brand` | 2 |
| Design Taste | `design-taste-frontend` `design-taste-frontend-v1` `high-end-visual-design` `loop-design-check` | 2,5 |

### 🖌️ UI 風格 (MengTo 40+)

| 風格 | 技能 |
|------|------|
| 極簡 | `minimalist-ui` `clean-minimal-beige-light-mode` |
| 玻璃 | `glass-dark-ui` `glass-dark-mode-clock` `dark-glass-clean-layout` `liquid-glass-design` |
| 工業 | `industrial-brutalist-ui` `technical-wireframe-info-layout` |
| 3D/WebGL | `threejs` `cobejs` `webgl-3d-object` `globe-gl` `globe-particles` `background-grid-webgl` `webgl-laser` |
| 動效 | `animation-systems` `animation-on-scroll` `gsap` `gsap-scrolltrigger-storytelling` `cinematic-gsap-lenis-motion-system` `cinematic-scroll-storytelling` |
| 特效 | `skeuomorphic-ui` `progressive-blur` `masked-reveal` `staggered-word-reveal` `marquee-loop` `dither-background` |
| 佈局 | `landing-page` `pricing-page` `agency-grid-layout-minimal` `split-layout-technical` `framed-grid-layout` `nested-container-frames` |
| 元件 | `matterjs` `vantajs` `tailwindcss` `beautiful-shadows` `company-logos` `css-border-gradient` |

### ✨ 動畫/3D 系統

| 類別 | 技能 | Phase |
|------|------|:---:|
| 基礎動畫 | `motion-foundations` `motion-advanced` `motion-patterns` `motion-ui` | 4,5 |
| 影片 | `remotion` `remotion-video-creation` | 5,6 |
| 3D/WebGL | `threejs` `cobejs` `webgl-3d-object` `webgl-laser` `globe-particles` | 4 |
| 特效 | `progressive-blur` `masked-reveal` `solar-duotone-bold` `corner-diagonals` `corner-lasers` | 5 |

### 🔍 QA/測試

| 類別 | 技能 | Phase |
|------|------|:---:|
| TDD | `tdd` `tdd-workflow` `test-driven-development` | 4 |
| Code Review | `flutter-dart-code-review` `code-review` `code-review-specialist` `requesting-code-review` `receiving-code-review` | 4 |
| 設計審查 | `loop-design-check` | 2,4,5 |
| 調試 | `systematic-debugging` `diagnosing-bugs` `qa` | 4,5 |
| E2E | `e2e-testing` `browser-qa` `webapp-testing` | 6 |
| 安全 | `security-review` `security-scan` `safety-guard` `gateguard` | 6 |

### 🚀 構建/發布

| 類別 | 技能 | Phase |
|------|------|:---:|
| MVP 構建 | `orch-build-mvp` `prototype` | 4 |
| 項目管理 | `plan-orchestrate` `writing-plans` `executing-plans` | 1,4 |
| 部署 | `deployment-patterns` `netlify-deploy` | 6 |
| CI/CD | `git-workflow` `using-git-worktrees` `finishing-a-development-branch` | 4,6 |
| 監控 | `production-audit` `automation-audit-ops` | 6 |

### 🔧 後端/API

| 類別 | 技能 | Phase |
|------|------|:---:|
| API | `api-design` `api-connector-builder` `mcp-builder` | 3 |
| FastAPI | `fastapi-patterns` | 3 |
| Django | `django-patterns` `django-tdd` `django-security` `django-verification` | 3 |
| 資料庫 | `postgres-patterns` `mysql-patterns` `redis-patterns` | 3 |
| 通用 | `backend-patterns` `docker-patterns` `codebase-design` `to-tickets` `request-refactor-plan` | 3,4 |

### 🧠 思維/策略

| 類別 | 技能 | Phase |
|------|------|:---:|
| 策略 | `thinking-first-principles` `thinking-jobs-to-be-done` `thinking-inversion` `thinking-second-order` `thinking-pre-mortem` | 0,1 |
| 產品 | `steve-jobs-perspective` `elon-musk-perspective` `naval-perspective` | 0,1 |
| 創意 | `brainstorming` `what-if-oracle` `hypothesis-generation` `grok-imagine` | 1 |
| 研究 | `deep-research` `research-synthesis` `academic-paper` `summarize-document` | 0,1 |
| 需求 | `to-spec` `meeting-notes-to-actions` `domain-modeling` `ubiquitous-language` | 1,3 |

### 🎬 媒體/內容

| 類別 | 技能 | Phase |
|------|------|:---:|
| 圖片 | `screenshot` `image-to-code` `unsplash-asset-images` `aura-asset-images` `gimi-illustration` | 5 |
| 影片 | `video-to-superprompt` `manim-video` | 5 |
| 圖表 | `architecture-diagram` `excalidraw` `drawio-generator` `cli-anything-drawio` `cli-anything-mermaid` | 2,4 |
| 文案 | `copywriting` `humanizer` `copy-editing` `content-strategy` `article-writing` `writing-shape` `writing-beats` | 2,4 |
| PPT | `officecli-pptx` `officecli-pitch-deck` `dashiai-ppt` `frontend-slides` | 2,5 |

### 🏥 垂直領域（可選）

| 領域 | 技能 |
|------|------|
| 醫療 | `healthcare-emr-patterns` `healthcare-cdss-patterns` `hipaa-compliance` `clinical-decision-support` `treatment-plans` `clinical-reports` |
| 金融 | `officecli-financial-model` `financial-calculator` |
| 學術 | `academic-pipeline` `academic-paper-reviewer` `scientific-writing` |
| 法律 | `legal-risk-assessment` `legal-document-summarization` 等 38 個法律技能 |

| 模式 | 定價 | 試用 | 來源 |
|------|------|------|------|
| 低價訂閱 | HK$10/月 | 3次免費 | Posture AI / Micro-Log |
| 分級 VIP | HK$58-388 | 永久免費基礎版 | Medic Agent |
| 數字保險庫 | 付費解鎖 | 有限儲存 | Micro-Log |
| 遊戲化 streak | 免費功能 | N/A | Posture AI |

| 粘性機制 | 心理原理 | 來源 |
|----------|---------|------|
| 百日火苗 | 連續不中斷的承諾 | Posture AI |
| 脊椎年齡 | 個人化進步指標 | Posture AI |
| AI 煉金術 | 等待=期待的魔法時刻 | Micro-Log |
| 保險庫鎖定 | 數據越多越離不開 | Micro-Log |
| 門診報告 | 看得見的產出價值 | Micro-Log |
| 本地 AI 標籤 | 隱私=信任 | Posture AI / Micro-Log |
