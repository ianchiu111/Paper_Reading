### 背景補充
Digital Content(數位內容)
- 比較：
  - 非同步平台 v.s. 同步平台
  - Reddit、維基百科 v.s. Twitch、YouTube Live
- 平台的互動性 ➡️ 使用者的規模增加
- Raid 功能：允許一位直播主在自己的直播結束時，將自己的觀眾群「轉移」或「引導」到另一位直播主的頻道中 ➡️ 具有不可預測與控制性

### 研究問題與發現
本研究探討了 Twitch 平台上**Raid 功能**帶來的外生性觀眾增加，並實證證明 群體規模對即時評論者參與度的影響。具體來說，研究發現：
1. **群體規模增加對現有評論者參與度的影響**：透過 Raid 功能引入的新觀眾，會導致現有的評論者參與度通常會降低。
2. **負向參與效應的中介機制**：群體規模的增大導致聊天室中的**主題不連貫性**和**評論情感極性**(comment polarity)上升，造成現有評論者的參與度的減少。
3. **版主的調節作用**：**機器人版主** 或 **人工版主**，能有效減輕群體規模增加帶來的負面影響：
   - **機器人版主** 在**大規模觀眾**進入時，能有效減少聊天室中 **主題不連貫性** 的升高，從而改善討論的流暢度。
   - **人工版主** 在**較小規模的觀眾**進入時，更能有效控制 **評論情感極性** 的激增，從而維持聊天室情緒的穩定性。
4. 該議題存在**擁擠效應**(congestion effect)：群體規模增加對同步內容平台評論者參與度的負外部性

### 內容整理：群體規模、主題不連貫性、評論極性與用戶參與之間的微妙關係
1. group size：群體規模
- 定義：平台觀眾的數量，當觀眾數量增加時會出現**正向效應**與**負向效應**兩種不同的效應
  - 正向效應：基於**網路效應**可知觀眾的數量提高整體的參與度與討論機會
  - 負向效應：基於**擁擠效應**可知，過多的觀眾會使討論變得快速且雜亂，這會造成信息過載
2. topic incoherence：主題不連貫性
- 定義：聊天室中各個評論之間的語義一致性，即觀眾是否在同一個話題上進行討論，當群體規模增大時，討論往往會變得更加分散，故而衍生**討論分散**與**影響參與度**兩種狀況
  - 討論分散：討論焦點變得無法集中
  - 影響參與度：主題不連貫性對讓觀眾覺得失去討論的興趣
3. comment polarity：評論極性
- 定義：觀眾在聊天室中的情感表達強度
  - 情感強度增加：當群體規模增大時，情感表達會變得更加極端
  - 負向影響：過於激烈或情緒化的評論會降低討論的質量
4. user engagement：用戶參與
- 定義：觀眾在直播過程中對聊天室的互動程度，與平台的廣告收入、訂閱數量以及觀眾留存率密切相關
- 用戶參與容易受到**群體規模**、**主題不連貫性**、**評論極性**的影響
- 論文使用的衡量指標
  - 評論者數量
  - 單一評論者的評論數量
  - 評論主題不連貫性
  - 評論情感極性

---
小結論：
- 群體規模的增加在一定程度上會引發主題不連貫性和評論極性的升高，這些因素進一步抑制了用戶參與
- 內容管理（如機器人版主與人工版主）的有效介入能夠緩解群體規模增大帶來的負面影響，特別是在控制 話題一致性 和 情感平衡 方面發揮關鍵作用。

### Bot and Human Moderators on Digital Platforms
1. 基本介紹
  - 機器人版主：基於演算法進行自動化任務 
  - 人工版主：基於自願協助管理頻道的用戶
2. 功效比較
  - 機器人版主：高效處理重複性任務，這創造了對線上社群有益的資訊氛圍，從而促進參與者之間的交流
  - 人工版主：保護用戶動機的重要性，並在干預和保護觀眾發言權之間找到平衡(Base on 56 interviewed volunteer moderators from reference)
3. 調節效果：
  - 機器人版主：有效抑制話題不連貫度的上升，尤其在大型 Raid 時最顯著
  - 人工版主：更善於調節情緒極性，對小型 Raid 的情緒波動控制效果最佳
---
小結論：
- 人工版主與機器人版主的協作可以更好地維護社群的互動，機器人版主複雜重複的自動化工作，而人工版主則是在聊天室提供社群管理與情感上的支持

### 資料集的蒐集與處理
1. 資料來源與平台選擇
- 研究選擇 **Twitch** 作為研究平台，因為 Twitch 是全球領先的即時直播平台，並且擁有大量的用戶互動數據，特別是用戶評論資料。
- 研究期間：資料收集時間範圍從 **2022年5月15日** 到 **2022年9月23日**。
2. 資料集的範圍與結構
- 直播類別：研究選取了 Twitch 上最受歡迎的 **10個直播類別**，這些類別的選擇是基於平台上觀看數量最多的分類，包括但不限於：
  - Just Chatting（即時聊天類別，非遊戲類別）
  - Minecraft、Valorant、Counter-Strike: Global Offensive、Call of Duty: Warzone、Fortnite、Warcraft 等遊戲類別。
- 資料內容：
  - 播放片段(Live Vedio)：資料集涵蓋 **7,074個直播播放片段**，每個片段包含所有觀眾的即時評論。
  - 評論數據(Chat Room)：研究蒐集了來自每個播放片段的評論，並追蹤了每條評論的詳細時間戳（即評論發佈的具體時間）。
- 總觀察數據：
  - 資料集包含 **141,665個觀察樣本**，即 **每一個時間點的聊天室數據**。
  - Raid事件：資料集涵蓋了 **129,119次Raid事件**，這些事件是引發群體規模增加的關鍵。
3.  資料收集過程
- Twitch API：研究利用 **Twitch API** 進行數據收集，獲取每位直播主的ID、觀眾數量、評論內容等數據。
- 聊天室評論：所有評論都記錄下來，包括每條評論的 **發佈時間、評論者名稱、評論內容**，並根據時間戳進行索引。
- 標註Raid事件：每次Raid的發生都會在系統中標註，並記錄引入的觀眾數量（Raid者數量）。
4. 數據匹配與處理：對照有無 Raid 事件的結果
- 播放片段對比：研究將**有Raid事件**的播放片段與相同頻道的**無Raid**播放片段進行對比，作為對照組。
- 時間窗口設置：使用 **10分鐘前後** 的時間窗口來對比Raid前後的觀眾參與度變化，這樣可以確保Raid事件對觀眾行為的影響在合理的時間範圍內被捕捉。
- 精確匹配：為了減少選擇偏誤，研究使用了 **精確匹配（Exact Matching）** 方法，匹配相同頻道和相同時間段的播放片段。
  - 避免時間對研究結果的影響 ➡️ 針對Raid事件發生在**同一天、同一時間段內**的無Raid播放片段進行匹配，以確保觀察樣本的可比性。
5. 資料蒐集與前處理
- 評論與參與度的測量：
  - 評論者數量：計算**每分鐘**內發表評論的**獨立用戶數量**。
  - 每位評論者的評論數：計算**每位評論者**在**特定時間內**的發言數量，這樣可以衡量評論者的活躍程度。
- 主題不連貫性與情感極性：
  - 使用 **GloVe詞嵌入（Word Embedding）** 技術來量化評論之間的語義距離，計算每個時間段的 **主題不連貫性**。
  - 使用 **RoBERTa情感分析模型** 來分析評論的情感強度（情感極性），並取其絕對值來衡量情感表達的強烈程度。
- 缺失值處理：對於**只有一條評論的情況或無評論**的情況，缺失的數值會被設為零，因為這樣的情況下無法計算主題不連貫性或情感極性。
- 傾向分數匹配（PSM）：在進行匹配過程中，為了控制影響參與度的其他變數（如視頻的受歡迎程度和發佈時間），使用了傾向分數匹配來進一步保證實驗組和對照組之間的可比性。
6. ✴️ 數據分析模型
- 差異中的差異（DID）模型：用來估計Raid事件對現有觀眾參與度的影響，這樣可以控制時間和其他不可觀察因素對參與度的影響。
- 回歸模型：通過引入 **固定效應（Fixed Effects）**，研究考慮了直播主的固有特徵（例如，直播主的經驗和頻道類型）以及時間效應（例如，不同的星期和時間段）。

### 對評論的語意分析及情感分析
1. 語意分析：利用**預訓練的 GloVe 模型** + **GloVe Twitter 向量** 衡量聊天室評論的主題不連貫性
  - 分析步驟：計算每個評論的評論向量➡️使用評論向量之間的平均歐氏距離來建模主題不連貫性➡️獲得評論主題的不連貫性分數
  - 主題不連貫性分數越大，表示聊天室的話題越分散，這會影響觀眾的參與意願
  - 補充：
    - 相關的 GloVe 公式如果在**標題 3.3 Topic Incoherence Measure**
    - 圖 2 展示了構建主題不連貫性分數的過程
    - 表 1 則提供了計算數據集中不連貫性分數的範例
2. 情感分析：
  - Twitch 評論輸入預訓練的 RoBERTa 模型，獲得一個情感分數，即情感極性，範圍從 -1（極度負向）到 1（極度正向）
  - 透過**絕對值處理**捕捉情感的強度（因為研究者這邊沒有要探討情感屬於正向還是負向）
  - 補充：
    - 表 2 為描述性統計數據

---
❓疑問：
- 情感的正向與負向對於本篇論文的研究真的不會有影響嗎
- 正向與負向的言論是否會影響觀眾的存留

### 論文實證分析與結果重點

1. 研究設計與辨識策略
- 利用 Twitch「Raid」功能的外生性流量衝擊，構建差異中之差異（DID）模型，衡量觀眾群增加對既有留言者之影響。
- 觀察時間窗為 Raid 前後各 10 分鐘，並以同一頻道、同一時間段的無 Raid 影片對照。
2. 主要效果（Main Effect）
- Raid 後，既有留言者數量平均減少約 8.1%，每人發言數平均減少約 5.6%。
- 樣本再分為「大型 Raid」與「小型 Raid」，大型 Raid 造成的負向影響更為顯著。
3. 中介機制（Mediation Analyses）
- 觀察到 Raid 使得聊天室話題不連貫度（topic incoherence）顯著上升（+0.133），且情緒極性（polarity）上升（+0.015）。
- 話題不連貫度每上升一個單位，留言者發言數減少約 6.7%、留言者數減少約 12.6%；而情緒極性每上升一個單位，則略微增加留言數。
- 因此，約 10.3%（發言數）及 8.4%（留言者數）的負向效果可歸因於上述兩項中介，其中話題不連貫度的影響遠大於情緒極性。
4. 結論與實務啟示
- 同步即時平台易因群體擴張而產生資訊擁擠與品質劣化，進而抑制既有用戶的互動動機。
- 設計上可結合人、機審核機制：利用機器人快速過濾離題發言、人類審核者維持情緒氛圍，以提升平台的可持續參與度。

