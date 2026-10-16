# Smart Home Control Dashboard

A fully functional, single-file **Smart Home Automation Dashboard** built with pure HTML, CSS, and JavaScript - no frameworks, no backend required.

---

## Features

### Navigation Tabs
| Tab | Description |
|---|---|
| **Overview** | Home status, environmental sensors (temp, humidity, light, smoke), quick stats |
| **Rooms & Devices** | Browse all rooms and control every smart device |
| **Energy Analytics** | Daily / Weekly / Monthly / Yearly power consumption with charts |
| **Automations** | Create smart rules, scenes, and schedules |
| **Notifications & Family Safety** | Alert types, family members, notification history |
| **CCTV & Security Center** | Live camera feeds with motion detection and alarm control |
| **Admin & Settings** | Roles, units (C/F), currency (INR/USD/EUR), system diagnostics |

---

### Rooms

| Room | Devices |
|---|---|
| **Living Room** | Ceiling Light, Ceiling Fan, Air Conditioner, Smart TV, Smart Plug, Curtains, Door Lock, Speaker |
| **Bedroom** | Bedside Lamp, Bedroom AC, Ceiling Fan, Smart TV, Speaker |
| **Kitchen** | Water Heater, Refrigerator, Kitchen Light, Smart Plug |
| **Hall** | Hall Camera (CCTV), Hall Light, Front Door Lock |
| **Garage** | Garage Camera (CCTV), Garage Light, Front Door Camera |

---

### Supported Device Types

| Device | Controls |
|---|---|
| Ceiling Light | On/Off + Brightness slider (0-100%) |
| Ceiling Fan | On/Off + Speed slider (1-5) |
| Air Conditioner | On/Off + Temperature step control |
| Smart TV | On/Off (Playing / Standby) |
| Smart Plug | On/Off power toggle |
| Curtains | On/Off + Open percentage slider (0-100%) |
| Door Lock | Lock / Unlock toggle |
| Speaker | On/Off + Volume slider (0-100%) |
| Water Heater | On/Off + Temperature monitoring |
| Refrigerator | On/Off + status |
| CCTV Camera | Live animated feed + Motion detection |

---

### Energy Analytics
- **Live Power Usage** - real-time wattage of all active devices
- **Consumption Trend** - smooth area chart over 24 hours
- **Device-wise Breakdown** - donut chart by appliance category
- **Cost Estimation** - supports INR, USD, EUR currencies
- **Carbon Footprint** - CO2 emission tracking
- **Time Frames** - Daily, Weekly, Monthly, Yearly views

---

### Automations
- **My Automations** - custom IF condition THEN action rules
- **Scenes** - one-tap presets (Good Night, Movie Time, etc.)
- **Suggestions** - AI-generated smart home recommendations
- **Recent Activity** - timeline log of all device events

---

### Notifications & Family Safety
- **Alert Types** - Device, Security, Energy, Safety, System alerts
- **Family Members** - Role-based access (Owner / Family / Guest)
- **Multi-channel** - SMS, Email, Push notification settings
- **Safety Alarm** - Emergency alarm with door-lock and recording trigger

---

### CCTV & Security
- **Live Camera Feeds** - animated canvas-based live simulation
- **REC indicator** - pulsing red recording badge
- **Motion Detection** - per-device motion state tracking
- **Alarm Panel** - arm/disarm with visual alert banner

---

## Technology Stack

| Layer | Technology |
|---|---|
| Structure | HTML5 (semantic, accessible) |
| Styling | Vanilla CSS (CSS variables, grid, animations) |
| Logic | Vanilla JavaScript (ES6+, no frameworks) |
| Icons | Lucide Icons (CDN) |
| Fonts | Instrument Sans (Google Fonts) |
| Charts | SVG (hand-crafted area chart + donut chart) |
| Images | Base64 embedded (4K-enhanced, no external assets) |

---

## Getting Started

### Requirements
- Any modern web browser (Chrome, Firefox, Edge, Safari)
- No server, no npm, no build step needed!

### Run Locally
1. Download or clone this repository
2. Open `Smart Home Control Dashboard.html` in your browser
3. That's it -- everything runs offline!

`ash
# Clone
git clone <your-repo-url>
cd Smart-Home-Automation

# Open in browser (Windows)
start "Smart Home Control Dashboard.html"

# Open in browser (macOS)
open "Smart Home Control Dashboard.html"

# Open in browser (Linux)
xdg-open "Smart Home Control Dashboard.html"
`

---

## Design Highlights

- **Dark Theme** - Deep navy palette (#0a0c10) with frosted card surfaces
- **Glass-morphism Cards** - Subtle borders and depth via layered backgrounds
- **Micro-animations** - Toggle switches, hover effects, pulsing live indicators
- **Responsive Layout** - Sidebar collapses to bottom nav on mobile
- **4K Room Images** - All room and device images enhanced to HD/4K resolution
- **2x Room Cards** - Large, immersive room selector cards (280px min-width, 168px height)
- **Live Indicators** - Animated dot pulsing for live status, camera REC badge

---

## CSS Architecture

`
CSS Variables (root)
|-- Colors:    --bg, --sf, --cd, --bd, --tx, --mu
|-- Accent:    --bl (blue), --gr (green), --am (amber), --rd (red)
|-- Layout:    #side (sidebar), #app (main content)
|-- Cards:     .card, .dv (device), .rc (room card)
|-- Controls:  .tg (toggle), .rng (range slider), .step (stepper)
|-- Utilities: .btn, .pill, .lv (live badge), .wb (status badge)
`

---

## File Structure

`
Smart Home Automation/
|-- Smart Home Control Dashboard.html   # Complete self-contained app (~2 MB)
|-- README.md                           # Project documentation
`

All assets (images, icons, fonts via CDN, styles, scripts) are embedded inline for maximum portability.

---

## Role-Based Access

| Role | Capabilities |
|---|---|
| **Admin** | Full access - control devices, change settings, manage automations |
| **Family** | View and control devices, receive alerts |
| **Guest** | View-only access |

Switch roles via **Admin & Settings** to test different permission levels.

---

## Device Power Ratings (Simulated)

| Device | Rated Power |
|---|---|
| Air Conditioner | 340 W |
| Ceiling Fan | 125 W |
| Water Heater | 800 W |
| Refrigerator | 90 W |
| Ceiling Light | 25 W |
| Smart TV | 80 W |
| CCTV Camera | 8 W |

---

## Extending the Project

### Add a New Room
`js
// In the JS state object S:
rooms: [..., 'New Room'],
// Also add to RIMG and RIC maps for image/icon
`

### Add a New Device
`js
D('Device Name', 'Room Name', 'type', { v: 50, rate: 100 })
`

### Add a New Automation Rule
`js
S.ru.push({ ic: 'icon', a: 'condition', b: 'value', ic2: 'icon2', c: 'action', d: 'value', on: 1 })
`

---

## Responsive Breakpoints

| Breakpoint | Layout |
|---|---|
| > 900px | Full 3-column grids |
| 720px - 900px | 2-column grids |
| < 720px | Single column + bottom navigation bar |

---

## Project Context

This dashboard was built as part of **AI Cohort 2 Project - Smart Home Automation**.

It demonstrates:
- Complex state management in pure JavaScript
- Reactive UI rendering without any framework
- Real-time simulation of IoT sensor data
- Energy analytics with SVG chart rendering
- Multi-user role-based access control
- Responsive single-page application design

---

## License

This project is intended for educational and demonstration purposes as part of AI Cohort 2.

---

*Built with pure HTML/CSS/JS - no frameworks, no build tools, no dependencies.*
