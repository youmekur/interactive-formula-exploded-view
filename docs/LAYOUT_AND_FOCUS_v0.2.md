# IFEV v0.2.1 — Layout and semantic focus contract

## Reading order
- Define one semantic ID for each variable (not by character equality).
- Traverse the formula in semantic reading order; for repeated IDs, keep the first occurrence.
- Position callouts counterclockwise, beginning at the left edge and moving toward the bottom (screen coordinates).
- Formula DOM order is explicit in the examples. Fractions, matrices and multi-line expressions need a semantic AST traversal in a future release.

## Focus
- A semantic ID may map to any number of occurrences (`data-id`).
- Clicking any occurrence or the callout highlights every occurrence of that ID.
- Every occurrence has an independent SVG connector and synchronized light pulse.
- Switching focus cancels the previous animation.
- Identical glyphs with different meanings must use distinct semantic IDs.

## Limitations
- Current positioning is radial and clamped, without a general collision solver.
- Multiple independent lines may intersect; shared trunk routing remains future work.
- The six examples are static, not yet a packaged reusable component.
- Browser and iPad Safari visual verification remain outstanding.

## Coordinate convention
In screen coordinates, positive Y points **down**. From the leftmost position (angle π), **subtract** the angle increment to move first toward the bottom: `angle = Math.PI - 2 * Math.PI * i / N`. Adding the increment incorrectly produces a clockwise visual order.
