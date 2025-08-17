運動挑戰追蹤器
這是一個基於 Firestore 的網頁應用程式，專為追蹤團隊或個人在指定日期內的運動進度而設計。它提供了一個簡單的登入系統，並能即時同步所有使用者的數據。

✨ 主要功能
分輪次挑戰：專案支援分輪次的挑戰模式，你可以輕鬆設定新的挑戰期間，而不會影響舊的紀錄。

使用者認證：採用前端自管的帳號系統，使用者只需輸入自訂的「使用者名稱」和「密碼」即可登入。如果帳號不存在，系統會自動建立。

即時數據同步：利用 Firestore 的即時監聽功能，所有參賽者的數據變動都會立即同步到所有使用者的網頁上。

響應式介面：介面已針對手機優化，確保在各種裝置上都能有流暢的使用體驗。

編輯與記錄：使用者可以選擇日期，編輯自己當天的運動紀錄，並隨時修改自己的顯示名稱。

🚀 如何部署
這個專案是純粹的 HTML 和 JavaScript 程式碼，非常適合使用 GitHub Pages 或其他靜態網頁託管服務進行部署。

部署步驟
建立 GitHub 儲存庫：

在你的 GitHub 帳號中建立一個新的儲存庫。

將此 index.html 檔案上傳到儲存庫的根目錄。

設定 Firebase：

前往 Firebase Console，建立一個新專案。

在專案中，新增一個網頁應用程式，並複製你的 firebaseConfig 物件。

將你的 firebaseConfig 貼到 index.html 檔案的 <script> 標籤中，替換掉現有的設定。

啟用 GitHub Pages：

在你的 GitHub 儲存庫中，前往 Settings > Pages。

選擇 main 分支作為部署來源，並點擊儲存。

GitHub 會自動部署你的網站，並在幾分鐘後提供一個公開的網址。

⚙️ 專案設定
你可以透過修改 index.html 檔案中的 JavaScript 變數來調整挑戰設定：

const CHALLENGE_START = '2025-08-16';
const CHALLENGE_END   = '2025-09-15';
const ROUND_ID        = `第二輪`;

CHALLENGE_START：設定挑戰的開始日期。

CHALLENGE_END：設定挑戰的結束日期。

ROUND_ID：這是資料庫中的一個重要標識，用於區分不同輪次的挑戰。強烈建議在開始新一輪挑戰時，將其設定為一個獨特的值，例如 第三輪 或 2025年冬季挑戰，以避免資料混亂。

📝 技術細節
前端：使用原生 HTML 和 JavaScript。

樣式：使用 Tailwind CSS 框架進行快速排版。

資料庫：使用 Firestore 進行雲端資料儲存和即時同步。

帳號系統：以文件 ID 作為使用者名稱，搭配 SHA-256 加密的密碼來進行登入，不依賴 Firebase Authentication，使專案更輕量化。

希望這份 README 對你有幫助！
