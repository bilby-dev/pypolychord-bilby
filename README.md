# pypolychord-bilby

`pypolychord` plugin for `bilby`.

This plugin provides the `pypolychord` sampler in `bilby`.

## Installation

**Note:** since `polychord` cannot be installed via `pip` or `conda`, this
plugin can only be installed from source.

First, install `polychord` following the instructions in the `polychord`
[documentation](https://github.com/PolyChord/PolyChordLite?tab=readme-ov-file#python-quickstart).

Once `polychord` is installed, the plugin can be installed from the source
code. This can either be done directly using pip:

```bash
pip install git+https://github.com/bilby-dev/pypolychord-bilby.git
```

or by first cloning the git repository and then installing the package:

```bash
git clone git@github.com:bilby-dev/pypolychord-bilby.git
cd pypolychord-bilby
pip install .
```

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
