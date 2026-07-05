# DBE Auto Pilot — PixInsight Update Repository

PixInsight 的 AI 輔助全自動背景梯度校正工具（DynamicBackgroundExtraction）。

## 安裝

1. PixInsight → **Resources → Updates → Manage Repositories** → **Add**：

   ```
   https://conan0312.github.io/dbe-updates/
   ```

2. **Resources → Updates → Check for Updates** → 安裝 → 重新啟動 PixInsight
3. Script 選單出現 **DBEAutoPilot**；第一次執行時輸入你的
   [Anthropic API Key](https://console.anthropic.com/)（會記住）

## 使用摘要

- 選擇剛疊好的線性影像 → 設定 Bortle 等級與濾鏡 → 開始全自動流程
- 完成後產生 `<影像>_DBE_<時間戳>`（校正後）與 `<影像>_background_<時間戳>`（背景模型）兩個新視窗，原始影像不會被更動
- 詳細調整說明報告輸出到 `<家目錄>/DBEAutoPilot/`
- AI 只分析統計數據並建議取樣點與參數，影像像素僅經 PixInsight DBE
  古典演算法（2D surface spline）處理，無任何生成式處理
- AI 分析約需 30~90 秒，期間介面凍結屬正常現象；API 呼叫依 Anthropic 費率計費
