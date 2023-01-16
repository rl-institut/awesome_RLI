# awesome_RLI
A curated list of python packages used in RLI projects.

The idea is to share best practices and knowledge of python packages across projects at RLI.


Package description should look like:
```
- [packagename](link-to-package) | short description
  - [projectname1](link-to-rli-project1) | Package-Maintainers | project insights on package integration/ comments
  - [projectname2](link-to-rli-project2) | Package-Maintainers | project insights on package integration/ comments
```

## Web development

### Django

- [django-tables](https://django-tables2.readthedocs.io/en/latest/) | Class-based customizable tables for django
  - [RMS](https://github.com/rl-institut-private/rms) | Hendrik Huyskens, Alexis Michaltsis | Custom rendered columns; custom css per cell/row/column; high inheritance

- [django-crispy-forms](https://github.com/django-crispy-forms/django-crispy-forms) | The best way to have Django DRY forms. Build programmatic reusable layouts out of components, having full control of the rendered HTML without writing HTML in templates
  - [RMS](https://github.com/rl-institut-private/rms) | Hendrik Huyskens, Alexis Michaltsis | Change form layout and styling depending on data using crispyforms
  - [Digiplan](https://github.com/rl-institut-private/digiplan) | Hendrik Huyskens | Change form template using crispyforms (this will be integrated out-of-the-box in [Django 4](https://smithdc1.github.io/my-blog/2022/forms/forms.html))

- [djangorestframework-mvt](https://github.com/corteva/djangorestframework-mvt) | A Django REST Framework extension for creating views that serialize model data to Map Box Vector Tiles via Postgres.
  - [Digiplan](https://github.com/rl-institut-private/digiplan) | Hendrik Huyskens | Extended version to allow multiple vector tiles per source

- [Template for RLI privacy statement and imprint](https://gist.github.com/Bachibouzouk/d80775e3adc2b5253903ee1e07166243) |  Privacy Statement of RLI for django .html templates (EN main language with DE translation), to save you the trouble to add all the translation tags and fill the .po file.

- [open_plan](https://github.com/open-plan-tool/gui/) | A GUI which allow user to build energy system with drag and drop and then request a simulation (currently only with [multi-vector-simulator](https://github.com/rl-institut/multi-vector-simulator)), and allow results vizualisation and scenarios comparisons.
  - [DualNumberField](https://github.com/open-plan-tool/gui/blob/ab707b7a5ee8e32d953d1e1bbcbe6bed47222e60/app/projects/helpers.py#L193) | @Bachibouzouk | Form to allow the user to write down a scalar OR upload a timeseries which then format them as json to be saved into the database. This form is implemented in open_plan with a js onchange function which plots the timeseries uploaded (if any), nevertheless this is not included by default in the field.
  - [Drag and drop energy system components](https://github.com/open-plan-tool/gui/blob/main/app/static/js/grid_model_topology.js) | @Bachibouzouk | **Not very well commented code yet** using [draflow js](https://github.com/jerosoler/Drawflow) to have draggable and clickable energy system components. The helper functions to interact with a django DB is made in a [separate file](https://github.com/open-plan-tool/gui/blob/main/app/projects/scenario_topology_helpers.py). An example of the implementation is done in the template of the [scenario creation step 2](https://github.com/open-plan-tool/gui/blob/main/app/templates/scenario/scenario_step2.html)

## Data Management

- [frictionless](https://github.com/frictionlessdata/frictionless-py) | Data management framework for Python that provides functionality to describe, extract, validate, and transform tabular data
  - [oedatamodel_api](https://github.com/open-modex/oedatamodel_api.git) | Hendrik Huyskens | Users can upload datapackages to OEP; datapackages are validated by frictionless

## Data visualization

- [plotly](https://plotly.com/python/) | Plotly Open Source Graphing Library for Python
  - [E-MetroBus](https://github.com/rl-institut/E_Metrobus) | Hendrik Huyskens, Bryan Lancien | Django-class for integrating plotly charts in templates; asynchronous requests for plotly charts delivered to frontend; visit [E-MetroBus Homepage](https://e-metrobus.berlin/)
  
- [dash](https://dash.plotly.com/)/plotly | Dash is the original low-code framework for rapidly building data apps in Python
  - [Open-MODEX Dashboard](https://github.com/open-modex/result_comparison) | Hendrik Huyskens | Interactive dashboard for applying different charts on data from OEP; Filter settings depending on/updating with data; user settings can be stored in DB: visit [MODEX Dashboard](https://modex-results.rl-institut.de/)

## Configuration

- [dynaconf](https://www.dynaconf.com/) | Configuration Management for Python
  - [oemof-B3](https://github.com/rl-institut/oemof-B3) | Hendrik Huyskens | Load configuration for snakemake and oemof-B3 via .yaml files
