# Class 14

**Matplotlib** is a Python package used for 2d graphics.

**IPython** is an enhanced interactive Python shell that allows interactive matplotlib sessions that have Matlab/Mathematica-like functionality.

**Pyplot** provides a convenient interface to the matplotlib object-oriented plotting library

A simple plot can be made by entering coordinates and endpoints.

```python
import numpy as np
import matplotlib.pyplot as plt

x = np.arange(0, 5, 0.1);
y = np.sin(x)
plt.plot(x, y)
```

 [plot() command](http://matplotlib.sourceforge.net/api/pyplot_api.html#matplotlib.pyplot.plot)

You can control the defaults of almost every property in matplotlib: figure size and dpi, line width, color and style, axes, axis and grid properties, text and font properties and so on. It is very customizable, and modifications may be desirable in certain use cases.

Line properties can be customized by entering colors and linewidths.

```
plt.xlim(X.min()*1.1, X.max()*1.1)
plt.ylim(C.min()*1.1, C.max()*1.1)
```

plt.xlm & plt.ylim are commands for setting limiters

```
plt.xticks( [-np.pi, -np.pi/2, 0, np.pi/2, np.pi],
      [r'$-\pi$', r'$-\pi/2$', r'$0$', r'$+\pi/2$', r'$+\pi$'])#Labels
plt.yticks([-1, 0, +1])
```

Commands for setting ticks along the axis. Labels can also be set as an argument

```
ax = plt.gca()
ax.spines['right'].set_color('none')
ax.spines['top'].set_color('none')
ax.xaxis.set_ticks_position('bottom')
ax.spines['bottom'].set_position(('data',0))
ax.yaxis.set_ticks_position('left')
ax.spines['left'].set_position(('data',0))
```

Spines can be set with positions

Animations are also possible in matplotlib.

All notes are taken from : [https://github.com/rougier/matplotlib-tutorial#introduction](https://github.com/rougier/matplotlib-tutorial#introduction)
