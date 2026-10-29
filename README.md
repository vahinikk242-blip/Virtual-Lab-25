# 🧪 Cheminformatics Virtual Laboratory (Website)

SRM Institute of Science and Technology, Tiruchirappalli · Division of Chemistry

A static, glassmorphism website version of the Cheminformatics Virtual Laboratory.
No build step, no backend, no installs: every page runs in the browser.

## Pages

| File | Purpose |
|---|---|
| `index.html` | Home, aim, example molecules, developer details |
| `theory.html` | Cheminformatics, SMILES, descriptors, 3D models |
| `visualization.html` | SMILES input, 2D structure, rotatable 3D structure (4 styles) |
| `properties.html` | Descriptor table, interpretation, CSV download |
| `analysis.html` | Multi-molecule comparison table, chart, CSV download |
| `assessment.html` | 12-question quiz with scoring |
| `report.html` | Printable student report (Print → Save as PDF) |

## Structure

```
index.html … report.html
assets/css/style.css     shared glassmorphism theme
assets/js/chem.js        SMILES parser, 2D/3D layout, descriptors, renderers
assets/js/site.js        navigation, footer, saved molecule/student details
assets/img/srm_logo.jpeg
vercel.json
```

## Deploy

**Vercel:** drag the unzipped folder into vercel.com/new, or run `vercel --prod` inside it.
**Anywhere else:** upload the folder to any static host (GitHub Pages, Netlify, college server).
**Local preview:** open `index.html` in a browser.

## Accuracy note

Molecular weight, ring count, HBD, HBA, rotatable bonds and TPSA are computed in the browser from the
SMILES graph. LogP is a simplified fragment estimate, except for the six course examples, which use
reference values. 2D/3D coordinates come from a simple force-directed layout, so geometry is
illustrative rather than energy-minimised. For exact RDKit results, use the original Streamlit app.
