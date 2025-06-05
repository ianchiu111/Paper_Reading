### 無人機目前的特色
1. 操控方式：pre-programmed operation OR human remote control(game console controllers、control app running on a smartphone or computer tablet)
2. 供電方式：batteries OR engine‑driven propulsion(論文中以**on a forced basis**表示)
3. 論文應用：
  - 無人機送貨服務 FROM reference 1
    - 技術層面：
      - GPS Module in UAV ➡️ 利用 GPS 定位使用者的位置
      - OTP ➡️ 一次性密碼避免詐欺
    - 理論層面：
      - 探討 **個人創新性、使用者預期結果、使用者的預期情緒與態度、產品的感知風險** 對無人機送貨服務的影響
      - 測量量表可參閱 **Reference 1 - 3. Methodology - 3.1. Measurement**
4.   



### 選擇的無人機 - PX4／ArduPilot
[MAVSDK - 開發網站](https://mavsdk.mavlink.io/main/en/index.html)
1. 多無人機管理（UAV1, UAV2）
- PX4／ArduPilot 支援多架無人機協同控制，只要每架無人機使用不同的MAVLink系統ID，就能在同一套控制程式裡分配不同任務。
- 可用 Python + MAVSDK 控制多台無人機同時執行不同配送路線。

2. GPS導航、路徑規劃
- 內建強大導航與自動任務功能（如自動起降、定點飛行、航點任務等）。
- 可用 Python/MAVSDK 實作動態導航、根據配送/充電需求規劃路徑（就像圖中GPS箭頭所示）。
- 仿真器（Gazebo, AirSim）可模擬GPS與地圖環境，開發初期不用實體飛機即可驗證系統。

3. RFID感測整合
- PX4/ArduPilot 控制板本身可透過UART、I2C等介面連接RFID模組（需要搭配樹莓派等單板電腦）。
- 可用 Python 控制樹莓派/Jetson Nano 讀寫RFID，然後用 MAVLink 指令協同任務（例如：只有感應到正確RFID才丟包裹）。

4. 充電站與自動返航
- PX4/ArduPilot 支援低電量自動返航（RTL, Return-to-Launch）。
- 你也可以用 Python/MAVSDK 自訂觸發條件（例如：到特定充電站執行降落、充電）。
- 充電狀態可以與雲端/地面站即時同步。

5. 配送點多樣化（大樓、便利店、充電站）
- 可將各種任務點（社區大樓、7-11、充電站等）事先設定為航點或座標，Python 程式可依據即時任務自動選擇最佳路線。
- 方便擴展新站點，只需新增GPS座標與任務邏輯。

6. 與地面站/雲端連動
- PX4/ArduPilot 透過 MAVLink 協定，能與 Python 應用程式、Web API 或資料庫交換資料。
- 可以串接雲端（如AWS IoT, Google Cloud, MQTT等）或本地伺服器做即時任務派送、監控。

7. 結論：你的系統規劃，完全適合 PX4／ArduPilot 平台！
- 從硬體彈性、功能擴充到軟體開發，這兩個平台都能支援你圖中所有功能。
- 以 Python 撰寫各種自動化、導航、感測、通訊程式都有完整範例與支援。



---
Reference：

[1. The drone delivery services: An innovative application in an emerging economy](https://github.com/ianchiu111/Paper_Reading/blob/main/UAV/01%20-%20The%20drone%20delivery%20services%3A%20An%20innovative%20application%20in%20an%20emerging%20economy.md)
