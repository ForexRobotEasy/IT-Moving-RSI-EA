# IT Moving RSI EA

This code is an Expert Advisor (EA) written in MQL5 for the MetaTrader 5 platform. The EA is designed to trade based on the combination of the Moving Average and Relative Strength Index (RSI) indicators.

## Input Parameters

- RSI_Period: The period used for calculating the RSI indicator (default: 14).
- MA_Period: The period used for calculating the Moving Average indicator (default: 20).
- StopLoss: The stop loss level in points (default: 100).
- TakeProfit: The take profit level in points (default: 200).
- LotSize: The lot size for trading (default: 0.1).

## Initialization

The EA includes necessary libraries such as Trade.mqh, MovingAverages.mqh, and RSI.mqh. It also defines global variables for the trade object, moving averages object, and RSI object.

The `OnInit()` function is used for custom initialization. It sets up the Moving Averages and RSI indicators by setting the symbol and period.

## Deinitialization

The `OnDeinit()` function is called when the EA is being deinitialized. It cleans up the objects by calling the `Deinit()` function of the moving averages and RSI indicators.

## Tick Event

The `OnTick()` function is called on every tick. It calculates the moving average and RSI values using the `iMA()` and `iRSI()` functions. 

If the RSI value is above 70 and the current bid price is below the moving average, a sell trade is opened using the `Sell()` function of the trade object. The trade action is logged using the `Print()` function.

If the RSI value is below 30 and the current ask price is above the moving average, a buy trade is opened using the `Buy()` function of the trade object. The trade action is logged using the `Print()` function.

## Trade Event

The `OnTrade()` function is called when there is a trade event. It checks for closed trades using the `HistoryTotal()` function. If a sell trade is closed, the details of the trade (lots, entry price, and profit) are logged. If a buy trade is closed, the details are also logged.

## Product Description

This code is an example of an Expert Advisor (EA) that uses the Moving Average and RSI indicators to trade in the Forex market. 

The EA opens a sell trade when the RSI value is above 70 and the price is below the moving average. It opens a buy trade when the RSI value is below 30 and the price is above the moving average. The EA includes stop loss and take profit levels to manage risk and potential profits.

Please note that this code is provided as a sample and is not the official product developed by ForexRobotEasy. To find the official developer of this product, please refer to the MQL5 platform.

For detailed reviews and trading results of this product, please visit [Forex Robot Easy](https://forexroboteasy.com/forex-robot-review/it-moving-rsi-ea-review-empowering-forex-trading-insights/).
