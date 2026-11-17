# Urda 2026 railway collision reconstruction

A single-file, interactive educational visualization of the rear-end collision reported near Urda, Toledo, on 28 October 2026. Open [`index.html`](index.html) in a current desktop or mobile browser. No backend, build step, or frontend framework is used.

## Running it

- The HTML, CSS, UI, procedural train geometry, terrain, and controls are all contained in `index.html`.
- The full 3D scene loads Three.js 0.160.0 from jsDelivr (`cdn.jsdelivr.net`). The first load therefore needs an internet connection and a browser with WebGL enabled. No external 3D models, textures, or image assets are used.
- If the CDN is unavailable or WebGL cannot initialize, the page switches to an interactive 2D schematic fallback; timeline and playback controls remain usable. The fallback is not a 3D substitute.
- You can open the HTML directly with `file://`. For stricter browser setups, serve the directory locally, for example with `python -m http.server 8000`, then open `http://localhost:8000`.

## Controls

- **Play / Pause**, **Restart**, timeline scrubbing and 0.5×–4× playback speed.
- Camera presets: aerial drone, ground tracking, front-facing, side tracking, wide overview, and free look.
- In free look, drag to orbit, use the wheel or +/- buttons to zoom, and use **W/A/S/D** (or arrow keys) to navigate; **Q/E** move vertically.
- Use **Hide UI** in the top bar to clear the screen; click **Show controls**, press **H**, or press **Escape** to restore the interface. Fullscreen is separate and can be combined with the clean view.
- Toggle train labels, catenary/trackside infrastructure, and vegetation. **Space**, **R**, and **F** are playback, restart and fullscreen shortcuts.

The train models use smooth tapered cab shells, reflective paint, layered liveries, framed windows, door hardware, roof HVAC and pantographs, inter-car bellows, underbody equipment, profile-shaped wheels, and animated bogies/wheels. They are detailed procedural interpretations rather than photogrammetry or imported model files.

## Evidence and limits

The scene is based on the Spanish transport ministry / AITAT case file and its first-24-hour information note. Those sources identify the incident as a rear-end collision on Track 2 of line 010 at PK 118+800; the note identifies Iryo 6076 (Hitachi ETR1000 109.015) and Renfe AVE 2080 (Siemens 103.006 variant), and reports the Iryo train stopped at entry signal E242. The note also says the investigation was at an early stage and possible causes remained open.

This is **not** an official accident reconstruction. Train bodies and liveries are procedural visual interpretations, not photogrammetry. The landscape, route geometry, landmarks, spacing, animation timing, normalized movement, and simplified post-impact tableau are illustrative and not to scale. The simulation does not state a speed, assign a cause, or claim an exact wreckage footprint.

- [AITAT case file 146/2026](https://www.transportes.gob.es/organos-colegiados/ciaf/investigaciones-en-curso/expediente-1462026)
- [AITAT information note: information available after the first 24 hours](https://www.transportes.gob.es/recursos_mfom/paginabasica/recursos/note_urda_accident_-_available_information_after_first_24_hours.pdf)
