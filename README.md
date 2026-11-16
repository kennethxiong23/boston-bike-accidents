# Boston Bike Accidents

A data-analysis project exploring bicycle-related accidents in Boston in relation to the city's bike-lane network. The repository combines prepared JSON and GeoJSON datasets with Python analysis modules and a Jupyter notebook for spatial and categorical exploration.

## What the project does

- Loads Boston street, boundary, bike-lane, and accident data.
- Associates accident locations with nearby road or bike-lane context.
- Produces visualizations of accidents by lane and geographic area.
- Supports exploratory analysis in `comp_essay.ipynb`.

## Repository layout

- `comp_essay.ipynb` - primary notebook for the analysis and written exploration.
- `accidents_by_lane.py` - creates accident-by-lane plots.
- `heatmap.py` - generates geographic heatmap visualizations.
- `helpers.py` - shared data-loading and transformation helpers.
- `data/` - JSON and GeoJSON source data used by the analysis.
- `test_helpers.py` - tests for helper functions.
- `pyproject.toml`, `requirements.txt` - project and dependency configuration.

## Requirements

Python 3.8+ is recommended. Install the project dependencies with:

```sh
pip install -r requirements.txt
```

For notebook work, also install or enable Jupyter:

```sh
jupyter notebook
```

## Run the analysis

Open the notebook and run its cells from top to bottom:

```sh
jupyter notebook comp_essay.ipynb
```

The standalone plotting modules can also be imported or run directly as needed:

```sh
python accidents_by_lane.py
python heatmap.py
```

The scripts expect the files in `data/` to remain at their repository-relative paths.

## Test

Run the helper tests with:

```sh
pytest
```

## Data notes

The repository includes derived datasets and public geographic data in JSON and GeoJSON formats. Results should be interpreted as an exploratory analysis rather than proof that a bike lane caused or prevented an accident; lane coverage, reporting, road geometry, and other confounding factors affect the comparison.