# Educational Fringe Explorer

An interactive, browser-based teaching tool for exploring optical etalon fringes, Airy transmission, free spectral range, finesse, fringe amplitude, and slow drift effects relevant to tunable diode laser absorption spectroscopy (TDLAS) baseline fringes. The app is a standalone HTML/CSS/JavaScript web app. It runs locally in any browser and does not require a build step, package installation, backend server, or external JavaScript libraries.

Web app link: https://goueguel.github.io/etalon-fringe-explorer/


## Features

- Interactive Airy transmission plot.
- Sliders for refractive index $n$, gap length $L$, internal angle $θ$, and surface reflectivity $R$.
- Real-time derived quantities:
  - free spectral range, FSR
  - finesse
  - peak FWHM
  - fringe amplitude
  - fringe order at the operating wavenumber
  - number of fringes in the displayed spectral window
  - transmission at fixed `ν₀`
- Presets for uncoated windows, AR-coated surfaces, high-finesse cavities, and oblique incidence.
- Time-trace drift simulation showing how a small refractive-index drift can produce slow detector-signal oscillations at a fixed laser wavenumber.

## Why this exists

Etalon fringes are often discussed through equations, but they are easier to understand visually. This explorer lets users see how each physical parameter changes the fringe pattern and how slow thermal or refractive-index drift can appear as a breathing baseline oscillation in a fixed-wavelength detector signal.

The core relationships used in the app are:

```text
Fringe maxima:      2 n L cos(theta) = m lambda
Phase:              phi = 4 pi n L cos(theta) / lambda
Airy transmission:  T(phi) = 1 / [1 + F sin^2(phi/2)]
Coefficient:        F = 4 R / (1 - R)^2
FSR:                1 / [2 n L cos(theta)]
```

In the app, the spectrum is plotted versus wavenumber `ν` in `cm^-1`, so the phase is evaluated as:

```text
phi = 4 pi n L cos(theta) nu
```

where `L` is converted to centimeters.

## Quick start

Clone the repository:

```bash
git clone https://github.com/<your-username>/educational-fringe-explorer.git
cd educational-fringe-explorer
```

Open the app directly:

```bash
open index.html
```

Or serve it locally:

```bash
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Repository structure

```text
educational-fringe-explorer/
├── index.html                  # Standalone web app
├── README.md                   # Project overview and instructions
├── LICENSE                     # MIT license
├── CHANGELOG.md                # Version history
├── CONTRIBUTING.md             # Contribution guidelines
├── .gitignore                  # Common local/dev files to ignore
├── .github/workflows/pages.yml # GitHub Pages deployment workflow
├── docs/theory.md              # Short physics notes
└── assets/.gitkeep             # Placeholder for future images/assets
```

## Suggested repository description

> Interactive educational web app for visualizing etalon fringes, Airy transmission, FSR, finesse, and TDLAS-style drift effects.

## Suggested topics

```text
optics spectroscopy etalon fabry-perot airy-function tdlAS laser-absorption spectroscopy-education javascript html5 canvas
```

## Version

Current app version: `v0.1.1`

## Roadmap ideas

- Add export-to-PNG for plots.
- Add an option to plot wavelength instead of wavenumber.
- Add detector averaging/noise simulation.
- Add a small glossary for students.
- Add a comparison mode for AR-coated versus uncoated surfaces.
- Add a wedge-angle / beam-overlap explanation panel.

## License

This project is released under the MIT License. See [`LICENSE`](LICENSE).
