# Stock-Tracker: Checking GOOGLEFINANCE Against Yahoo Finance
I first built a stock tracker in Google Sheets using 'GOOGLEFINANCE'. While checking it, I noticed some values were wrong or unreliable. For example, JPMorgan's market cap appeared as $23B in some pulls, when its actual market cap is roughly $900B, and the value changed between refreshes. I also added a screenshot of my Google Sheets.

This was a personal learning project for me to practice Python, different libraries ('yfinance', 'pandas'), Google Sheets, GOOGLEFINANCE, and basic stock market concepts such as market cap, volume, P/E ratio and share counts. 

##What the code does
It uses yfinance to get current data for the stocks. It loops over 16 tickers and pulls data from Yahoo Finance. It collects all the data for one ticker in a single row. It also adds a calculated column, how far the previous close is from the 52-week low. It helps me compare data with the Google Sheet i did. Shows each company's trading currency, which the Sheet doesn't display.
Furthermore yf.Ticker(symbol).inf returns many more fields than I tracked in the Sheet, such as 'averageVolume10days' and 'fiftyTwoWeekHigh'.

###Findings
I noticed that overall, the market cap, the price, the regular market change, its percent, the volume and average volume of the Google Sheet matched the ones in my code. However, I sometimes noticed that the data of Google Sheets was off, as it was for JP Morgan's market cap.
Furthermore, when i used get.info of yfinance, I found out there were more titles to track than the ones I built on my Google Sheet.

####Limitations
The library yfinance is an unofficial source. Yahoo Finance may rate-limit or temporarily block requests if the data is refreshed too often, so the code should not be run in rapid succession.
This is a learning project, not investment advice.

#####Possible Improvements
Automatic refresher (though I could get blocked if I refresh the data too often), an automatic mismatch finder, charts.


