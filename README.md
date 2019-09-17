# pySIIB: A python implementation of Speech intelligibility in bits (SIIB)

This Python implementation of SIIB is ported from the author's matlab codes: https://stevenvankuyk.com/matlab_code/

## Install

```bash
python setup.py install
```


## Usage

```python
from pysiib import SIIB
fs = 16000
# SIIB with MI function in C-implementation (this is used in [1],[2])
SIIB(x, y, fs)
# SIIB with MI function in python implementation
SIIB(x, y, fs, use_MI_Kraskov=False)
# SIIB^gauss
SIIB(x, y, fs, gauss=True)
```

The first version is proposed in [1] and  SIIB^Gauss is more simple implmentation and faster.
The speed comparison is SIIB^gauss > C-SIIB > python-SIIB.

## Reference

- [1] S. Van Kuyk, W. B. Kleijn, and R. C. Hendriks, ‘An instrumental intelligibility metric based on information theory’, IEEE Signal Processing Letters, 2018.
- [2] S. Van Kuyk, W. B. Kleijn, and R. C. Hendriks, ‘An evaluation of intrusive instrumental intelligibility metrics’, IEEE/ACM Transactions on Audio, Speech, and Language Processing, 2018.