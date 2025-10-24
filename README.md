# Weather-Dashboard-
step 1:Start the Program
step 2:Save the file
      • Open a text editor (VS Code, Notepad, Sublime, etc.).
      • Paste the whole HTML you posted into a new file.
      • Save it as index.html in a folder you choose.
      
Step 3:Add your OpenWeatherMap API key
      • Create a free account at OpenWeatherMap and get an API key.
      • In your index.html, find the <script> area and add this near the top (before any function that uses apiKey):

const apiKey = "YOUR_OPENWEATHERMAP_API_KEY";

Replace YOUR_OPENWEATHERMAP_API_KEY with the key you got.

Step 4: Serve the file (recommended) — why and how
Why: navigator.geolocation often only works on pages loaded over HTTPS or http://localhost. So open the file via a simple local server to avoid location issues.

  • VS Code + Live Server
  • Install the Live Server extension, right-click index.html → Open with Live Server.

Python (terminal / command prompt)

In the folder with index.html run:

python -m http.server 8000

Open http://localhost:8000 in your browser.
Node (http-server)

Install and run:

npx http-server -p 8000
Open http://localhost:8000.

You can also open index.html directly by double-clicking it, but geolocation may be blocked in some browsers that require a secure context.

Step 5: Open the page in your browser

1. Go to http://localhost:8000 (or the Live Server URL).
2. Allow location access when the browser asks (so getLocationWeather() can work).
3. Use the search box or saved history buttons to request weather for cities.

5) Debugging & checks

   • Open DevTools Console (F12) to see fetch errors or messages.
   • If air quality shows “unavailable”, check your API key and the air_pollution endpoint.
   • If location is blocked, make sure you served the page over localhost or HTTPS and that you allowed location in the browser settings.
   • Check network tab to see the requests to api.openweathermap.org and any HTTP status codes.

Step 6: Optional improvements (quick ideas)

   • Hide your API key (server proxy) if you publish the site — putting the key directly in a client file can expose it.
   • Add nicer CSS or icons for weather conditions.
   • Add error messages for invalid city names.
Step 7: Close the Program

TECHNOLOGY USED
HTML — page structure.
CSS — styling (inline/embedded in your file).
JavaScript (vanilla) — DOM manipulation, app logic.
Fetch API — to call OpenWeatherMap endpoints.
OpenWeatherMap API — weather, forecast, and air pollution data.
Navigator Geolocation API — get user's location.
localStorage — save and display search history.
Browser (DevTools) — for debugging.
