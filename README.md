# SpreadRecorder TrustfulTrading

This code is a sample implementation of a spread recorder in MQL5. It records the current spread of a trading symbol and stores it in a CSV file. The code consists of several functions:

## Global Variables
- `fileName`: The name of the file to store the spread data.

## OnInit Function
- This function is executed once when the Expert Advisor is initialized.
- It creates a file to store spread data using the `FileOpen` function with the `FILE_WRITE` and `FILE_TXT` flags.
- If the file is created successfully, it is closed. Otherwise, an error message is printed.

## OnTick Function
- This function is executed on every tick of the symbol.
- It gets the current spread of the symbol using the `MarketInfo` function with the `MODE_SPREAD` parameter.
- It appends the spread data to the file using the `FileOpen`, `FileWrite`, and `FileClose` functions.
- If the file is opened successfully, the spread value is printed. Otherwise, an error message is printed.

## GenerateSpreadFile Function
- This function is used to generate a new file with the spread values.
- It opens the file created in the `OnInit` function using the `FileOpen` function with the `FILE_READ` and `FILE_TXT` flags.
- If the file is opened successfully, it reads the spread data using the `FileReadString` function and closes the file.
- It then creates a new file named 'spread_values.csv' using the `FileOpen` function with the `FILE_WRITE` and `FILE_TXT` flags.
- If the new file is created successfully, it writes the spread data to the file using the `FileWrite` function and closes the file.
- If any errors occur during the process, error messages are printed.

## SpreadRecorderTrustfulTrading Function
- This function is the main entry point of the Expert Advisor.
- It calls the `OnInit` function to create the file for spread data.
- It calls the `OnTick` function to record live spreads in real-time.
- It calls the `GenerateSpreadFile` function to generate a spread values file.

Please note that this code is not the official product code for SpreadRecorder TrustfulTrading. ForexRobotEasy, the developer of this code, is not the official developer of this product. This code is provided as a sample implementation that can work similarly to the SpreadRecorder TrustfulTrading software. To find the official developer of this product, please refer to MQL5.

For detailed reviews and trading results of the SpreadRecorder TrustfulTrading product, please visit [forexroboteasy.com](https://forexroboteasy.com/forex-robot-review/spreadrecorder-trustfultrading-review-of-forex-algo-trading-software/).
