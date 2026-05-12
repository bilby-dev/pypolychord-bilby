# pypolychord-bilby

`pypolychord` plugin for `bilby`.

This plugin provides the `pypolychord` sampler in `bilby`.

## Installation

First, install `PolyChordLite` and `pypolychord` following the instructions in
the `PolyChordLite`
[documentation](https://github.com/PolyChord/PolyChordLite?tab=readme-ov-file#python-quickstart).

Once `pypolychord` is installed, install the plugin from PyPI:

```bash
pip install pypolychord-bilby
```

**Note:** due to licensing constraints `pypolychord-bilby` is not available via `conda-forge`.


## Usage

Once `pypolychord-bilby` is installed, the sampler can be used directly in
`bilby` via the `run_sampler` function:

```python
import bilby

likelihood = ...
priors = ...

bilby.run_sampler(
    sampler="pypolychord",
    likelihood=likelihood,
    priors=priors,
    nlive=1000,
    ...
)
```

### Usage with `bilby_pipe`

This plugin has not been tested with `bilby_pipe`.
