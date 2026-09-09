# Module 4 — Data Visualization

## Skill covered

| Skill | Role |
|-------|------|
| `dataviz` | The design system for **any** chart, graph, plot, or dashboard — in any medium |

## Why this is its own skill

Charts are easy to make and easy to make badly. `dataviz` is a set of rules Claude reads
*before writing the first line of chart code*: how to pick the right chart form, a color
formula (with a validator) that stays accessible in light and dark, mark specs, and
interaction rules. The result is that a dashboard reads as one coherent system instead of
a pile of mismatched charts.

## When it triggers

Basically any time a visualization is involved, in **any** output:

- an HTML or React artifact with charts
- inline SVG
- plotting code (matplotlib, plotly, d3, Recharts, …)
- a rendered PNG chart
- a KPI row, stat tile, sparkline, heatmap, legend, or axis

Trigger words: *chart, graph, plot, dashboard, visualization, analytics, "visualize
this", "color by series", "categorical/sequential/diverging palette."*

## The one rule worth knowing

**When the chart is going into a live document tool that renders charts itself, give it the
data, not a picture of a chart.** A PNG of a chart loses hover, inspection, and comments.
`dataviz` teaches Claude to hand over rows (or a data file the chart cites) in that case.

## Worked examples

**A dashboard:**
> **You:** build a sales dashboard from this data — revenue by month, top products, and a KPI row

Claude loads `dataviz` first, chooses forms, applies a validated palette, then builds.

**A single chart in code:**
> **You:** write matplotlib code to plot this time series with a clean, accessible style

Even though it's "just code," `dataviz` fires because a chart is being created.

**Recoloring:**
> **You:** these 6 series are hard to tell apart — give me a proper categorical palette

`dataviz` provides a palette that's distinguishable and theme-safe.

## Try it

1. Paste ~10 rows of made-up numbers and ask for "a dashboard."
2. Then ask: "make the same chart as matplotlib code" — notice the same design thinking
   carries over.
3. Ask Claude to "validate the palette for color-blind accessibility" and see what it
   checks.

Next: [Module 5 — Memory](05-memory.md)
