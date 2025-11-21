# Gamestop vs Tesla Stock Price

In early 2021 the finance world felt completely unhinged for a minute. On one side you had **GameStop (GME)** – a struggling brick‑and‑mortar game retailer that turned into a meme stock, fuelled by Reddit, short squeezes, and wild volatility. On the other side you had **Tesla (TSLA)** – already a cult stock on its own – with Elon Musk casually tweeting “Gamestonk!!” and pouring even more petrol on the fire.

This little project is me turning that chaos into something a bit more structured: pulling real price data for both companies, lining it up with basic fundamentals (revenue), and visualising how their stories play out on a chart.

---

## What this project does

At a high level:

- Pulls **historical stock prices** for Tesla and GameStop using the `yfinance` API.
- Scrapes **revenue data** from the web using `BeautifulSoup` (for a bit of real‑world data collection).
- Cleans and reshapes everything with **pandas**.
- Builds **visualisations** that:
  - Show each stock’s price over time.
  - Compare price vs revenue for a single company.
  - Put **Tesla and GameStop side‑by‑side** so you can see how differently the market treats a meme stock vs a high‑growth EV giant.

It’s not a trading model or a price predictor. It’s an end‑to‑end data story from **raw web data → cleaned tables → charts → interpretation**.

---

## Files in this folder

- [`Extracting and Visualizing Stock Data.ipynb`](Extracting%20and%20Visualizing%20Stock%20Data.ipynb)  
  Notebook that:
  - Uses `yfinance` to download historical stock prices.
  - Uses web scraping to fetch revenue data.
  - Cleans and merges the two sources.
  - Plots price and revenue trends for each company.

- [`Stock-Price-and-Profit-Analysis-main/src/Stock-Price-and-Profit-Analysis.ipynb`](Stock-Price-and-Profit-Analysis.ipynb)  
  Notebook that:
  - Focuses on **Tesla vs GameStop** as a direct comparison.
  - Recreates and refines stock‑price and revenue charts.
  - Uses the outputs to generate static images for sharing.

---

## Results  
  - [`Stock-Price-and-Profit-Analysis-main/result_tesla.png`](result_tesla.png)  
  - [`Stock-Price-and-Profit-Analysis-main/result_gamestop.png`](result_gamestop.png)

---

## Tech stack

- **Python**
- **pandas** for data wrangling
- **yfinance** for historical stock prices
- **requests + BeautifulSoup** for scraping revenue data
- **matplotlib / seaborn / plotly** for visualisation (depending on the notebook)

---

## Methodology

Even though the focus is “just” stock charts, it still walks through the full pipeline:

1. **Data extraction**  
   - Call an API (`yfinance`) instead of downloading a CSV manually.  
   - Scrape a public site for revenue data instead of relying on a pre‑cleaned dataset.

2. **Data cleaning and alignment**  
   - Parse dates, sort timelines, handle missing values.  
   - Align different data sources on a common time axis.

3. **Analysis and visualisation**  
   - Plot long‑term price trends.  
   - Plot price against revenue to see whether fundamentals and hype move together.

4. **Communication**  
   - Export clean images (`result_tesla.png`, `result_gamestop.png`) that can be dropped into a report, slide deck, or blog post.  

For a lot of finance people, this is exactly what they care about in a first pass:  
> “Can you get real market data, clean it, and show me something meaningful on a chart?”

That’s what this project is designed to show.

---
