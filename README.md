# Web-Scraping-Project
This is a project to scrape data from the web and store the results in both a text file as well as the SQLite
database.

A) The WSJ’s US Stock Market Movers website (https://www.wsj.com/marketdata/stocks/us/movers) or (https://money.cnn.com/data/hotstocks/ ) tracks the most active stocks on a
real time basis. First wrote Python scripts that collect the list of Most Actives tickers only from one of the above websites. Next, took these ticker symbols and built a
comma separated text file (called stocks.txt) with data about each stock from the Google finance
website: . https://www.google.com/finance/quote/AMD:NASDAQ which gives the quote for ticker symbol
AMD as an example. The data was collected from the Google Finance site that did not include (Actual
text as seen in the website is in brackets):
OPEN price (Open)
VOLUME (Avg. Volume)
PE RATIO (PE Ratio (TTM))

B) Note that the stock average volume is an INTEGER type but the quantity obtained from the website
may have commas. Program removed these commas from the average volume quantity
and stored it as numbers.

C) In addition to the stocks.txt file, the data was stored in an SQLite database. The
StocksDatabase had a table called StocksTable that contains the following columns and
types:
Ticker Symb TEXT
OpenPrice REAL
Volume INTEGER
PERatio REAL
