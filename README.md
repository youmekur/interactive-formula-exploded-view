# IFEV — Interactive Formula Exploded View

A dependency-free, interactive formula annotation prototype for STEM education.

**Current design revision: v0.2.1** · **Status: prototype, not a packaged reusable library.**

## Interaction contract
- Preserve the centered mathematical formula.
- Place semantic callouts in first-occurrence reading order, counterclockwise around the formula (left → bottom → right → top).
- Clicking a symbol highlights **all occurrences** sharing its semantic ID.
- Each occurrence sends a synchronized light pulse along its connector to the shared callout.
- Different meanings must never be merged merely because their glyphs match.

See [layout and focus specification](docs/LAYOUT_AND_FOCUS_v0.2.md).

## Example set (prepared, upload pending)
1. Physics — Ohm's law
2. Mechanics — Newton's second law
3. Electronics — RC time constant
4. Materials — thermal expansion
5. Fluid mechanics — Reynolds number
6. Electrical engineering — RLC impedance

**The six interactive HTML files are not yet committed to this repository.** Do not treat the examples as hosted demos until the `examples/` directory is published.

## Limitations
Current layouts use radial positioning without general collision avoidance. Multi-line formulas and complex math AST traversal are future work. Browser/iPad Safari visual regression has not yet been completed.

## License
[MIT](LICENSE). The examples are educational visualizations, not certified engineering calculators.
