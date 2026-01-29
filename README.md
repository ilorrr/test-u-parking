# U‑Parking Console (NeuroFit-style Vanilla JS SPA)

This is a quick re-skin + route swap of your NeuroFit SPA shell into a U‑Parking “inner web interface” dashboard.

## Run locally
Just open `index.html` in a browser (or use a simple static server).

### Option (recommended): Python static server
```bash
cd u-parking-web
python -m http.server 5173
```
Then open http://127.0.0.1:5173

## Hook up to Django
In `app.js`, replace the demo code blocks with real calls:
- `POST /api/auth/login`
- `POST /api/auth/register`
- `GET /api/lot/summary`
- `GET /api/lot/spots`
- `GET/POST/DELETE /api/reservations`
- `GET /api/rover/status`
- `GET /api/alerts`

Update API base in Settings page or change `DEFAULT_API_BASE`.

## Notes
- Current build uses *demo mode* auth (`demo-token`) so you can click around without a backend.
- “Lot View” lets you click a spot to cycle `free → occupied → reserved → free` (demo).
