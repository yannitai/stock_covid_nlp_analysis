# Stock Market Analysis Using Deep Learning and NLP During the Covid-19 Pandemic

This project explores how COVID-19-related news sentiment and confirmed case data impacted stock performance in Taiwan. We used Natural Language Processing (NLP) and Deep Learning techniques to predict stock trends and evaluated model performance using real market data.

## 📌 Overview

- **Index**: Taiwan 50 Index (TWII) and six selected industrial subindices
- **Timeframe**: Jan 2020 – Jul 2022
- **Dataset**:
  - 60,000+ financial news articles from [cnyes.com](https://www.cnyes.com)
  - COVID-19 confirmed case data from [data.gov.tw](https://data.gov.tw/dataset/120451)
  - Historical stock price data from [TWSE](https://www.twse.com.tw)

## 🧠 Methods & Workflow

### Phase 1: Data Collection & Preprocessing
- Scraped financial news articles using a web crawler
- Tagged and segmented Chinese text using [CKIP Tagger](https://github.com/ckiplab/ckiptagger)
- Merged with COVID-19 case data and historical stock prices
- Labeled sentiment (positive, neutral, negative) using a sentiment lexicon

### Phase 2: Feature Engineering
- Sentiment features (mean score, ratios)
- Technical indicators:  
  - Moving Average (MA)  
  - Bias Ratio (BIAS)  
  - Momentum  
- Text-based features from financial news

### Phase 3: Modeling
- **ARIMA**: Time series forecasting
- **LSTM**: Deep learning with integrated sentiment + COVID-19 + technical indicators

### Phase 4: Evaluation
- Expanding rolling window evaluation
- Directional accuracy comparison between predicted and actual trends

## 🎯 Results

- **LSTM with sentiment features** achieved **30% higher prediction accuracy** compared to ARIMA.
- Significant correlation observed between TWII movements and COVID-19 case surges.
- The combined use of NLP and technical indicators led to more robust market forecasts.

## 🛠 Tech Stack

- **Python**
- **Pandas / Numpy**
- **scikit-learn**
- **TensorFlow / Keras**
- **ARIMA (statsmodels)**
- **CKIP Tagger**
- **Matplotlib / Seaborn**

## 🔍 Key Takeaways

> Leveraging sentiment from financial news and pandemic-related data improves stock market forecasting, particularly in times of crisis.

## 📚 References

1. [TWSE Index Data](https://www.twse.com.tw/zh/page/products/indices/series.html)  
2. [Taiwan COVID-19 Open Data](https://data.gov.tw/dataset/120451)  
3. [CKIP Tagger](https://github.com/ckiplab/ckiptagger)  
4. [Cnyes Financial News](https://www.cnyes.com)

---

> ✨ Created by Yan-Ni Tai  
> M.S. in Applied Statistics, National Cheng Kung University  
> Contact: yannitai@umich.edu
