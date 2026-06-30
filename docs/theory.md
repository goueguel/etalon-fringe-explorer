# Theory Notes

## Etalon condition

An etalon is formed when two partially reflecting surfaces create multiple beams that interfere. Constructive interference occurs when the round-trip optical path corresponds to an integer number of wavelengths:

```text
2 n L cos(theta) = m lambda
```

where:

- `n` is refractive index,
- `L` is the physical gap length,
- `theta` is the internal propagation angle,
- `m` is the fringe order,
- `lambda` is wavelength.

## Airy transmission

The ideal transmission of a lossless Fabry-Pérot etalon can be written as:

```text
T(phi) = 1 / [1 + F sin^2(phi/2)]
```

with:

```text
F = 4R / (1 - R)^2
phi = 4 pi n L cos(theta) / lambda
```

For a wavenumber-domain plot, using `nu = 1/lambda`, the phase becomes:

```text
phi = 4 pi n L cos(theta) nu
```

## Free spectral range

The free spectral range, FSR, is the spacing between adjacent transmission maxima. In wavenumber units:

```text
FSR = 1 / [2 n L cos(theta)]
```

A larger gap length or refractive index makes fringes denser. Oblique propagation changes the spacing through the `cos(theta)` term.

## Reflectivity and fringe contrast

Reflectivity controls fringe sharpness and contrast. Higher `R` produces narrower, deeper Airy features. Low-reflectivity surfaces, such as well-designed AR coatings, reduce the amplitude of parasitic fringes.

## Drift interpretation

At a fixed laser wavenumber, a small drift in refractive index or optical length changes the etalon phase. The detector signal can therefore oscillate slowly even when the laser is nominally fixed. This is one mechanism behind thermally induced baseline fringes in laser absorption instruments.
