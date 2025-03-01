# 🚀 AdEase: Optimizing Ad Placements with Page View Forecasting  

## 📌 Problem Statement  
AdEase aims to **optimize ad placements** on Wikipedia by accurately **forecasting page views**. Since different Wikipedia pages attract varying levels of attention based on **language, access type, and origin**, predicting future traffic helps **maximize ad impact** and **improve data-driven ad targeting**.  

## 📊 Model Performance & Data Processing  

### ✔ Handling Missing Data  
- Removed rows with **>30% missing values**.  
- Retained only pages with **≤3 consecutive missing days**.  
- Applied **linear interpolation, forward & backward filling** during training/testing.  
- Used **IQR-based clipping** to remove outliers.  

### ✔ Forecasting with SARIMA  
- **Grid search** was used to **tune SARIMA models** for different languages.  
- **Performance Metrics (MAPE):**  

  | Language  | MAPE  |
  |-----------|-------|
  | 🇩🇪 **German**  | **1.8%**  |
  | 🇬🇧 **English**  | **2.1%**  |
  | 🇫🇷 **French**  | **2.5%**  |
  | 🇯🇵 **Japanese**  | **2.3%**  |
  | 🇪🇸 **Spanish**  | **9.9%** (Seasonality issues) |

  - **Spanish model** exhibits **unexplained seasonality**, with a **7th lag correlation** in the error correlogram.

## 🎯 Key Takeaways  
✅ **Accurate forecasting** enables **optimal ad placements** on Wikipedia.  
✅ SARIMA models performed **well across most languages**, except **Spanish**, which showed **seasonality challenges**.  
✅ **Future work**: Explore **alternative models** (e.g., **Prophet, LSTMs, or Hybrid models**) to **improve Spanish forecasts**.  

---

This README provides a **structured, engaging, and visually appealing** summary of your project! 🚀 Let me know if you need any tweaks! 😃
