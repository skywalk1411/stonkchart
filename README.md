# http://stonkch.art - about

Welcome to stonkch.art,
 ~ is a popular charting terminal for the stock market, cryptocurrencies and more using TradingView data.
 
 ~ mission is to provide one simple but powerful interface to quickly display a chart on the screen. 
 
 ~ also provide almost all tools supported on the TradingView platform.
 
 ~ take a strong and respectful stance on user privacy and security. We support Do Not Track settings.
 
 ~ may currently be sending analytics to a third party of TradingView, please refer to TradingView ToS.
 
 ~ traffic to our website and APIs is encrypted.
 
 ~ currently run using nodejs in backend using TradingView data.
 
 ~ has plans to move the platform to use tradingvue-js and vuejs and/or express in the future.
 
 ~ url is short and perfect to reference a certain chart quickly like bellow.
 

# Example url with parameters
* https://stonkch.art
* https://stonkch.art/?wl=penny
* or long format https://stonkch.art/?watchlist=penny
* https://stonkch.art/?s=BITMEX:XBTUSD or http://stonkch.art/?s=NASDAQ:TSLA or ...
* or long format https://stonkch.art/?symbol=BITMEX:XBTUSD
* https://stonkch.art/?s=BITMEX:XBTUSD&i=30
* or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30
* https://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light
* or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light
* https://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD
* or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD
* https://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI
* or long format  https://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD&basics2=RSI
* https://stonkch.art/m/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* or long format  https://stonkch.art/min/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* https://stonkch.art/l/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* or long format  https://stonkch.art/lite/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple

# Description
* Routes
  * /
  * /min or /m
  * /lite or /l
  * /v1, /v7, v8, v10 (any valid yahoo finance api request).

* Routes explanation
  * / is main root webpage with all features.
  * /min is minimal chart minus the extra tools.
  * /lite is the most lightweight chart, uneditable with no tools.

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
  * ?watchlist=validWatchlist* or ?wl=validWatchlist*


* EXCHANGE:TICKER*
  ```NASDAQ:TSLA, NYSE:GME, TSX:TGOD, BITMEX:XBTUSD, BINANCE:BTCUSDT, AMEX:SPY, FOREXCOM:SPXUSD, FX_IDC:EURUSD``` or [TradingView supported symbols.](https://www.tradingview.com/widget/#AvailableMarketsForWidgets)
  
* validIntervals*
  ```1, 3, 5, 15, 30, 60, 120, 180, 240, D, W```
  
* validThemes*
  ```dark, light```
  
* validStudies* 
  (maximum 3 studies, basics1, basics2 and basics3 or b1, b2 and b3)
  
  ```ACCD, studyADR, AROON, ATR, AwesomeOscillator, BB, BollingerBandsR, BollingerBandsWidth, CMF, ChaikinOscillator, chandeMO, ChoppinessIndex, CCI, CRSI, CorrelationCoefficient, DetrendedPriceOscillator, DM, DONCH, DoubleEMA, EaseOfMovement, EFI, ENV, FisherTransform, HV, hullMA, IchimokuCloud, KLTNR, KST, LinearRegression, MACD, MOM, MF, MoonPhases, MASimple, MAExp, MAWeighted, OBV, PSAR, PivotPointsHighLow, PivotPointsStandard, PriceOsc, PriceVolumeTrend, ROC, RSI, VigorIndex, VolatilityIndex, SMIErgodicIndicator, SMIErgodicOscillator, Stochastic, StochasticRSI, TripleEMA, Trix, UltimateOsc, VSTOP, Volume, VWAP, MAVolumeWeighted, WilliamR, WilliamsAlligator, WilliamsFractal, ZigZag```

* validWatchlist*
  ```penny, ```
