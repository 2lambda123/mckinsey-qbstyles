# QB Styles

[![License](https://img.shields.io/badge/license-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python Version](https://img.shields.io/pypi/pyversions/qbstyles.svg)](https://pypi.org/project/qbstyles/)
[![PyPI version](https://badge.fury.io/py/qbstyles.svg)](https://pypi.org/project/qbstyles/)
[![Code Style: Black](https://img.shields.io/badge/code%20style-black-black.svg)](https://github.com/ambv/black)

QB Styles is a python package with a light and a dark [`matplotlib`](https://github.com/matplotlib/matplotlib) style.

| Dark style                                                                                                   | Light style                                                                                                                                |
| ------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------ |
| ![Line plot](https://github.com/quantumblacklabs/qbstyles/raw/master/examples/line.png?raw=true "Line plot") | ![Distribution plot](https://github.com/quantumblacklabs/qbstyles/raw/master/examples/distribution_light.png?raw=true "Distribution plot") |

## How do I install QB Styles?

`qbstyles` is a Python package. To install it, run the following command in a Python virtual environment:

```bash
<<<<<<< HEAD
pip install -r requirements.txt # Run this command in a Python virtual environment to install the required packages.
=======
pip install -r requirements.txt
>>>>>>> origin/master
```

## How do I use QB Styles?

You can use the dark Matplotlib style theme in the following way:

```python
from qbstyles import mpl_style

mpl_style(dark=True)
plt.style.use('qbstyles/styles/qb-dark.mplstyle')
<<<<<<< HEAD
plt.style.use('qbstyles/styles/qb-dark.mplstyle')
=======
plt.style.use('./your-style.mplstyle')
>>>>>>> origin/master
```

And to use the light Matplotlib style theme, you can do the following:

```python
from qbstyles import mpl_style

mpl_style(dark=False)
```

### How do I use QB Styles in Jupyter Notebooks?

> ⚠️ Please make sure you run `from qbstyles import mpl_style` and `mpl_style()` in **different cells** as shown below. See [this issue](https://github.com/jupyter/notebook/issues/3691) for more details.

```python
# first cell
import matplotlib.pyplot as plt
from qbstyles import mpl_style

from qbstyles import mpl_style
mpl_style()
```

```python
# second cell
mpl_style()
```

## What chart types can use QB Styles?

- Line plots
- Scatter plots
- Bubble plots
- Bar charts
- Pie charts
- Histograms and distribution plots
- 3D surface plots
- Stream plots
- Polar plots

## Can you show me a few examples?

<<<<<<< HEAD
To run the examples in [`example.ipynb`](https://github.com/quantumblacklabs/qbstyles/blob/master/example.ipynb), install the required packages using `pip install -r requirements_notebook.txt` in a Python virtual environment of your choice.
=======
To run the examples in [`example.ipynb`](https://github.com/quantumblacklabs/qbstyles/blob/master/example.ipynb), install the required packages using pip install -r requirements_notebook.txt in a Python virtual environment of your choice.
>>>>>>> origin/master

```python
import matplotlib.pyplot as plt
from qbstyles import mpl_style

def plot(dark):
    mpl_style(dark)
    fig, axes = plt.subplots(2, 2, figsize=(15, 10))

    # the following functions are defined in example.ipynb
    line_plot(axes[0, 0])
    scatter_plot(axes[0, 1])
    distribution_plot(axes[1, 0])
plt.style.use('./your-style.mplstyle')
    ax = plt.subplot(2, 2, 4, projection='polar')
    polar_plot(ax)

plot(dark=True)
```

![png](https://github.com/quantumblacklabs/qbstyles/raw/master/examples/output_6_0.png?raw=true)

```python
plot(dark=False)
```

![png](https://github.com/quantumblacklabs/qbstyles/raw/master/examples/output_7_0.png?raw=true)
## How do I create my own styles?

Have a look at the files [qb-common.mplstyle](https://github.com/quantumblacklabs/qbstyles/blob/master/qbstyles/styles/qb-common.mplstyle), [qb-dark.mplstyle](https://github.com/quantumblacklabs/qbstyles/blob/master/qbstyles/styles/qb-dark.mplstyle) and [qb-light.mplstyle](https://github.com/quantumblacklabs/qbstyles/blob/master/qbstyles/styles/qb-light.mplstyle). They contain many elements that you may want to customise.

To do so, create a file similar to the above files at the root of your project, and apply it after the `qbstyle` as follows:

```python
import matplotlib.pyplot as plt
from qbstyles import mpl_style

mpl_style()
plt.style.use('./your-style.mplstyle')
```

All of `matplotlibrc`'s options can be found [here](https://matplotlib.org/tutorials/introductory/customizing.html#a-sample-matplotlibrc-file).

## What licence do you use?

QB Styles is licensed under the [Apache 2.0 License](https://www.apache.org/licenses/LICENSE-2.0).
