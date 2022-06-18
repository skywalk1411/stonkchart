# https://stonkch.art - about

Welcome to stonkch.art,

 ~ is a popular charting terminal for the stock market, cryptocurrencies and more. Powered by TradingView data.
 
 ~ mission is to provide one simple but powerful interface to quickly display a chart on the screen. 
 
 ~ also provide almost all tools supported on the TradingView platform.
 
 ~ take a strong and respectful stance on user privacy and security. We support Do Not Track settings.
 
 ~ may currently be sending analytics to a third party of TradingView, please refer to TradingView ToS.
 
 ~ traffic to our website and APIs is encrypted.
 
 ~ currently run using nodejs, express in backend using TradingView data.
 
 ~ has plans to move the platform to use tradingvue-js and vuejs in the future.
 
 ~ url is short and perfect to reference a certain chart quickly like bellow.
 
# Example url with parameters
* https://stonkch.art
* https://stonkch.art/exchange/symbol (ex: https://stonkch.art/nyse/amc )
* https://stonkch.art/m/exchange/symbol (ex: https://stonkch.art/m/nasdaq/tsla )
  > or long format https://stonkch.art/min/exchange/symbol (ex: https://stonkch.art/min/nasdaq/tsla )
* https://stonkch.art/l/exchange/symbol (ex:  https://stonkch.art/l/binance/btcusdt )
  > or long format https://stonkch.art/lite/exchange/symbol (ex:  https://stonkch.art/lite/binance/btcusdt )
* https://stonkch.art/o/yahooSymbol (ex: https://stonkch.art/o/tsla )
 > or long format https://stonkch.art/old/yahooSymbol (ex: https://stonkch.art/old/btc-usd , https://stonkch.art/old/^cmc200 , https://stonkch.art/old/gc=f )
* https://stonkch.art/?s=EXCHANGE:SYMBOL (ex: http://stonkch.art/?s=NASDAQ:TSLA )
  > or long format https://stonkch.art/?symbol=BITMEX:XBTUSD
* https://stonkch.art/?s=EXCHANGE:SYMBOL&i=30
  > or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30
* https://stonkch.art/?s=EXCHANGE:SYMBOL&i=30&t=light
  > or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light
* https://stonkch.art/?s=EXCHANGE:SYMBOL&i=30&t=light&b1=MACD
  > or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD
* https://stonkch.art/?s=EXCHANGE:SYMBOL&i=30&t=light&b1=MACD&b2=RSI
  > or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD&basics2=RSI
* https://stonkch.art/m/?s=EXCHANGE:SYMBOL&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
  > or long format  https://stonkch.art/min/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* https://stonkch.art/l/?s=EXCHANGE:SYMBOL&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
  > or long format  https://stonkch.art/lite/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* https://stonkch.art/i/tsla

# Description
* Routes
  * /
  * /min or /m
  * /lite or /l
  * /img or /i
  * /old or /o
  * /xdebug or /xd
  * /exchange/symbol
  * /exchange/symbol/exchange/symbol/... (@@@to do)
  * /old/symbol or /o/symbol (ex: https://stonkch.art/old/tsm (use yahoo symbols)) 
  * /rss2api/fullUrlToRss URIEncoded (ex: https://stonkch.art/rss2api/http%3A%2F%2Ffeeds.feedburner.com%2Fzerohedge%2Ffeed )
  * /api2api/fullUrlToApi URIEncoded (ex: https://stonkch.art/api2api/https%3A%2F%2Fquery2.finance.yahoo.com%2Fv7%2Ffinance%2Fquote%3Fformatted%3Dtrue%26crumb%3DJA3EgfRNNMR%26lang%3Den-US%26region%3DUS%26symbols%3Damc%2Cgme%2Cpltr%2Cnok%2Cbb%2Cbtc-usd%2Ceth-usd%2Cltc-usd%2Cdoge-usd%26fields%3Dsymbol%2CregularMarketPrice%26corsDomain%3Dfinance.yahoo.com )

* Routes explanation
  * / is main root webpage with all features.
  * /min is minimal chart minus the extra tools.
  * /lite is the most lightweight chart, uneditable with no tools.
  * /old is a vintage google chart with yahoo data.
  * /img is a small yahoo api powered png chart financial 400x400pixels image ~16kb.
  * /xdebug is the json img chart data for debuging chart.
  * /exchange/symbol is a quick way to load a specific exchange/symbol chart.
  * /rss2api is a rss to api mirror.
  * /api2api is a api to api mirror.

* Charts

Route | Editable | Parameters | Afterhours | Draw | Bars | Details | Watchlist | Calendar | Hotlists
----- | -------- | ---------- | ---------- | ---- | ---- | ------- | --------- | -------- | --------
/     | yes      | yes       | yes        | yes     | yes       | yes     | yes       | yes      | yes
/min  | yes      | yes       | yes        | yes     | yes       | no      | no        | no       | no
/lite | no       | yes       | yes        | no      | no        | no      | no        | no       | no


* Parameters /? (only the first parameter require /?, separate additional parameters with &)
  * ?symbol=EXCHANGE:TICKER* or ?s=EXCHANGE:TICKER*
  * ?interval=validIntervals* or ?i=validIntervals*
  * ?theme=validThemes* or ?t=validThemes*
  * ?basics1=validStudies* or ?b1=validStudies*
  * ?basics2=validStudies* or ?b2=validStudies*
  * ?basics3=validStudies* or ?b3=validStudies*
  * ?style=validStyles* or ?st=validStyles*
  * ?locale=validLocales* or ?l=validLocales*
  * ?timezone=validTimezones* or ?tz=validTimezones* or ?timezone=validUTCs* or tz=validUTCs*


* EXCHANGE:TICKER*
  ```NASDAQ:TSLA, NYSE:GME, TSX:TGOD, BITMEX:XBTUSD, BINANCE:BTCUSDT, AMEX:SPY, FOREXCOM:SPXUSD, FX_IDC:EURUSD``` or [TradingView supported symbols.](https://www.tradingview.com/widget/#AvailableMarketsForWidgets)
  
   Default symbol is NYSE:GME or the most PercentGainer from TradingView if world markets are open, otherwise BITMEX:XBTUSD if world markets closed.
  
* validIntervals*
  ```1, 3, 5, 15, 30, 60, 120, 180, 240, D, W```
  
   Default interval is 30.
  
* validThemes*
  ```dark, light```
  
   Default theme is dark.
  
* validStudies* 
  (maximum 3 studies, basics1, basics2 and basics3 or b1, b2 and b3)
  
  ```ACCD, studyADR, AROON, ATR, AwesomeOscillator, BB, BollingerBandsR, BollingerBandsWidth, CMF, ChaikinOscillator, chandeMO, ChoppinessIndex, CCI, CRSI, CorrelationCoefficient, DetrendedPriceOscillator, DM, DONCH, DoubleEMA, EaseOfMovement, EFI, ENV, FisherTransform, HV, hullMA, IchimokuCloud, KLTNR, KST, LinearRegression, MACD, MOM, MF, MoonPhases, MASimple, MAExp, MAWeighted, OBV, PSAR, PivotPointsHighLow, PivotPointsStandard, PriceOsc, PriceVolumeTrend, ROC, RSI, VigorIndex, VolatilityIndex, SMIErgodicIndicator, SMIErgodicOscillator, Stochastic, StochasticRSI, TripleEMA, Trix, UltimateOsc, VSTOP, Volume, VWAP, MAVolumeWeighted, WilliamR, WilliamsAlligator, WilliamsFractal, ZigZag```
  
   There is no default studies.
  
* validStyles*
  ```0 = bars, 1 = candles, 2 = hollow candles, 3 = heikin ashi, 4 = line, 5 = area, 6 = baseline, 7 = renko, 8 = line break, 9 = kagi, 10 = points and figure, 11 = range```
  
   Default Style is candles.
  
* validLocales*
  ```en, uk, in, de_DE, fr, es, it, pl, hu_HU, sv_SE, tr, ru, br, id, ms_MY, th_TH, vi_VN, ja, kr, zh_CN, zh_TW, ar_AE, he_IL, fa_IR```
  
   Default Locale is en.
  
* validTimezones*
  ```Etc/UTC, exchange, Pacific/Honolulu, America/Juneau, America/Los_Angeles, America/Phoenix, America/Vancouver, US/Mountain, America/Mexico_City, America/El_Salvador, America/Bogota, America/Chicago, America/Lima, America/Caracas, America/New_York, America/Toronto, America/Argentina/Buenos_Aires, America/Santiago, America/Sao_Paulo, Atlantic/Reykjavik, Europe/Dublin, Africa/Lagos, Europe/Lisbon, Europe/London, Europe/Amsterdam, Europe/Belgrade, Europe/Berlin, Europe/Brussels, Africa/Cairo, Europe/Copenhagen, Africa/Johannesburg, Europe/Luxembourg, Europe/Madrid, Europe/Malta, Europe/Oslo, Europe/Paris, Europe/Rome, Europe/Stockholm, Europe/Warsaw, Europe/Zurich, Europe/Athens, Asia/Bahrain, Europe/Helsinki, Europe/Istanbul, Asia/Jerusalem, Asia/Kuwait, Europe/Moscow, Asia/Qatar, Europe/Riga, Asia/Riyadh, Europe/Tallinn, Europe/Vilnius, Asia/Dubai, Asia/Muscat, Asia/Tehran, Asia/Ashkhabad, Asia/Kolkata, Asia/Almaty, Asia/Bangkok, Asia/Ho_Chi_Minh, Asia/Jakartar, Asia/Chongqing, Asia/Hong_Kong, Australia/Perth, Asia/Shanghai, Asia/Singapore, Asia/Taipei, Asia/Seoul, Asia/Tokyo, Australia/Brisbane, Australia/Adelaide, Pacific/Norfolk, Australia/Sydney, Pacific/Auckland, Pacific/Chatham, Pacific/Fakaofo```
  
   Default Timezone is exchange.

* validUTCs*
  ```Etc/UTC, exchange, UTC-10, UTC-8, UTC-7, UTC-7, UTC-7, UTC-6, UTC-6, UTC-6, UTC-5, UTC-5, UTC-5, UTC-4, UTC-4, UTC-4, UTC-3, UTC-3, UTC-3, UTC, UTC+1, UTC+1, UTC+1, UTC+1, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+2, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+3, UTC+4, UTC+4, UTC+4:30, UTC+5, UTC+5:30, UTC+6, UTC+7, UTC+7, UTC+7, UTC+8, UTC+8, UTC+8, UTC+8, UTC+8, UTC+8, UTC+9, UTC+9, UTC+10, UTC+10:30, UTC+11, UTC+11, UTC+12, UTC+12:45, UTC+13```
  
   Default UTC is Etc/UTC.
