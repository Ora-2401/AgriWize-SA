# AgriWise SA: Smart Agriculture Companion

## Project Summary

**AgriWise SA** is an AI-powered smart agriculture assistant designed specifically for South African farmers. It leverages predictive analytics to provide real-time weather forecasts, AI-based crop recommendations, profitability insights, and market trend analysis. This intelligent agent empowers farmers to make informed, data-driven decisions about which crops to plant and when, improving yield and financial outcomes.

## Project Goals

- Deliver seasonal crop recommendations using region-specific data
- Provide real-time weather insights to guide farming schedules
- Analyze market trends to highlight profitable opportunities
- Make farming more accessible through an intuitive, no-code prototype

## Installation Instructions

### 🔗 Prerequisites

- Web browser (Chrome, Firefox, Safari)
- Glide account (for cloning/editing the app)
- Internet access

### Setup Steps

1. **View the prototype in Creatie:**

   - Visit [Creatie](https://creatie.ai/file/161857066902119?fileOpenFrom=home&fileTileSwitch=false&page_id=25%3A7226&layer_id=25%3A75416)
   - Search or import the AgriWise SA prototype link

2. **Connect Data Sources:**

   - Use Google Sheets or Glide Tables with crop data, weather sources, and market values

3. **Configure API Integrations (Optional):**

   ```
   Weather API Key = YOUR_API_KEY
   Market API Endpoint = https://api.marketdata.za/v1/
   ```

4. **Publish & Test:**

   - Customize branding, add team members
   - Publish to web/mobile

## Usage Examples

### Quick Start

1. Open the AgriWise App
2. Log in using your email
3. Choose your province and season
4. Receive crop recommendations instantly

### Detailed Workflow

1. Select “Weather Forecast” to view your region’s 7-day outlook
2. Tap “Market Trends” to compare crop prices by region
3. Navigate to “Crop Library” to explore optimal planting times
4. Use the planting guide and expert tips for smarter planning

## Visual Aids

### Screenshots

- Welcome/Login Screen
![My Screenshot](Resources/Pictures/WelcomePage.jpg)
- Weather Dashboard
![My Screenshot](Resources/Pictures/WeatherAnalysispage.jpg)
- Market Analytics
![My Screenshot](Resources/Pictures/MarketAnalysis.jpg)
- Crop Detail View
![My Screenshot](Resources/Pictures/cropCategory.jpg)

### Video Demo

- Display as to how the Prototype works:
[![Watch Demo](Resources/Pictures/WelcomePage.jpg)](Resources/Pictures/DisplayOfPrototype.mp4)


### Flow Diagram

```mermaid
flowchart TD
    A["Start: Open AgriWise SA App"] --> B["Welcome Screen"]
    B --> C["Login / Sign Up"]
    C --> D{"Authenticated?"}
    D -- "Yes" --> E["Dashboard"]
    D -- "No" --> C
    
    E --> F["Select Province & Season"]
    F --> G{"Enter Optional Data?"}
    G -- "Yes" --> G1["Enter Soil Type, Rainfall, Temperature"]
    G -- "No" --> H
    G1 --> H["Fetch Weather Data"]
    
    H --> H1{"API Success?"}
    H1 -- "No" --> H2["Use Default Conditions"]
    H1 -- "Yes" --> I["Preprocess Data"]
    H2 --> I
    
    I --> J["Run Crop Matching Algorithm"]
    J --> K["Calculate Profit Scores"]
    K --> L["Display Top 3 Crop Recommendations"]
    L --> M["View Crop Details"]
    
    E --> N["Edit Profile / Terms"]
    M --> N
    
    E --> O["Open Navigation"]
    O --> P{"Exit App?"}
    P -- "Yes" --> Q["Confirm Exit?"]
    Q -- "Yes" --> R["Close App"]
    Q -- "No" --> E
    P -- "No" --> E

    subgraph "User Interface"
        direction TB
        B
        C
        E
        L
        M
        N
        O
        Q
    end
    
    subgraph "Data Input"
        direction TB
        F
        G
        G1
    end
    
    subgraph "AI Engine"
        direction TB
        I
        J
        K
    end
    
    subgraph "External APIs"
        direction TB
        H
        H1
        H2
    end

    classDef user fill:#64B5F6,stroke:#1565C0,stroke-width:2px
    classDef ai fill:#FFB300,stroke:#C62828,stroke-width:2px
    classDef data fill:#81C784,stroke:#2E7D32,stroke-width:2px
    classDef system fill:#9575CD,stroke:#4527A0,stroke-width:2px
    classDef decision fill:#FF8A65,stroke:#BF360C,stroke-width:2px
    classDef startEnd fill:#00695C,stroke:#003300,color:#E0F7FA,stroke-width:2px
    
    class A,R startEnd
    class D,G,H1,P,Q decision
    class B,C,E,L,M,N,O user
    class F,G1 data
    class I,J,K ai
    class H,H2 system
```
## Table of Contents

- [Project Summary](#project-summary)
- [Project Goals](#project-goals)
- [Installation Instructions](#installation-instructions)
- [Usage Examples](#usage-examples)
- [Visual Aids](#visual-aids)
- [Technical Overview](#technical-overview)
- [User Interaction](#user-interaction)
- [Landing Page](#landing-page)

## Technical Overview

### Core AI Flow

1. **User Input**: Province, Season, Soil Data, Rainfall
2. **Preprocessing**: Cleans data and assigns scores
3. **AI Prediction**: Matches input to crops and calculates profitability scores
4. **Output**: Displays top 3 crops with detailed profiles

### 🔧 Data & API Dependencies

| Component        | Function                                           |
| ---------------- | -------------------------------------------------- |
| Weather API      | Real-time weather metrics                          |
| Crop Dataset     | Historical yield, demand, seasonal info            |
| AI Crop Model    | Matches user input to top-performing crops         |
| Output Interface | Renders charts, tables, actionable recommendations |
| Fallback Logic   | Uses static dataset when APIs fail                 |

## User Interaction

- **Input**: Province, season, and farming conditions
- **View**: Real-time weather, expert crop advice, and market trends
- **Navigation**: Simple tab bar + logout/exit confirmation
- **Crop Details**: Tap entries for in-depth planting and care tips

## Landing Page

You can view and explore AgriWise SA via its public landing page:

- **Video Demo**: Available Above — link above
- **Creatie Prototype**: View and duplicate directly via [Creatie](https://www.glideapps.com/)

## Notes

- Built using **Readdy.ai** (no-code platform)
- Easily adaptable to include more provinces, crops, or user profiles
- Ideal for agricultural support programs, extension workers, and farming cooperatives
- Demonstrates use of an **AI Agent** for **predictive analysis** in agriculture
