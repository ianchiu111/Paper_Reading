## 30 個論文期刊選項
這份名單來自「管理二學門國際學術期刊之品質分析」排名：
1. MIS Quarterly
2. Information Systems Research
3. Journal of Management Information Systems
4. Journal of the Association for Information Systems
5. Information Systems Journal
6. Journal of Strategic Information Systems
7. European Journal of Information Systems
8. Journal of Information Technology
9. Information & Management
10. Decision Support Systems
11. Decision Sciences
12. Information and Organization
13. International Journal of Electronic Commerce
14. International Journal of Information Management
15. Human-Computer Interaction
16. Information Systems Frontiers
17. International Journal of Human-Computer Studies
18. Internet Research
19. Data Base for Advances in Information Systems
20. Information Technology and People
21. Electronic Markets
22. Communications of the Association for Information Systems
23. Information Society
24. Electronic Commerce Research and Applications
25. Journal of Global Information Management
26. Electronic Commerce Research
27. Journal of Organizational Computing and Electronic Commerce
28. Information Technology and Management
29. Information Systems Management
30. Information Systems and e-Business Management

## Paper_Reading
- 快速翻譯論文內容
  - 選用模型：`gpt o4-mini-high`
  - Prompt + 論文附件：
    ``` Plaintext
    Step 1: Please use the OCR function to identify all the English contents without any modifications and summarizations (Please only focus on paper contents to avoid uncompleted print out) from title "-----" until title "-----" and print them in English in this journal.
    (------ 人工確認是否完整辨識所有的論文內容、缺漏內容)
    Step 2: Please translate all the english contents into traditional chinese without any modification and summarize.
    ```
  - 測試結果：翻譯內容完整，且遇到表格也會一併產出
  - Prompt Engineering 想法來源：實作 Multiagent 需要了解**不同任務會需要不同的能力與思考方向**，因此在這邊將問題拆成**使用OCR對PDF進行掃描**再進行**需要具備較佳的語言能力的翻譯任務**
    
- 筆記整理起手式
```Plaintext
## 論文基本資料整理
- 論文名稱：`---`
- 論文主題：`---`
- 作者名稱：`---`
- 期刊名稱：`---, (---) Vol. ---, Issue ---.`
- 期刊連結：[---](---)
## 論文重點整理
## 論文心得
```
    
