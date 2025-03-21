# Solar Potential Analysis Tool

An advanced web application for analyzing solar potential on buildings using Google Maps Platform and Solar API.

## Features

### Core Functionality
- Building insights analysis using Google Solar API
- Data layer visualization (roof mask, DSM, aerial imagery, flux maps)
- Solar panel placement visualization
- Energy production estimates

### Advanced Solar Panel Placement & Roof Logic
- **Setback Rules**:
  - Configurable setbacks from roof edges (default: 4ft)
  - 4ft clearance around obstructions (HVAC, vents, skylights)
  - Jurisdiction-specific presets (California, Arizona, Florida, Texas)

- **Access Paths**:
  - Auto-generated maintenance walkways between panel rows
  - Configurable walkway width (default: 3.5ft)

- **Layout Optimization**:
  - Grid-aligned linear blocks for optimal installation
  - Orientation priority (South > West > East > North)
  - Installation cost estimates based on labor time

### Energy Rate Calculations
- **Rate Data Integration**:
  - EIA API for historical rate data
  - County-level rate escalation (4.23% national default)
  - Regional comparisons using Census division data

- **Bill Breakdown**:
  - Base energy rate
  - Delivery charges
  - Demand charges
  - Regulatory fees
  - Location surcharges

### ROI Modeling
- **Financial Engine**:
  - Interactive sliders for rate escalation (4-20% range)
  - Panel degradation adjustment (0.5-1% annual)
  - Financing terms configuration
  - 25-year cash flow projections
  - Payback period calculation
  - IRR and NPV metrics

## Getting Started

### Prerequisites
- Google Maps API key with Solar API enabled
- Modern web browser

### Installation
1. Clone the repository
2. Install dependencies:
   ```
   npm install
   ```
3. Create a `.env` file with your Google Maps API key:
   ```
   GOOGLE_MAPS_API_KEY=your_api_key_here
   ```
4. Start the development server:
   ```
   npm run dev
   ```

## Technical Details

### Key Dependencies
- Svelte/SvelteKit for UI framework
- Google Maps JavaScript API
- Google Solar API
- Material Web Components
- TailwindCSS for styling

### Architecture
- Component-based UI with Svelte
- Service-based data handling
- Responsive design for desktop and mobile

## License
Licensed under the Apache License, Version 2.0
#   I m p e r i u m - S o l a r - B a c k e n d  
 #   I m p e r i u m - S o l a r - B a c k e n d  
 