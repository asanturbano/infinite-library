# The Infinite Library

*Salle Ovale · Richelieu · Paris*

An immersive Three.js recreation of the Salle Ovale reading room at the Bibliothèque nationale de France. The visitor walks an endless loop around the inside perimeter of the great oval room, beside a continuous multi-level wall of ~20,000 procedurally generated books with seeded French titles.

## Running

Serve the folder over HTTP and open it in a browser (internet access is needed once, for the pinned Three.js CDN module):

```sh
python3 -m http.server 8123
# then open http://localhost:8123/
```

## Controls

- **↑ / W** — walk forward
- **↓ / S** — walk back
- **Mouse wheel / trackpad** — glide along the path
- **Mouse** — restrained look (right toward the books, left across the room, up toward the skylight)

Everything is a single self-contained `index.html`: deterministic seeded generation, one merged mesh for the near books, painted strips for the far galleries, and an arc-length-parameterized closed camera path so the loop has no seam.
