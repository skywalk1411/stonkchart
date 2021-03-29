# http://stonkch.art - stonkch.art

stonkch.art is a nodejs webserver to display charts using tradingview widget api. Also have yahoo finance api mirror.

# Example url with parameters
* http://stonkch.art/?s=BITMEX:XBTUSD or http://stonkch.art/?s=NASDAQ:TSLA or ...
* or long format http://stonkch.art/?symbol=BITMEX:XBTUSD
* http://stonkch.art/?s=BITMEX:XBTUSD&i=30
* or long format  http://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30
* http://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light
* or long format  http://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light
* http://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD
* or long format  http://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD
* http://stonkch.art/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI
* or long format  http://stonkch.art/?symbol=BITMEX:XBTUSD&interval=30&theme=light&basics1=MACD&basics2=RSI
* http://stonkch.art/m/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* or long format  http://stonkch.art/min/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* http://stonkch.art/l/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple
* or long format  http://stonkch.art/lite/?s=BITMEX:XBTUSD&i=30&t=light&b1=MACD&b2=RSI&b3=MASimple

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
