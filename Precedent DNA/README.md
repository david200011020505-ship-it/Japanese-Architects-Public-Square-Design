### 使用說明
1. 名稱：Precedent DNA
2. 用途/目的：整理建築案例知識
3. 使用者：AI 知識庫的建構者
4. 使用範例 : 使用步驟請參考以下 workflow 說明。

### Workflow
1. 蒐集建築案例資料，資料包含文字、圖片(基本圖面、現場照片、diagrams)
2. 使用LLM（ChatGPT、Gemini）對文字及圖片進行預處理的前置工作：\
   創建一個MyGPT或Google Gem，指令欄輸入'KnowledgeMaker'的內容，方便批次大量進行案例資料的預處理。
3. 將資料餵給LLM的方式：\
   開啟先前創建的MyGPT或Google Gem，在對話欄上傳圖片(基本圖面、現場照片、diagrams)，並將案例文字資訊用以下格式輸入：\
_case_id: JP_001_\
_case_name_original: Ginza Sony Park_\
_case_type: public plaza / urban park_\
_location: Ginza, Tokyo, Japan_\
\
_input_materials:_\
_-photos_\
_-plans_\
_-sections_\
_-elevations_\
_-diagrams_\
_-web_text_\
\
_web_text:\
_以下為案例網頁介紹文字，請將其作為分析依據，萃取與 site、scale、users、event、function 有關的資訊，並轉換為標準 JSON。不要逐字摘要，也不要保留與空間分析無關的宣傳語句。_\
\
_[在這裡貼上網頁文字全文]_\
"

4. LLM會以包含在'KnowledgeMaker'中的格式說明為範例，將資料打包成json格式(output)，請確認內容及結構正確無誤。
