# HCS Presentation Template for Typst

A clean & modern (and cute :3) workshop slide deck template crafted for **HCS** seminar and lecture series, powered by [Touying](https://github.com/touying-typ/touying).

## ✨ Features

- **HCS Brand Palette**: Deep midnight navy (`#090043`), royal shield blue (`#2C5CB9`), electric cyan (`#00FFFF`), and slate periwinkle (`#ADBCD1`).
- **HUD & Mini-Navigation**: Breadcrumb trails, seminar status pills, and segmented Endfield-style footers with slide counters and dynamic progress bars.
- **Modern Multi-Role Typography**:
  - `heading`: `Century Gothic`
  - `body`: `Corbel`
  - `code`: `Cascadia Code`
  - `accent`: `Century Gothic`
  - Presets: `font-style: "cute"` (default), `font-style: "modern"` (Bahnschrift + Segoe UI), and `font-style: "tech"`.
- **Academic & Workshop Components**:
  - `#exercise-box`: Hands-on lab callouts with duration, difficulty, point values, and step items.
  - `#cblock`: Colored card boxes (`info`, `tip`, `warning`, `danger`, `cute`, `exercise`).
  - `#stat-card`: Large metric cards for seminar statistics.
  - `#quote-block`: Clean left-bordered quotation blocks.
  - `#split`: Responsive column split helper.
  - `#note`: Speaker notes integrated with `pdfpc`.
- **Custom Slide Types**:
  - `#title-slide`: Elegant cover slide with metadata badges and HCS logo.
  - `#outline-slide`: Automated agenda / roadmap.
  - `#section-slide`: Module dividers with large pill numbers and watermark dragon emblem.
  - `#focus-slide`: High-contrast midnight navy standout slide.
  - `#blank-slide`: Borderless canvas for fullscreen diagrams and live terminals.

## 🚀 Quickstart

Create a `slides.typ` file:

```typ
#import "@preview/hcs-presentation:0.1.0": *

#show: hcs-theme.with(
  aspect-ratio: "16-9",
  progress-bar: true,
  config-info(
    title: [Modern Systems & Binary Security],
    subtitle: [Hands-on Seminar & Workshop Series],
    author: [Your Name],
    institution: [HCS Research Lab],
    date: [Fall 2026],
  ),
)

#title-slide(tags: ([Security], [Workshop]))
#outline-slide()

= Module Name

== Slide Title

Slide content goes here!

#cblock(title: [Tip], type: "tip")[
  Always validate boundaries!
]
```

## 🔨 Compile

```bash
typst compile --root . template/slides.typ output.pdf
```
