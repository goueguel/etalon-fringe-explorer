# Etalon Fringe Explorer

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
  - transmission at fixed $\nu_₀$
- Presets for uncoated windows, AR-coated surfaces, high-finesse cavities, and oblique incidence.
- Time-trace drift simulation showing how a small refractive-index drift can produce slow detector-signal oscillations at a fixed laser wavenumber.

## Background

Etalon fringes are often discussed through equations, but they are easier to understand visually. This explorer lets users see how each physical parameter changes the fringe pattern and how slow thermal or refractive-index drift can appear as a breathing baseline oscillation in a fixed-wavelength detector signal.

The core relationships used in the app are:

Fringe maxima:      

$$ 2nL \textbf{cos}(\theta) = m\lambda $$

Fringe phase:              

$$ \phi = \frac{4\pi nL \textbf{cos}(\theta)}{\lambda} $$

Airy transmission function:  

$$ T(\phi) = \frac{1}{1 + F\textbf{sin}^{2}(\frac{\phi}{2})} $$

Finesse coefficient:        

$$ F = \frac{4R}{(1-R)^{2}} $$

Free spectral range:                

$$ FSR = \frac{1}{2nL \textbf{cos}(\theta)} $$


In the app, the spectrum is plotted versus wavenumber $\nu$ in $\text{cm}^{-1}$, so the phase is evaluated as: 

$$ \phi = 4\pi nL \textbf{cos}(\theta) \nu $$

where $L$ is converted to centimeters.