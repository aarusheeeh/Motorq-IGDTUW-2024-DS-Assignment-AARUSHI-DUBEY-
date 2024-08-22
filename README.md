# Motorq-IGDTUW-2024-DS-Assignment-AARUSHI-DUBEY-

When working with vehicle telemetry data and calculating metrics like fuel economy, several assumptions may be made. Here are some common ones:

### 1. **Linear Consumption Between Telemetry Points**
   - **Assumption**: Fuel consumption and other metrics (like distance traveled) change linearly between recorded telemetry points if no intermediate data is available.
   - **Implication**: This means that the data between two timestamps is assumed to vary at a constant rate, which simplifies calculations but may not always reflect real-world variations.

### 2. **Consistent Measurement Intervals**
   - **Assumption**: The telemetry data is collected at regular intervals, and any missing data is assumed to follow a similar pattern.
   - **Implication**: If the intervals are irregular, the assumptions about linearity might not hold, potentially leading to inaccurate calculations.

### 3. **Odometer Values Should Always Increase**
   - **Assumption**: Odometer readings should never decrease as the vehicle is assumed to always be moving forward(No negative values).
   - **Implication**: Any decreases in odometer readings are considered anomalies or errors and are handled by setting those values to NaN.

### 4. **Fuel Level as a Percentage of Tank Capacity**
   - **Assumption**: The fuel level is expressed as a percentage of the total tank capacity, and changes in fuel level can be directly converted to fuel used.
   - **Implication**: This assumes that the fuel level percentage is accurate and represents a straightforward proportional change.

### 5. **No External Factors Affecting Fuel Economy**
   - **Assumption**: The calculation of fuel economy (MPG) does not consider external factors such as driving conditions, vehicle load, or maintenance.
   - **Implication**: This simplification assumes that fuel consumption is only affected by the parameters in the dataset.

### 6. **Consistency in Telemetry Reporting**
   - **Assumption**: Telemetry data from different sources (Telemetry 1 and Telemetry 2) are reported in a consistent manner.
   - **Implication**: Differences in reporting formats or scales might need to be addressed to ensure accurate data integration.

### 8. **Handling of Missing Values**
   - **Assumption**: Missing values are handled by forward-filling or backward-filling, assuming that missing data can be reasonably estimated from adjacent values.
   - **Implication**: This method assumes that the data points around missing values are representative of the missing values, which might not always be true.

These assumptions are important to understand and consider as they affect the accuracy and reliability of the analysis and results derived from the data.
