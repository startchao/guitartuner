# 🎸 吉他調音器 Guitar Tuner（PWA）

免費、免安裝的網頁版吉他調音器。手機開瀏覽器就能用，可加到主畫面像 App 一樣開啟，**離線可用**。

**線上版**：https://startchao.github.io/guitartuner/

## 功能

- 麥克風即時音高偵測（自相關法 autocorrelation＋拋物線插值），顯示音名、頻率（Hz）與偏差（cents）
- 指針表：偏低（藍）／偏高（紅）／±5 cents 內調準（綠）
- 自動偵測最接近的弦並亮框；點任一根弦可鎖定目標＋播放參考音（用耳朵對音）
- 調弦法：標準 EADGBE、Drop D、半音降低 Eb、Open G、DADGAD、貝斯四弦
- 基準音 A4 可調 430–450 Hz
- 隱私：所有運算都在裝置本機（Web Audio API），不錄音、不上傳、無伺服器、無帳號

## 使用

1. 安靜環境，手機靠近音孔（電吉他靠近音箱）。
2. 按「開始調音」，允許麥克風權限。
3. 一次撥一根弦，讓聲音自然衰減；偏低把弦鈕往緊轉、偏高放鬆，進綠區就是準了。

> iPhone 需用 Safari 開啟（HTTPS），麥克風權限只會在本頁使用。

## 技術

- 純 HTML/CSS/JavaScript，零依賴、零建置，GitHub Pages 靜態托管
- 音高偵測：時域自相關＋拋物線插值（作法參考 cwilso/PitchDetect 的 ACF 思路，MIT；本專案程式碼自行實作）
- PWA：manifest + service worker（cache-first 離線）

## 授權

MIT
