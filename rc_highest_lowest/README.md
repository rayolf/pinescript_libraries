# Pine Script Library: rc_highest_lowest

Welcome to the **rc_highest_lowest** library! This library provides two essential functions to help you identify the highest and lowest prices within a specified range of candles on your TradingView charts. It's a simple and powerful tool for technical analysts and traders looking to pinpoint critical market levels with ease.

## Overview

The `rc_highest_lowest` library includes two primary functions:
1. `f_highest`: Returns the highest price and its index within a specified range of bars (candles).
2. `f_lowest`: Returns the lowest price and its index within a specified range of bars (candles).

### Key Features:
- **Dynamic Range Selection**: Analyze any range of bars by specifying start and end points.
- **Precise Price and Index Detection**: Get both the price value and its corresponding index within the range.
- **Easy to Use**: Simple functions that can be easily integrated into any Pine Script project.

## Functions

### 1. `f_highest(start, end)`
This function finds the highest price within the range of candles you define.

**Parameters:**
- `start` (int): The starting bar index for the range.
- `end` (int): The ending bar index for the range.

**Returns:**  
- `index_result`: The index of the highest price within the range.
- `price_result`: The highest price within the range.

### Example:
```pinescript
//@version=5
indicator("Highest Price Example", overlay=true)

import "user/repository_name" as lib

[start, end] = [10, 50]
[index_high, high_price] = lib.f_highest(start, end)
plot(high_price, color=color.green, title="Highest Price")
