# Basic tool for (gently) scraping public ETF data (across exchanges) from the UK [Morningstar](http://tools.morningstar.co.uk/uk/etfquickrank/default.aspx?Site=UK&Universe=ETALL%24%24ALL&LanguageId=en-GB) ETF Quickrank / Database .

Please note:

- scraping this website is only allowed for personal use (as per Morningstar's Terms and Conditions).
- this tool is structured in a such a way that it gently / ethically scrapes the pages it encounters (in other words, scraping data might take a bit longer given the couple of "sleep" intervals embedded in the code)
- you will have to point the browser variable to the local path of your webdriver
- though this scraper has specifically been built for the UK Morningstar website, it enables one to extract data from multiple non-UK universes (e.g. ETFs listed on the Xetra, Nasdaq etc)

This tool has been written by means of [Python 3.5.1](https://www.python.org/downloads/release/python-351/), [Selenium 3.4.3](https://pypi.python.org/pypi/selenium) and [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/).

Example of the resulting dataframe one might expect:

```
    TER                       category   close  \
0  0.15  Europe Large-Cap Blend Equity  260.39
1  0.15      US Large-Cap Blend Equity   39.34
2     -   Sector Equity Infrastructure       -
3     -     Property - Indirect Global   62.74
4     -                    Global Bond   55.92

                                                link  \
0  http://www.morningstar.co.uk/uk/etf/snapshot/s...
1  http://www.morningstar.co.uk/uk/etf/snapshot/s...
2  http://www.morningstar.co.uk/uk/etf/snapshot/s...
3  http://www.morningstar.co.uk/uk/etf/snapshot/s...
4  http://www.morningstar.co.uk/uk/etf/snapshot/s...

                                                name  \
0             Amundi ETF MSCI Europe UCITS ETF C USD
1               Amundi ETF S&P 500 UCITS ETF USD EUR
2  Amundi Index Solutions - Amundi Global Infrast...
3  Amundi Index Solutions - Amundi Index FTSE EPR...
4  Amundi Index Solutions - Amundi Index J.P. Mor...

                                           stars
0  http://tools.morningstar.co.uk/img/4stars.gif
1  http://tools.morningstar.co.uk/img/5stars.gif
2                                             NA
3                                             NA
4                                             NA

```
