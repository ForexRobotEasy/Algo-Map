# Algo Map - Non-repainting Indicator Feature

This is the code for the Algo Map indicator, a non-repainting forex indicator developed by the Forex Robot Easy Team. This indicator analyzes data using a specified period and generates signals based on the analysis. The signals are then stored in a buffer for further use.

## Indicator Input Parameters

- `period` (default: 14): The period for data analysis.

## Indicator Buffers

- `buffer[]`: The buffer used to store the generated signals.

## Custom Indicator Initialization Function

The `OnInit()` function is called during the indicator initialization process. In this function, the indicator buffers are mapped and the indicator properties are defined.

- Indicator buffers mapping: The `SetIndexBuffer()` function is used to map the `buffer[]` to the first index buffer.
- Indicator properties definition: The `IndicatorSetInteger()` and `IndicatorSetString()` functions are used to define the indicator properties. In this code, the indicator digits are set to 5 and the indicator shortname is set to 'AlgoMap'.
- Indicator labels: The `SetIndexLabel()` function is used to set the label for the first index buffer as 'Algo Map'.

## Custom Indicator Iteration Function

The `OnCalculate()` function is called during each indicator calculation iteration. In this function, the indicator values are calculated and signals are generated.

- Calculation of indicator values: The `limit` variable is calculated as the difference between `rates_total` and `prev_calculated`. This represents the number of bars that need to be calculated.
- Signal generation: A loop is used to iterate over the bars that need to be calculated. For each bar, the `iMA()` function is called to perform the data analysis and generate a signal. The signal is then stored in the `buffer[]`.
- Return value: The `rates_total` is returned to indicate the total number of bars.

## Product Description

Algo Map is a non-repainting forex indicator developed by the Forex Robot Easy Team. It is designed to analyze data using a specified period and generate signals based on the analysis. The signals are stored in a buffer for further use.

This indicator is customizable with the input parameter `period`, allowing users to adjust the period for data analysis according to their trading preferences.

Algo Map is a reliable tool for forex traders as it does not repaint signals, ensuring that the generated signals remain consistent and accurate. It can be used in various trading strategies to identify potential entry and exit points.

Please note that ForexRobotEasy is not the official developer of this product. We are only providing a sample code that demonstrates how this indicator works. To find the official developer of this product and access detailed reviews and trading results, please visit [Forex Robot Easy - Algo Map Review](https://forexroboteasy.com/forex-robot-review/algo-map-review-non-repainting-forex-software-at-45/). For further information and support, we recommend using MQL5, the official platform for MetaTrader indicators and expert advisors.
