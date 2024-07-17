
# CryptoSMA200Analyzer

CryptoSMA200Analyzer is a Python script that retrieves historical data for cryptocurrencies using the CCXT library. It identifies symbols ending with USDT where the price is greater than and close to the current SMA200 value. The data is organized in a table form, sorted based on the proximity to the SMA200 value, and excludes stablecoins.

## Description

This script was created by AI to assist in analyzing cryptocurrency prices relative to their SMA200 (Simple Moving Average of 200 periods) on a 1-hour timeframe. The script filters out stablecoins and only considers symbols ending with USDT.

## Installation

To run this script, you need to have Python installed on your machine. You can install the required libraries using pip:

```bash
pip install ccxt pandas numpy
``` 

## Usage

1. Clone the repository or download the script file.

2. Run the script:

```bash
python CryptoSMA200Analyzer.py
```

3. The script will output a table with the following columns:
   - Symbol: The cryptocurrency symbol.
   - Current Price: The current price of the cryptocurrency.
   - SMA200: The current SMA200 value.
   - Proximity: The proximity of the current price to the SMA200 value.

## Example Output

```plaintext
         Symbol  Current Price       SMA200  Proximity
0  BTC/USDT      40000.00      39500.00  0.012658
1  ETH/USDT       2500.00       2470.00  0.012146
...
```

## Notes

- The script filters out stablecoins to avoid unnecessary analysis.
- The proximity threshold is set to 5% of the SMA200 value.
- The script handles exceptions and skips symbols that cause errors during data retrieval.
