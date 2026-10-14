# CholombeCAD

**Don't expect much. It's the alpha version of a Friday afternoon project.**

That said — it's already perfectly functional as a full, ordinary CAD. Don't take my word for it. Just click the file, it'll open in a new tab, and see for yourself.

---

## What is this?

A complete 2D CAD application running in a **single HTML file**. No install, no build step, no dependencies to download, no license server phoning home. Double-click `CholombeCAD.html` and you're drafting.

It runs in any browser. Your laptop, your school computer, your Xbox, your phone. If it can render a `<canvas>`, it can run CholombeCAD.

---

## What's in it

A lot, honestly, for something I threw together on a Friday:

- **Draw** — Lines, polylines, splines, xlines, rays, circles (center-radius, 2-point, 3-point), arcs, rectangles, polygons, ellipses, donuts, points, revclouds, wipeouts
- **Modify** — Move, copy, rotate, scale, mirror, stretch, array, offset, fillet, chamfer, trim, extend, break, join, explode, align, lengthen
- **Annotation** — Text, mtext, multileaders, dimensions (linear, aligned, angular, radius, diameter, ordinate, continue, baseline) with associative updating
- **Regions & Booleans** — Union, subtract, intersect with real polygon clipping
- **Blocks & References** — Define, insert, edit, explode, WBlock, XREF attach
- **Hatching** — 24+ patterns with live swatch preview
- **Layers** — Full properties manager with on/off/freeze/lock, filters, layer states
- **Layouts & Plotting** — Paper space, viewports, PDF export via jsPDF, browser print
- **DXF Import/Export** — Real DXF round-tripping, plus experimental DWG via WASM
- **Full command line** — With autocomplete, aliases, and AutoCAD-compatible command names
- **Undo/redo, clipboard, groups, quick select, purge, audit, mass properties, layer states**

That's not a plan. **It's all in there.**

---

## How to run it

1. Click `CholombeCAD.html`
2. It opens in a new tab
3. Draft

That's the whole procedure. No `npm install`, no `pip`, no *"please ensure you have Python 3.11 or higher."*

---

## Command line

Type `HELP` in the command line for the full list. If you've ever used AutoCAD, the aliases will feel familiar — `L` for line, `C` for circle, `TR` for trim, `EX` for extend, and so on.

---

## Things it doesn't do

To be fair about it:

- **No 3D.** It's 2D only, and that's not changing.
- **DWG import** relies on a WASM library that may or may not load depending on the day. Convert to DXF if it gives you trouble (there's a modal that walks you through it).
- Some **edge cases** in associative dimensions and complex boolean operations will probably surprise you.
- **It's an alpha.** Bugs exist. I find them, I fix them, more appear. That's how it goes.

---

## Known issues

- It's **Friday-afternoon code** in places. Some functions are long. Some naming is inconsistent. I know.
- **Mobile works** but the UI is built for a mouse.
- **Extremely large drawings** (thousands of entities) will make the canvas cry. There's no spatial index yet. (Now there is!)

---

## Contributing

If you're a real developer and you're reading the source thinking *"this kid has no idea what he's doing"* — you're kinda right, and you're welcome to help. Open a PR, file an issue, or just point out what's broken.

If you're another 16yo who wants to build something: **do it.** This whole thing started because I was annoyed that an AutoCAD license subscription asks you to sell your kidney.

---

## License

**MIT.** Do whatever you want with it. Just don't sue me AutoDesk, I'm a literal kid.

---

**CholombeCAD** — *REAL software doesn't require selling both your kidneys.*

---

### Very Special thanks to

- **Mr. DeepSeek** — for the help.
- The **ArtCraft** repo — which motivated me to clone a big money-cow software similar to the real one and open-source it. They are already doing much greater than me.
