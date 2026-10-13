# Metro’s Sports Hub

A responsive dark-mode sports hub prototype for iPhone and desktop. The interface requests live scoreboard data, standings, and player leader categories from public ESPN endpoints where available.

## Features
- Scores for NBA, NHL, NFL, MLB, and English Premier League
- Date selection and manual refresh; scoreboard refreshes about once per minute while the page is open
- League standings and player leader pages
- Navigation between Scores, Leagues, Players, Fantasy Lab, and Watch, including URL hash routes and browser back/forward
- iPhone-friendly responsive layout and PWA shell for Add to Home Screen when hosted over HTTPS
- Graceful loading/error states; no invented live scores or fantasy projections

## Important data note
This prototype uses public, undocumented ESPN site API endpoints. They may change, throttle, block browser requests, or have inconsistent coverage. This is not a guaranteed or licensed commercial data feed. Before a public commercial launch, review provider terms and arrange an appropriate sports-data license. Fantasy projections are intentionally shown as unavailable until a real projection provider is connected.

## Run locally
Because browsers restrict service workers and some fetch behavior on `file://`, serve the folder through a local HTTP server, for example:

```bash
python3 -m http.server 8080
```

Then open `http://localhost:8080`.

## Publish as an iPhone home-screen web app
1. Create a GitHub repository and upload the contents of this folder.
2. In the repository settings, enable GitHub Pages for the main branch/root folder (or deploy the folder to another HTTPS static host).
3. Open the published HTTPS URL in Safari on your iPhone.
4. Tap Share → Add to Home Screen.

A true App Store listing is a separate native-app submission and requires an Apple Developer account, signing, and App Review. This package is a web app/PWA foundation, not an already-published App Store app.
