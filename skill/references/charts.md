# Chart theming — Tableau Classic 10

Categorical palette (fixed order):
`#4E79A7, #F28E2B, #E15759, #76B7B2, #59A14F, #EDC949, #AF7AA1, #FF9DA7, #9C755F, #BAB0AC`

Conventions: white background, Gray 500 `#6B6B6B` axis/label text, Gray 300 `#D7DAE0` gridlines, heading font for titles in Acadia Blue. Single-highlight charts: highlight = Acadia Red `#C41424`, rest = Gray 300.

## matplotlib
```python
import matplotlib as mpl
from cycler import cycler

CLASSIC10 = ["#4E79A7","#F28E2B","#E15759","#76B7B2","#59A14F",
             "#EDC949","#AF7AA1","#FF9DA7","#9C755F","#BAB0AC"]

mpl.rcParams.update({
    "axes.prop_cycle": cycler(color=CLASSIC10),
    "figure.facecolor": "white",
    "axes.facecolor": "white",
    "axes.edgecolor": "#D7DAE0",
    "axes.titlecolor": "#004077",
    "axes.labelcolor": "#1A1A1A",
    "xtick.color": "#6B6B6B",
    "ytick.color": "#6B6B6B",
    "grid.color": "#D7DAE0",
    "font.family": "Arial",
    "axes.titlesize": 14,
})
```

## plotly
```python
import plotly.io as pio
import plotly.graph_objects as go

CLASSIC10 = ["#4E79A7","#F28E2B","#E15759","#76B7B2","#59A14F",
             "#EDC949","#AF7AA1","#FF9DA7","#9C755F","#BAB0AC"]

pio.templates["house"] = go.layout.Template(layout=dict(
    colorway=CLASSIC10,
    font=dict(family="Arial", color="#1A1A1A"),
    title=dict(font=dict(family="Montserrat, Arial", color="#004077")),
    paper_bgcolor="white", plot_bgcolor="white",
    xaxis=dict(gridcolor="#D7DAE0", linecolor="#D7DAE0"),
    yaxis=dict(gridcolor="#D7DAE0", linecolor="#D7DAE0"),
))
pio.templates.default = "house"
```

## Vega-Lite / Observable Plot
Set the categorical range to the Classic 10 array above (scheme → custom range).

## D3 / JS
```js
const classic10 = ["#4E79A7","#F28E2B","#E15759","#76B7B2","#59A14F",
                   "#EDC949","#AF7AA1","#FF9DA7","#9C755F","#BAB0AC"];
const color = d3.scaleOrdinal(classic10);
```
