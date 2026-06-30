# Contributing

Contributions are welcome, especially improvements that make the physics clearer for students and instrument users.

## Good contribution areas

- Clarifying labels, units, and explanatory text.
- Adding simple educational examples.
- Improving accessibility and mobile layout.
- Adding plot-export features.
- Adding optional noise, averaging, detector response, or wavelength-domain views.

## Development notes

This app is intentionally dependency-free. Keep changes simple and easy to run from a local browser whenever possible.

To test locally:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.

## Pull request checklist

Before opening a pull request, please check that:

1. The app opens without console errors.
2. Sliders and presets update the plots correctly.
3. The drift simulation starts, pauses, and clears as expected.
4. Any new equations include units and plain-language explanation.
