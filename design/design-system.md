# EduNexa AI Design System

## Colour tokens (light)
| Token | Value | Use |
|---|---|---|
| primary | `#5645D8` | buttons, links, active menu, progress |
| primary-soft | `#EDEAFF` | selected items, chips |
| navy | `#14183A` | hero, footer, headings |
| bg / surface | `#F5F6FB` / `#FFFFFF` | page / cards |
| text / muted | `#1A1E3C` / `#5B6385` | body / secondary text |
| success / warning / error | `#0E7C57` / `#9A5B00` / `#B7311F` | status |

## Colour tokens (dark)
bg `#0E1126`, surface `#171B38`, border `#2B3160`, text `#E9EBFB`, muted `#A2A9D2`, primary `#8E80FF`.

All text and background pairs meet WCAG AA (4.5 : 1 or higher).

## Typography
Inter (fallback Segoe UI, system sans-serif). Page title 22 px bold, section title 15 px bold, body 14 px, small 12 px.

## Spacing and shape
4 px grid; card padding 18 px; card gap 16 px; radius 10 px (inputs, buttons) and 14 px (cards).

## Responsive rule
Wider than 860 px: sidebar layout. 860 px or narrower: bottom tab bar and single-column cards.
The tokens are defined as CSS variables in `prototype/index.html` and map directly to the Tailwind theme.
