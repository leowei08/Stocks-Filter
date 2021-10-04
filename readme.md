# Stocks Filter
A stock screener for the Taiwan Stock Exchange based on Technical Analysis

# Motivation
There are a lot of individual investors who invest as a side hobby and don't have the time to filter stocks one by one. This stock screener does that job for the users based on user-selected filters and saves so much time while giving technical picks. The filters currently include hourly, daily, weekly moving averages, daily volume, moving averge convergence divergence, the relative strength index, and institutional investors overbuy indicator (adding more).

# Files
[getStocks](getStocks.ipynb): Web-scrapes company info, daily stocks info, and institutional investors buying data from https://www.twse.com.tw/en/ and feed it to a local Postgres database.

[TWStocks](TWStocks.ipynb): Gets data from the local database, filters the stocks based on selected filters, and emails out the technical picks.

[gui](GUI.ipynb): A graphical user interface for the stock screener. Checkboxes and input thresholds to select filters and outputs a treeview for users to scroll through a list of results with stock number, company name, and company industry. Clicking on a stock will show its recent info in charts web-scraped at https://www.twse.com.tw/pdf/ch/[StockNumber]_ch.pdf. The info includes institutional investors overbuy indicator, margin trading, short selling, and recent trend.

[updateStocks](updateStocks.ipynb): An automated script ran daily (business days) to update stocks and institutional investors data to the local database.
