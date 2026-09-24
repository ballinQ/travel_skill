# Implementation choices

## Data contract

Keep the renderer downstream of a portable trip-map model. Useful entities include:

- `view`: id, mode, bounds, camera, day, objective
- `place`: id, coordinates, category, planned state, priority, day links, verified URL
- `landmark`: place id, model or icon, narrative scale, context-only flag
- `route`: day, ordered geometry, mode, duration, distance, start time, confidence, fallback
- `district`: polygon or label point, itinerary relevance, display priority
- `gate`: condition, authority, decision time, affected entities, fallback

Do not put authoritative trip facts only inside drawing commands or DOM text.

## Rendering decision

### SVG/CSS

Best when offline reliability, single-file delivery, print, and editorial illustration matter more than precise pan and zoom. Keep operational pins and routes separate from any raster background.

### MapLibre GL JS

Use for verified geographic geometry, styled vector maps, terrain, camera transitions, and extensible custom layers. Create a deliberately sparse style and apply zoom-dependent label visibility. Preserve attribution and disclose online tile requirements.

### Mapbox GL JS

Use when Mapbox Standard, maintained landmark models, lighting, or available datasets justify a token and commercial dependency. Never embed a secret token. Explain quotas and offline limitations.

### Three.js

Use glTF models, simple extrusions, billboards, or low-poly terrain only where they improve recognition. Anchor objects to verified coordinates. Use instancing and level of detail for repeated objects. Dispose GPU resources when views change.

### deck.gl

Use `TripsLayer` for timestamped route playback and core layers for large geospatial datasets. Normalize timestamps to avoid floating-point precision loss. Avoid it for a handful of static route lines.

## Performance budgets

Set budgets appropriate to the artifact rather than pursuing maximum fidelity. Reasonable starting targets for a travel dashboard are:

- useful content visible before the advanced map finishes loading;
- stable interaction near 60 fps on a recent laptop and acceptably smooth on the target phone;
- no perpetual render loop when the scene is idle;
- limited simultaneous 3D landmark models and texture sizes;
- lazy-load daily detail and heavy assets;
- pause animation when hidden or reduced motion is requested;
- retain an HTML or SVG itinerary fallback if WebGL initialization fails.

Measure before adding visual complexity. Prefer fewer distinctive landmarks over many generic models.

## Offline and failure behavior

The trip timeline, addresses, reservation details, emergency information, and verified outbound links remain in HTML. If online tiles fail, retain a simplified cached or embedded overview when permitted, or show the itinerary with coordinates and navigation links. Make the limitation visible without covering the page with an error modal.

## Security and trust

Escape trip data before inserting it into HTML. Do not inject copied review or social-media content as markup. Never store booking credentials, payment data, private access tokens, or secrets in the artifact.
