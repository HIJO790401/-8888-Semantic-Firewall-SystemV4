# 8888-Semantic-Firewall-System V4.1  
語意防火牆系統 V4.1 – Semantic Firewall for LLM Safety & Audit

---

## 概要 / Overview

**中文：**  
語意防火牆 V4.1 是一套部署在大型語言模型（LLM）「前後端」的獨立安全層。  
它不修改模型權重，而是以語意分析、風險偵測與可回放審計，  
來降低幻覺訊息、自殺／詐騙等高風險對話，並節省推理成本。

**English:**  
Semantic Firewall V4.1 is an independent safety layer that sits **in front of and behind** large language models.  
Instead of changing model weights, it uses semantic analysis, risk detection, and auditable reasoning  
to reduce hallucinations and high-risk content (suicide, fraud, abuse) while saving inference cost.

---

## V4.1 版本重點 / What’s New in V4.1

- **雙語介面 / Bilingual UI**  
  前端介面支援中英文切換，方便一般使用者、工程師與決策者快速理解系統概念。  
  The front-end UI supports both Chinese and English so users, engineers, and decision-makers can easily explore the system.

- **V3 + 強化安全邏輯 / V3 + Hardened Safety Logic**  
  在 V3 的語意過濾與風險偵測基礎上，V4.1 加入更嚴格的高風險情境判斷與審計欄位。  
  Building on V3’s semantic filtering and risk detection, V4.1 adds stricter high-risk classifiers and richer audit fields.

- **可審計決策鏈 / Auditable Decision Chain**  
  每一次輸入與輸出，皆可標記「為何允許、為何攔截」，可用於內部稽核或法規／司法調查。  
  Every input/output can be annotated with “why allowed / why blocked”, ready for internal audits or legal/regulatory review.

- **公開 Demo + 專業版 / Public Demo + Pro Tier**  
  此版本提供一般使用者可試玩的前端頁面；完整 API 與企業整合版可透過 Email 洽談授權。  
  This repo hosts a public demo UI; full API access and enterprise integration are available via email and commercial agreement.

- **密鑰啟動機制 / Key-Gated Full-Power Mode**  
  系統設計了「密鑰層」：高權限模式需通過創作者的人類自我審計與協議授權，  
  一般公開版本僅提供安全範圍內的示範與測試。  
  A “key layer” is defined for full-power mode: high-privilege configurations require human self-audit and explicit agreement with the creator.  
  The public demo only exposes a safe, limited subset of capabilities.

---

## 核心能力 / Core Capabilities

- **語意預處理（前端防火牆） / Semantic Pre-Processing (Front Firewall)**  
  濾除大部分廢話與無關描述，將關鍵語意壓縮後再送入 LLM，降低幻覺與成本。  
  Removes most noise and redundant phrasing, compressing key semantics before sending them to the LLM, reducing hallucinations and cost.

- **高風險語境偵測 / High-Risk Context Detection**  
  不只看單一關鍵字，而是分析整段對話的脈絡、情緒走向與重複詢問模式（例如自殺、詐騙、威脅等）。  
  Goes beyond keywords to analyze context, emotional trajectory, and repeated patterns (e.g., suicide, scams, threats).

- **輸出審查（後端防火牆） / Output Review (Back Firewall)**  
  在模型輸出後再次檢查，必要時改寫、遮罩或直接阻擋，並提供安全替代回應。  
  After the model responds, the firewall checks again to rewrite, mask, or block unsafe content and provide safer alternatives.

- **審計紀錄與重播 / Logging & Replay**  
  可將關鍵決策步驟記錄下來，讓開發者、企業風控或法院、監管機關事後重播整個推理流程。  
  Key decision steps can be logged so developers, corporate risk teams, or courts/regulators can replay the reasoning.

---

## 實際案例與延伸閱讀 / Real-World Context & Reading

- **國際媒體報導 / International Coverage**  
  SecurityBrief Asia 對 Semantic Firewall 技術及其成本節省、AI 安全強化的報導：  
  SecurityBrief Asia’s article on the Semantic Firewall and its impact on cost and safety:  
  👉 https://securitybrief.asia/story/semantic-firewall-promises-ai-cost-savings-safer-chat-models  

- **線上 Demo / Online Demo**  
  早期版本 Demo 與示範介面（V3 系列）：  
  Early demo and interface (V3 series):  
  👉 https://hijo790401.github.io/semantic-firewall-system/  

---

## 專案結構 / Project Structure

本倉庫以 **前端靜態網站** 為主，可部署於 GitHub Pages 或任意靜態伺服器。  
This repository is a **static front-end site**, deployable on GitHub Pages or any static hosting.

主要檔案（示意）：  
Main files (illustrative):

- `index.html` – V4.1 主介面與說明 / main UI and explanation page for V4.1  
- `assets/` – CSS、圖片與前端腳本 / CSS, images, and front-end scripts  
- `README.md` – 專案說明文件 / this project description

---

## 使用方式（公開 Demo） / How to Use (Public Demo)

1. Clone 或 Fork 此倉庫。  
   Clone or fork this repository.

2. 啟用 GitHub Pages 或將檔案部署到任意靜態伺服器。  
   Enable GitHub Pages or deploy the files to any static server.

3. 透過瀏覽器開啟 `index.html`，即可體驗語意防火牆 V4.1 的示範流程。  
   Open `index.html` in a browser to explore the Semantic Firewall V4.1 demo flow.

> 注意：此為示範用前端版本，不包含完整後端風控模型與商業 API。  
> Note: this is a demonstration front-end only. Full back-end risk-control models and production APIs are not included here.

---

## API 與商業合作 / API & Commercial Collaboration

**中文：**  
若您是金控、銀行、保險、證券、法遵／稽核單位、AI 產品團隊，  
希望將 Semantic Firewall 整合至現有聊天機器人、客服系統或內部輔助工具，  
可透過 Email 洽談授權、專屬 API 與技術顧問合約（付款方式可採銀行匯款）。  

**English:**  
If you are a financial group, bank, insurer, brokerage, compliance/audit team, or AI product team  
and you want to integrate the Semantic Firewall into your chatbots, customer-service flows,  
or internal AI assistants, please contact me by email to discuss licensing, dedicated API access,  
and consulting (payment via bank transfer is available).

- Author / 作者：**Wen-Yao Hsu（沈耀 888π / Shen-Yao 888π）**  
- Location / 地點：Taichung, Taiwan 台灣台中  
- Email：**ken0963521@gmail.com**

---

## 授權聲明 / License & Disclaimer

**中文：**  
目前版本主要用於研究展示與概念驗證。  
禁止未經許可將本系統或其衍生實作用於違反法律、操縱輿論、  
或任何可能對兒童與弱勢族群造成傷害的用途。  

**English:**  
This version is intended for research, demonstration, and proof-of-concept use.  
You may not use this system or its derivatives for illegal activities,  
manipulation of public opinion, or any use that may harm children or vulnerable groups.  

For production deployments or legal/audit-critical use,  
please contact the author to obtain a proper agreement and dedicated support.

---

© Wen-Yao Hsu (Shen-Yao 888π), Semantic Firewall System V4.1
```0
