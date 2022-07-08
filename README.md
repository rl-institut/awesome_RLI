# awesome_RLI
A curated list of python packages used in RLI projects.

The idea is to share best practices and knowledge of python packages across projects at RLI.


Package description should look like:
```
- [packagename](link-to-package) | short description
  - [projectname1](link-to-rli-project1) | Maintainers | project insights on package integration/ comments
  - [projectname2](link-to-rli-project2) | Maintainers | project insights on package integration/ comments
```

## Web development

### Django

- [django-tables](https://django-tables2.readthedocs.io/en/latest/) | Class-based customizable tables for django
  - [RMS](https://github.com/rl-institut-private/rms) | Hendrik Huyskens, Alexis Michaltsis | Custom rendered columns; custom css per cell/row/column; high inheritance

## Data Management

- [frictionless](https://github.com/frictionlessdata/frictionless-py) | Data management framework for Python that provides functionality to describe, extract, validate, and transform tabular data
  - [oedatamodel_api](https://github.com/open-modex/oedatamodel_api.git) | Hendrik Huyskens | Users can upload datapackages to OEP; datapackages are validated by frictionless

## Data visualization

- [plotly](https://plotly.com/python/) | Plotly Open Source Graphing Library for Python
  - [E-MetroBus](https://github.com/rl-institut/E_Metrobus) | Hendrik Huyskens, Bryan Lancien | Django-class for integrating plotly charts in templates; asynchronous requests for plotly charts delivered to frontend; visit [E-MetroBus Homepage](https://e-metrobus.berlin/)
  
- [dash](https://dash.plotly.com/)/plotly | Dash is the original low-code framework for rapidly building data apps in Python
  - [Open-MODEX Dashboard](https://github.com/open-modex/result_comparison) | Hendrik Huyskens | Interactive dashboard for applying different charts on data from OEP; Filter settings depending on/updating with data; user settings can be stored in DB: visit [MODEX Dashboard](https://modex-results.rl-institut.de/)