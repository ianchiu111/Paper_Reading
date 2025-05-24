## 論文基本資料整理
- 論文名稱：`Security and privacy risks in drone-based last mile delivery`
- 論文主題：`無人機` `隱私與安全風險`
- 作者名稱：`Tu, Y. J. & Piramuthu, S.`
- 期刊名稱：`European Journal of Information Systems, (2024) Vol. 33, Issue 5.`
- 期刊連結：[https://www.tandfonline.com/doi/full/10.1080/0960085X.2023.2214744](https://www.tandfonline.com/doi/full/10.1080/0960085X.2023.2214744)

## 論文重點整理
1. Last Mile Delivery (LMD)
   - 定義：**Last mile delivery is the final transportation segment of an item before it reaches its customer** FROM 論文 p.3
   - 特性：**直接面向消費者**
   - 目前的送貨方式：
      - ground vehicle-based：因車輛不受距離限制，可設置在較遠的據點
         - ❓配送距離嚴重影響配送時間，顧客無法快速獲得包裹/產品
      - drone-based：無人機航程有限，倉庫需相對鄰近配送區。仍存在無法配送的可能性
      - hybrid：以地面車輛將物品運至接近配送區，再由無人機投遞
2. Last Mile Drone Delivery (LMDD)
   - 潛在問題：
      - 電池壽命與續航力、負重能力、航程距離與時間的限制
      - 連接至未知的網路，可能會暴露隱私資訊
      - 法律規範 - 限定區域使用權限、飛行高度限制
   - 實際應用：
      - 如論文所述，現已有多家企業家無人機應用於 Last Mile Drone Delivery (LMDD)，常見商業無人機：可飛行約30分鐘，速度約18米／秒（use，2022） 
      - 案例分享：
  
| 新聞日期            | 企業                          | 重點                                             |
| ----------------- | ---------------------------- | ---------------------------------------------- |
| 2022 年 3 月 30 日 | FedEx & Elroy Air           | FedEx Express與Elroy Air合作，使用自動無人機執行配送          |
| 2022 年 4 月 24 日 | Walgreens & Wing            | Walgreens與Alphabet子公司Wing合作，在首座美國大城市推出無人機配送服務  |
| 2022 年 5 月 5 日  | Skyway & Zing               | Skyway與Zing在佛羅里達進行首航；UPS與CVS也提供無人機醫藥配送服務       |
| 2022 年 5 月 24 日 | Walmart                     | Walmart擴展DroneUp網絡，覆蓋六州400萬戶，年運送量逾百萬件          |
| 2022 年 6 月 16 日 | Amazon                      | Amazon Prime Air在加州Lockeford提供免費無人機配送，目標30分鐘送達 |
| 2022 年 6 月 17 日 | Papa John’s & Drone Express | Papa John’s與Drone Express在亞特蘭大試驗“無人機披薩”服務      |
| 2022 年 6 月 23 日 | Domino’s & SkyDrop          | Domino’s與SkyDrop簽署紐西蘭第二階段商業無人機配送協議             |

3. 統整 LMDD 風險、攻擊物件、顧慮維度的關聯
   - 由「程式碼、物件、信號」三大風險類型，決定可能的攻擊方式或攻擊渠道
   - 每種風險類型會對應到「受威脅物件／攻擊面」(遭攻擊的目標)
   - 攻擊發生時，會觸發的顧慮 (一種或兩種)
      - 無法遵守法律或監管要求 ➡️ 合規性顧慮
         - 無人機失控墜毀
         - 客戶資料外洩
      - 無法為客戶提供可接受或令人滿意的配送服務水準 ➡️ 服務顧慮
         - 配送延遲、中斷
   - 細看風險（看之後是否需要補充論文中提及的解決方式）：
    
| 風險類型（例子）                              | 受威脅實體   | 合規性顧慮（墜毀或資料外洩） | 服務顧慮（延遲或中斷） |
| ------------------------------------- | ------- | -------------- | ----------- |
| **程式碼風險**<br/>(例如資料外洩、偽指令、錯誤設定、惡意程式)  | 微控制器系統  | 可能             | 未知          |
|                                       | 韌體與作業軟體 | 可能             | 未知          |
|                                       | 資料儲存    | 可能             | 可能          |
|                                       | 標識資料    | 可能             | 可能          |
| **物件風險**<br/>(例如捕獲、破壞、偽造、劫持、逆向工程)     | 操作員     | 可能             | 未知          |
|                                       | 運輸包裹    | 未知             | 可能          |
|                                       | 硬體      | 可能             | 未知          |
|                                       | 標識實體    | 可能             | 可能          |
| **信號風險**<br/>(例如訊號干擾、中繼、GPS 重放、監聽、欺騙) | 感測器     | 可能             | 可能          |
|                                       | GPS     | 可能             | 可能          |
|                                       | 攝影機     | 可能             | 可能          |
|                                       | 地面控制站通訊 | 可能             | 可能          |
|                                       | 標識傳輸    | 可能             | 可能          |




## 論文心得
1. 此論文的範疇是以供應鏈，我認為可以限縮到電子商務(E-commerce)，因為電子商務存在低營運成本、快速、便捷的特性，與 Last Mile Drone Delivery (LMDD) 有較高的關聯，我相信透過無人機進行配送甚至可以減輕倉儲的管理成本與壓力
   - 電商與 Last Mile Drone Delivery (LMDD) 的相關處：
      - 低營運成本：無人機取代人力配送
      - 快速、便捷：不容易受到地形的限制
      - 改變電商的貨物管理方式：從被動管理(等待消費者領取包裹)改為主動管理(透過無人機主動配送至目的地)
      - 主動管理貨物可進一步改善倉儲管理的壓力，減少倉儲成本
   - 實驗證實：模擬蝦皮進行配送包裹的任務，解決店內包裹雜亂的現象
      - 包裹配送限制：包裹重量、目的地之距離與高度、配送路線、時間與成本
      - 此處以蝦皮或便利商店為例，因為據點多，可透過大量的無人機據點解決配送距離不足的問題
      - 此處不考慮耐摔、易碎性質與否，因為**安全配送**為主要目的
2. 論文中提供了國外多處已使用 Lat Mile Drone Delivery 的案例，但台灣卻尚未執行
   - 台灣人口分布較國外密集 ➡️ 電商據點較集中，可作為無人機送貨的據點
   - 法規問題尚未完善❓ 該如何幫助台灣推動無人機送貨服務
3. 論文聚焦主題的方式：UAV ➡️ LMDD ➡️ 脆弱性、威脅、攻擊、損害、延遲、中斷與風險
   - 可從本論文了解如何改善 UAV 執行任務的穩定性
   - 可將論文中 UAV 的特性與 AI Risk 做關聯
   - 關於**物件風險**，文獻沒有特別討論，但多個案例有呈現該問題 ➡️ 文獻空白❓
4. ✴️ 基於本片論文所延伸的風險
   - 本篇論文似乎尚未討論到，LMDD 普及後可能會衍生 **Multiple UAV System 的空中交通疑慮**，該疑慮隸屬於**M-UAV 空中交通風險**類型 (並未包含在程式碼、物件、訊號風險中) ➡️ **受威脅的實體將不再受限於單一 Single UAV System，而是 Multiple UAV System (受威脅的物件將擴大至 M-UAV 系統)** ➡️ 大幅增加合規性顧慮及服務顧慮
5. ✴️ 論文撰寫時針對**學術領域**，未對相關產業進行深入探討 ➡️ 是否可先與 E-Commerce 或零售業合作，打造 UAV Delivery Service ➡️ 解決倉儲、包裹過剩的問題 
6. 現有的解決風險方式仍存在大量的漏洞與衍生的風險
   - 如：包裹的保護措施
      - For example, merely counting on the parachuting mechanism is probably not suitable in many situations to protect the drone payload, but this is the only option available based on published literature. Conventionally, an adversary may use any hand-held weapon, such as a slingshot, to damage the drone payload especially when it hovers somewhere near the ground. When reachable, an adversary may directly detach the package from the drone and then take it away.

### 對照 LMDD Risk 及 AI Risk 的關聯：

**✴️ 論文中的風險與 AI Risk 的關聯性高，先舉五個例子作證明**
**✴️ 論文中的風險有提供解決辦法，若後續有需要進行正反方辯論可再使用**
1. 程式碼風險 - `惡意軟體、病毒的攻擊` ♾️ **4.3 Fraud, scams, and targeted manipulation**
   - Many such attacks are through malware or software viruses/worms that are essentially computational codes that affect the drone information systems (Choudhary et al., 2019; Nguyen & Nguyen, 2021; Rugo et al., 2022).
2. 物件風險 - `包裹、硬體設備等` + 程式碼風險 - `資料儲存/外洩` ♾️ **2. Privacy & Security**
   - Risk from objects relates to potential intentional physical harm that could be inflicted on the drone and/or its payload. These objects are external entities that attempt to physically derail drone-based last mile delivery from successful completion with no security or privacy violations (Fouda, 2018; Guo et al., 2020; Kong, 2021; Multerer et al., 2017; Nassi, Bitton, et al., 2021)
   - Incorrect parameter settings could be inserted into the drone systems to disable normal operations or enable unnecessary and dangerous drone operations. Even When the drone information systems perform normally, stored data such as private customer information could be exposed.
3. 訊號風險 - `中繼攻擊（relay attack）、重放攻擊（replay attack）等皆為有意透過技術進行網路攻擊或濫用` ♾️ **4.2 Cyberattacks, weapon development or use, and mass harm**
   - Relay attack can be mounted on drones whereby communication between a drone and an entity that is authorised to communicate with this drone is relayed between the drone and the entity by adversaries that are physically positioned between the communicating parties.
4. 訊號風險 - `GPS 欺騙（spoofing）` ♾️ **3.1 False or misleading information**
   - a drone could be subject to GPS spoofing attacks. Spoofing in this context signifies that GPS messages between a drone and GPS satellites are falsified
5. 訊號風險 - `訊號干擾與欺騙` ♾️ **7.3 Lack of capability or robustness**
   - a drone jamming attack refers to repeat edly sending signals to a drone sensor at high frequency to overload the sensor so it becomes too busy to respond and also to perform any other task. It could also be the case for noise to be used to block communication with a drone.

**對照 M-UAV 空中交通風險 與 AI Risk 的關聯性**

`M-UAV 指的是 Multiple UAV System`
1. M-UAV 空中交通風險 - `航線規劃` ♾️ **7.3 Lack of capability or robustness**
   - 案例舉例：多機航線規劃與碰撞避免需求凸顯系統對複雜空域的監管能力不足問題
      - [Reference](ttps://www.sciencedirect.com/science/article/pii/S1674862X25000047?via%3Dihub)
   - 案例舉例：若演算法無法即時分析，易導致多機航線交叉與事故風險提升
      - [Reference](https://www.sciencedirect.com/science/article/pii/S1366554524004502?via%3Dihub)
2. M-UAV 空中交通風險 - `無人機武器化` ♾️ **4.2 Cyberattacks, weapon development or use, and mass harm**
   - 案例舉例：協同無人機編隊可被用於大規模攻擊，如阿美科煉油廠的無人機襲擊
      - [Reference](https://www.airsight.com/blog/saudi-arabia-drone-attack-on-critical-infrastructures-after-action-report)
3. M-UAV 空中交通風險 - `Multiple UAV System 監管失敗` ♾️ **6.5 Governance failure** 
   - 案例舉例：坦尚尼亞無人機交通管理（UTM）運營失敗造成監管缺失
      - [Reference](https://www.unmannedairspace.info/uncategorized/the-lessons-of-failure-drone-delivery-and-utm-operations-fail-to-impress-tanzanias-regulators/)  
4. M-UAV 空中交通風險 - `空中交通擁堵與噪音汙染` ♾️ **6.6 Environmental harm**
   - 案例舉例：商業無人機配送的頻繁短途飛行顯著增加城市空域擁堵與噪音污染
      - [Reference](https://www.mdpi.com/2571-8797/7/1/24)

   

