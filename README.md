# Stock-Tracker
I first built a stock tracker in Google Sheets using 'GOOGLEFINANCE'. While checking it, I noticed some values were wrong or unreliable. For example, JPMorgan's market cap appeared as $23B in some pulls, when its actual market cap is roughly $900B, and the value changed between refreshes.

This was a personal learning project for me to practice Python, different libraries, Google Sheets, GOOGLEFINANCE, and basic stock market concepts such as market cap, volume, P/E ratio and share counts.

#What the code does
It uses yfinance to get current data for the stocks. It loops over 16 tickers and pulls data from Yahoo Finance. It collects all the data for one ticker in a single row. It also adds a calculated column, for example how far the previous close is from the 52-week low. It helps me compare data with the Google Sheet i did. Furthermore, thanks to my code, i can see which currency is being used by the company.

#Findings
I noticed that overall, the market cap of the Google Sheet matched the ones in the code. However, 


