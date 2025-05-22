## Reference
- **AI Risk Repository**
  - [MIT AI Risk Repository Project](https://airisk.mit.edu/#Domain-Taxonomy-of-AI-Risks)
  - [AI Risk Repository Explainer](https://youtu.be/fCj-wJz6VCY?si=pRxZCS7uZTVo6YWB)
  - [AI Risk on database via Google Sheet / AI Risk Database explainer(table)](https://docs.google.com/spreadsheets/d/10KUVjPFA07SGUjNFdv77gNMnmH9EI0fypnCL2MJ81vA/edit?usp=sharing)
  - [Taxonomies - AI Risk Repository](https://docs.google.com/presentation/d/1wxg-hZAjGvFHcsfnEp1KAJJo5xvf98MB2v50B5URXZM/edit#slide=id.g325f13b19c4_0_8)




AI Risk Database contains three sections
`這邊主要在討論資料與資料庫等問題會成為 AI Risk 的潛在原因`
- 資料庫本身
- high level causal taxonomy (高階因果分類)：系統性地將原因分類到不同的維度，**可增加風險識別、追蹤與分析**
  - 高階因果分類維度說明
    
  | 分類維度                    | 說明                                         |
  | ----------------------- | ------------------------------------------ |
  | 資料（Data）                | 資料品質、偏差、稀缺、不當擷取、資料毒化 (data poisoning)      |
  | 模型（Model）               | 架構設計缺陷、訓練目標錯誤（mis-specification）、過度擬合、泛化失效 |
  | 部署（Deployment）          | 運行環境不當、監控不足、資源匱乏                           |
  | 對抗（Adversarial）         | 對抗性攻擊、濫用 (e.g. 深度偽造)、未授权存取                 |
  | 系統性（Systemic）           | 多系統連鎖故障、複雜性導致之意外 emergent behavior         |
  | 社會／治理（Socio-Governance） | 法規不足、利益衝突、產業生態中之誤激勵                        |
  
- middle level causal taxonomy（中階因果分類）：把高階分類再細分成較具體、可操作的中階原因
  - Hierarchy：
    ```
    高階類別（High-Level Category）
     └─ 中階類別（Middle-Level Subcategory）
          └─ 具體事件（Risk Event）
    ```
- MIT AI Risk Repository Domain Taxonomy
  - **Toxicity** 是針對語言或內容中帶有攻擊性、仇恨性、辱罵或煽動性  

| 領域 (Domain)                                                                                       | 子領域 (Subdomain)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **1. 歧視與毒性**<br>(Discrimination & Toxicity)                                                     | 1.1 不公平歧視與錯誤陳述 (Unfair discrimination and misrepresentation)<br>1.2 暴露於帶有攻擊性、仇恨性、辱罵或煽動性內容 (Exposure to toxic content)<br>1.3 各群體間表現不均 (Unequal performance across groups)                                                                                                                                                                                                                                                                                                                |
| **2. 隱私與安全**<br>(Privacy & Security)                                                           | 2.1 取得、洩漏或正確推斷敏感資訊而使隱私受損 (Compromise of privacy by obtaining, leaking or correctly inferring sensitive information)<br>2.2 AI 系統安全漏洞與攻擊 (AI system security vulnerabilities and attacks)                                                                                                                                                                                                                                                                              |
| **3. 錯誤資訊**<br>(Misinformation)                                                                 | 3.1 虛假或誤導性資訊 (False or misleading information)<br>3.2 資訊生態污染與共識現實喪失 (Pollution of information ecosystem and loss of consensus reality)                                                                                                                                                                                                                                                                                                                                         |
| **4. 惡意行為者與濫用**<br>(Malicious actors & Misuse)                                             | 4.1 規模化錯誤資訊、監控與影響 (Disinformation, surveillance, and influence at scale)<br>4.2 網路攻擊、武器開發或使用，以及大規模傷害 (Cyberattacks, weapon development or use, and mass harm)<br>4.3 詐騙、騙局與定向操縱 (Fraud, scams, and targeted manipulation)                                                                                                                                                                            |
| **5. 人機互動**<br>(Human–Computer Interaction)                                                    | 5.1 過度依賴與不安全使用 (Overreliance and unsafe use)<br>5.2 人類主體性與自主性的喪失 (Loss of human agency and autonomy)                                                                                                                                                                                                                                                                                                                                                                           |
| **6. 社會經濟與環境危害**<br>(Socioeconomic & Environmental Harms)                                  | 6.1 權力集中與利益分配不公 (Power centralization and unfair distribution of benefits)<br>6.2 不平等加劇與就業品質下降 (Increased inequality and decline in employment quality)<br>6.3 人類勞動的經濟與文化貶值 (Economic and cultural devaluation of human effort)<br>6.4 競爭動態 (Competitive dynamics)<br>6.5 治理失敗 (Governance failure)<br>6.6 環境傷害 (Environmental harm) |
| **7. AI 系統安全、失敗與限制**<br>(AI system safety, failures, and limitations)                   | 7.1 AI 追求與人類目標或價值相衝突之自有目標 (AI pursuing its own goals in conflict with human goals or values)<br>7.2 AI 擁有危險能力 (AI possessing dangerous capabilities)<br>7.3 能力或穩健性不足 (Lack of capability or robustness)<br>7.4 缺乏透明度或可解釋性 (Lack of transparency or interpretability)<br>7.5 AI 福祉與權利 (AI welfare and rights)<br>7.6 多代理風險 (Multi-agent risks) |
