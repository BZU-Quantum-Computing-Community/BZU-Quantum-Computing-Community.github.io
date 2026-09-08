# BZU Quantum Computing Community — Website

Home of the **Quantum Series**, Birzeit University's edition of [Qiskit Fall Fest 2026](https://github.com/Qiskit-Fall-Fest-2026).

**Live site:** https://bzu-quantum-computing-community.github.io

## What this is

A single-page static site that introduces students to quantum computing and drives registration for the Quantum Series — five in-person sessions running October–November 2026, opening with the Quantum Open Day on Saturday 10 October.

The page includes an interactive 3D Bloch sphere so visitors can apply quantum gates to a real qubit simulation and watch it collapse when measured. It runs on plain canvas with no libraries.

## Structure

```
index.html          Entire site — HTML, CSS and JS in one file
assets/
  club-logo.png     BZU Quantum Computing Community logo
  birzeit-logo.webp Birzeit University logo
  fallfest-2026.svg Official Qiskit Fall Fest 2026 artwork (IBM)
  fallfest-badge.svg Official Fall Fest badge (IBM)
  og-image.png      1200x630 link-preview image for social sharing
```

## Editing

There is no build step. Edit `index.html`, commit, and push to `main` — GitHub Pages redeploys automatically within a minute.

### Registration link

Registration goes through a Google Form. Near the top of the `<script>` block in `index.html`:

```js
const REGISTRATION_FORM_URL = "";
```

Paste the form URL between the quotes and every "Register" button on the page points to it. While it is empty, the buttons show a "registration opens soon" message instead of a dead link.

### Local preview

Images need to be served over HTTP, so open the folder with a local server rather than double-clicking the file:

```bash
python3 -m http.server 5173
```

Then visit http://localhost:5173

## Credits

Fall Fest artwork and badge come from IBM's official
[materials-resources](https://github.com/Qiskit-Fall-Fest-2026/materials-resources) repository.
