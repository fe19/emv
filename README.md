# EMV Measurements Dashboard

A web application for analyzing electromagnetic field measurements from CSV files.

## Technologies

- HTML5
- CSS3
- JavaScript (ES6)
- Bootstrap 5.3.3
- Chart.js 4.4.6 (with zoom and date-fns adapter plugins)

## How to View

Open `index.html` in a web browser.

## Features

- CSV file import and parsing
- Three interactive charts: EF (V/m), RF Power Density (mW/m²), and EMF (mG)
- Synchronized zoom and pan across all charts
- Source filtering (Static, Mixed, WiFi/Phone)
- Adjustable Y-axis ranges for each chart
- Smoothing/windowing function for data averaging
- Summary statistics table (count, min, max, mean, median, p95)
- Responsive design with Bootstrap

## Behavior

### HTML (`index.html`)
- Builds the dashboard layout with toolbar, chart containers, and summary table
- Integrates Bootstrap framework and Chart.js libraries

### CSS (`styles.css`)
- Styles the device selector with custom dropdown arrow
- Defines chart container dimensions and responsive behavior
- Formats the Y-range input controls and source filter checkboxes

### JavaScript (`script.js`)
- **CSV Parser**: Parses CSV files starting from line 3, extracting timestamp, EMF, EF, RF, and source
- **Data Filtering**: Filters measurements by selected source checkboxes
- **Chart Management**: Creates and updates three Chart.js line charts with time-series X-axis
- **Synchronization**: Keeps zoom/pan ranges in sync across all charts
- **Smoothing**: Applies moving average window to data for noise reduction
- **Statistics**: Calculates min, max, mean, median, and p95 quantile for each metric
- **Event Handling**: Manages file input, source filters, and Y-range/smoothing adjustments
