IGRA2 Weather Stations Map
Interactive map of global radiosonde stations from NOAA's Integrated Global Radiosonde Archive (IGRA).
🚀 Quick Start
Option 1: GitHub Pages (Recommended)
Fork or create a new repository on GitHub
Upload both files to the repository:
igra2_stations_map.html (rename to index.html for cleaner URL)
igra2-station-list.txt (your data file)
Enable GitHub Pages:
Go to Settings → Pages
Source: Deploy from a branch
Branch: main / root
Save
Access your map at https://your-username.github.io/your-repo-name/
The map will automatically load the data from igra2-station-list.txt!
Option 2: Local Server
bash
Copy
# Navigate to the folder containing the files
cd /path/to/your/files

# Start a local server
python -m http.server 8000

# Open in browser
http://localhost:8000/igra2_stations_map.html
Option 3: VS Code Live Server
Install the "Live Server" extension in VS Code
Right-click on igra2_stations_map.html
Select "Open with Live Server"
📁 File Structure
plain
Copy
your-repo/
├── index.html (or igra2_stations_map.html)
├── igra2-station-list.txt
└── README.md
🗺️ Features
Interactive Map: Zoom, pan, click markers for details
Filters:
Search by station name, ID, or country
Filter by year range
Filter by altitude
Filter by country
Color Coding: Stations colored by altitude
🟢 Green: 0-100m
🟡 Yellow: 100-500m
🟠 Orange: 500-1000m
🔴 Red: 1000-2000m
🔴 Dark Red: >2000m
Data Display:
Total stations count
Filtered stations count
Time period coverage
📊 Data Format
The igra2-station-list.txt file should contain lines in this format:
plain
Copy
ID         LAT      LON      ALT    NAME                           START END   COUNT
ACM00078861  17.1170  -61.7830   10.0    COOLIDGE FIELD (UA)            1947 1993  13896
🔧 Troubleshooting
"Using sample data" message
Make sure igra2-station-list.txt is in the same folder as the HTML
Check that the filename matches exactly (case-sensitive)
On GitHub Pages, wait 1-2 minutes after uploading for the file to be available
Map doesn't load
Check browser console (F12) for errors
Ensure you have internet access (for Leaflet maps)
Try refreshing the page
CORS errors locally
Use a local server (Option 2 or 3) instead of opening the file directly
Or upload to GitHub Pages
📄 Data Source
NOAA National Centers for Environmental Information (NCEI) - IGRA
📝 License
This project is open source. The IGRA data is provided by NOAA.
