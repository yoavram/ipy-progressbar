# Note

This repo was imported from [Alexander Plavin's repo](https://hg.plav.in/my_projects/python/ipy-progressbar), which, according to [PyPI](https://pypi.python.org/pypi/ipy-progressbar/1.0.2) is under the MIT License.

Introduction
============

ipy-progressbar allows to use the same code for rich progressbars in IPython Notebooks, and for simple fallback ones in terminal sessions.


Example
=======

Code like this:

```python
from ipy_progressbar import ProgressBar

pb = ProgressBar(10, title='Outer', key='outer')
for i in pb:
    pb_inner = ProgressBar(5, title='Inner', key='inner')
    for j in pb_inner:
        # inner loop body
```

will work both in IPython Notebook and in plain console. When run in notebook, the output will be rich (Bootstrap progress bars), while console version is mainly thought of as a fallback.
