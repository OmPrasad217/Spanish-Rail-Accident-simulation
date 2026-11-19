# Urda railway incident reconstruction

A standalone, source-led HTML visualization of the reported rear-end collision near Urda, Toledo, on 28 October 2026. The scene is rebuilt as a cinematic, high-detail procedural 3D environment with interactive timeline, camera modes, train identification, reported signalling context, and an immersive clean-view mode.

## Open the simulation

Open [`index.html`](index.html) in a current browser. It uses no frontend framework, backend, database, or build step.

- Three.js 0.160.0 is loaded from jsDelivr for the full 3D view, so the first 3D load requires internet access and WebGL.
- Terrain, sky, paint, ballast, vegetation, train meshes, and scene details are procedurally generated; no external model or texture files are required.
- If Three.js or WebGL is unavailable, an interactive 2D schematic fallback still supports the timeline and train-name toggle. This fallback is not a 3D substitute.
- If a browser restricts opening local files, serve the folder locally, e.g. `python -m http.server 8000`, then open `http://localhost:8000`.

## Controls

- Play / pause, restart, timeline scrubbing, and 0.5×–4× playback speed.
- Camera modes: wide overview, aerial drone, ground tracking, front-facing, side tracking, a dedicated **LZB trackside** schematic view, and free look. In free look, drag to orbit, use the wheel or +/- buttons to zoom, and use W/A/S/D (or arrow keys) to move; Q/E move vertically.
- **Train names** toggles the in-scene Iryo and Renfe identity labels. Infrastructure and environmental detail also have separate toggles.
- **Hide interface** clears the panels and controls; **Show controls**, H, or Escape restores them. Fullscreen is independent.
- Keyboard shortcuts: Space (play/pause), R (restart), F (fullscreen), H/Escape (restore the interface from clean view).

## Train visuals and evidence

The train sets are high-detail procedural interpretations: shaped aerodynamic cab shells, reflective painted finishes, livery graphics, framed glazing, doors and fittings, roof HVAC and pantographs, gangways, underbody equipment, detailed bogies, profile-shaped wheels, and rolling wheel animation. The Iryo and Renfe cab silhouettes and swept windscreens are distinct, and the noses are informed by the supplied front-view references. They are not photogrammetry, manufacturer CAD, or exact vehicle models.

The AITAT first-24-hour note identifies Iryo 6076 (Hitachi ETR1000 109.015) and Renfe AVE 2080 (Siemens 103.006 variant), both eight-car sets, and reports the Iryo train stopped at entry signal E242 when the Renfe train struck it from behind. It also reports an LZB system failure beginning at 08:31 and degraded operation under the BSL lineside system. This is presented only as reported context: the note says the investigation was at an early stage and possible causes remained open. The simulation does not assign cause, claim a direct causal chain, or assert speed, exact approach timing, or physical scale.

The dedicated camera mode is LZB (Linienzugbeeinflussung) and frames a conceptual track-conductor route and generic lineside control cabinets; the 2D fallback provides a schematic close-up too. Their appearance and placement are illustrative, not evidence of the exact equipment or installation at Urda. The landscape, route landmarks, spacing, movement, signal appearance, and simplified post-impact tableau are likewise illustrative, not a surveyed site or exact damage map.

- [AITAT case file 146/2026](https://www.transportes.gob.es/organos-colegiados/ciaf/investigaciones-en-curso/expediente-1462026)
- [AITAT information note: available after the first 24 hours](https://www.transportes.gob.es/recursos_mfom/paginabasica/recursos/note_urda_accident_-_available_information_after_first_24_hours.pdf)
