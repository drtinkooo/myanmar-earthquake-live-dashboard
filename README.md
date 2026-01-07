# Myanmar Earthquake Live Dashboard

A real-time, interactive web dashboard for monitoring earthquake activity in Myanmar and surrounding regions. Built with vanilla JavaScript, Leaflet.js, and Chart.js.

![Dashboard Preview](https://img.shields.io/badge/Status-Live-brightgreen)
![License](https://img.shields.io/badge/License-MIT-blue)
![USGS Data](https://img.shields.io/badge/Data-USGS%20Earthquake%20API-orange)

## Features

### Real-Time Earthquake Monitoring
- **Live Data**: Fetches earthquake data from the USGS Earthquake API
- **Auto-Refresh**: Automatically updates every 60 seconds
- **Myanmar Focus**: Filters earthquakes within Myanmar's geographic bounding box (Lat: 9.5-28.5, Lon: 92-101.5)

### Interactive Map
- **Dark Theme**: Uses CartoDB dark tiles for better visualization
- **Color-Coded Markers**: Earthquakes displayed by magnitude severity
  - Red: M5.0+ (Major)
  - Orange: M4.0-4.9 (Moderate)
  - Yellow: M3.0-3.9 (Minor)
  - Green: M2.5-2.9 (Light)
- **Detailed Popups**: Click markers to view earthquake details (location, time, depth, status)
- **Tectonic Layer**: Displays Myanmar's tectonic fault lines with toggle control

### Statistics & Analytics
- **Summary Cards**: Total earthquakes, significant events (M5+), moderate events (M4-4.9), and latest event
- **Magnitude Distribution Chart**: Bar chart showing earthquake frequency by magnitude range
- **Scrollable Event List**: Clickable list that pans/zooms to selected earthquakes

### Filtering Options
- **Time Range**: 7 days, 30 days, 90 days, or 1 year
- **Minimum Magnitude**: Filter by 2.5+, 3.0+, 4.0+, or 5.0+

## Demo

Simply open `myanmar-earthquake-dashboard.html` in any modern web browser. No server or build process required.

## Installation

### Option 1: Direct Download
1. Download or clone this repository
2. Open `myanmar-earthquake-dashboard.html` in your browser

### Option 2: Clone Repository
```bash
git clone https://github.com/YOUR_USERNAME/myanmar-earthquake-dashboard.git
cd myanmar-earthquake-dashboard
# Open myanmar-earthquake-dashboard.html in your browser
```

### Option 3: GitHub Pages
Host directly on GitHub Pages for free:
1. Fork this repository
2. Go to Settings > Pages
3. Select "main" branch and save
4. Access at `https://YOUR_USERNAME.github.io/myanmar-earthquake-dashboard/`

## Usage

### Basic Navigation
- **Pan/Zoom**: Click and drag to pan, scroll to zoom
- **View Details**: Click any earthquake marker for detailed information
- **Focus on Event**: Click any item in the "Recent Earthquakes" list to zoom to that location

### Filtering Data
1. Use the **Time Range** buttons to select the time period (7 days to 1 year)
2. Use the **Minimum Magnitude** dropdown to filter by earthquake strength
3. Click **Refresh Now** to manually fetch the latest data

### Tectonic Layer
- Toggle the "Show Tectonic Layer" checkbox in the legend to display/hide fault lines
- Click on any fault line to view its name and details

## Data Sources

### Earthquake Data
- **Source**: [USGS Earthquake Hazards Program](https://earthquake.usgs.gov/)
- **API**: [USGS Earthquake Catalog API](https://earthquake.usgs.gov/fdsnws/event/1/)
- **Update Frequency**: Real-time data with 60-second auto-refresh

### Tectonic Data
- **Source**: Myanmar Tectonic Map 2011
- **Repository**: [myanmar-earthquake-archive](https://github.com/drtinkooo/myanmar-earthquake-archive)
- **Format**: GeoJSON containing fault line geometries

## Technology Stack

| Technology | Purpose |
|------------|---------|
| HTML5/CSS3 | Structure and styling |
| Vanilla JavaScript | Application logic |
| [Leaflet.js](https://leafletjs.com/) v1.9.4 | Interactive mapping |
| [Chart.js](https://www.chartjs.org/) | Data visualization |
| [CartoDB Dark](https://carto.com/basemaps/) | Map tiles |

## Project Structure

```
myanmar-earthquake-dashboard/
├── myanmar-earthquake-dashboard.html   # Main application (single-file)
├── README.md                           # This documentation
├── LICENSE                             # MIT License
├── CONTRIBUTING.md                     # Contribution guidelines
└── .gitignore                          # Git ignore file
```

## Configuration

The dashboard can be customized by modifying the configuration object in the JavaScript:

```javascript
const CONFIG = {
    refreshInterval: 60000,      // Auto-refresh interval (milliseconds)
    defaultDays: 365,            // Default time range
    defaultMinMagnitude: 2.5     // Default minimum magnitude filter
};

const MYANMAR_BOUNDS = {
    minLatitude: 9.5,            // Southern boundary
    maxLatitude: 28.5,           // Northern boundary
    minLongitude: 92.0,          // Western boundary
    maxLongitude: 101.5          // Eastern boundary
};
```

## Browser Support

| Browser | Support |
|---------|---------|
| Chrome | Full |
| Firefox | Full |
| Safari | Full |
| Edge | Full |
| IE11 | Not Supported |

## API Rate Limits

The USGS Earthquake API is free and does not require authentication. However, please be mindful of:
- Avoid excessive requests (the 60-second refresh interval is reasonable)
- For high-traffic applications, consider caching responses

## Contributing

Contributions are welcome! Please see [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

### Ideas for Contributions
- Add earthquake notifications/alerts
- Implement historical data comparison
- Add export functionality (CSV, PDF)
- Create mobile-responsive improvements
- Add additional data layers (population density, infrastructure)

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Acknowledgments

- **USGS Earthquake Hazards Program** for providing free, real-time earthquake data
- **Leaflet.js** community for the excellent mapping library
- **Chart.js** team for the charting library
- **Myanmar Geological Survey** for tectonic data

## Related Projects

- [USGS Earthquake Map](https://earthquake.usgs.gov/earthquakes/map/)
- [Myanmar Earthquake Archive](https://github.com/drtinkooo/myanmar-earthquake-archive)

## Contact

For questions or feedback, please [open an issue](https://github.com/YOUR_USERNAME/myanmar-earthquake-dashboard/issues).

---

**Disclaimer**: This dashboard is for informational purposes only. For official earthquake information and alerts, please refer to the [USGS](https://earthquake.usgs.gov/) and local authorities.
