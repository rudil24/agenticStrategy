# Diagram Scratchpad

Doodles of diagrams made with [mermaid](https://mermaid-js.github.io/mermaid/#/).

## Project structure

```mermaid
graph LR
    root[.] --> 1[README.md]
    root --> 2[docs]
    root --> 3[notebooks]
    subgraph 3g[All project notebooks.]
      3 --> 31[notebook-1.ipynb]
      3 --> 32[notebook-2.ipynb]
    end
    subgraph 2g[All project documents.]
      2 --> 21[doc-1.md]
      2 --> 22[doc-2.md]
    end
    subgraph 1g[The project overview.]
      1
    end
    click root "https://gitlab.com/joaommpalmeiro/diagram-scratchpad"
    click 1 "https://gitlab.com/joaommpalmeiro/diagram-scratchpad/blob/master/README.md"

linkStyle 0,1,2,3,4,5,6 stroke-width:1px;

style 1g fill:transparent,stroke:#E5E5E5,stroke-width:1px,stroke-dasharray:5;
style 2g fill:transparent,stroke:#323232,stroke-width:1px,stroke-dasharray:5;
style 3g fill:transparent,stroke:#323232,stroke-width:1px,stroke-dasharray:5;
```

The diagram below (except the helper text) was generated using the `tree -L 2` command.

<!-- prettier-ignore-start -->
<!-- Don't forget the two tabs! -->
    .
    ├── README.md             <- The project overview.
    ├── docs                  <- All project documents.
    │   ├── doc-1.md
    │   └── doc-2.md
    └── notebooks             <- All project notebooks.
        ├── notebook-1.ipynb
        └── notebook-2.ipynb
<!-- prettier-ignore-end -->
