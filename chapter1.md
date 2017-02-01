---
title       : Plotly in Python
description : Insert the chapter description here

--- type:NormalExercise lang:python xp:100 skills:1 key:880d44e748
## Plotly example

This exercise features an example of plotly.

*** =instructions
- Just hit submit answer

*** =hint
- No hints!

*** =pre_exercise_code
```{python}
```

*** =sample_code
```{python}
from plotly import __version__
from plotly.offline import plot
from plotly.graph_objs import Scatter, Figure, Layout
x = [1, 2, 3]; y = [1, 2, 3];
plot([Scatter(x=x, y=y, mode = 'markers')])
```

*** =solution
```{python}
from plotly import __version__
from plotly.offline import plot
from plotly.graph_objs import Scatter, Figure, Layout
x = [1, 2, 3]; y = [1, 2, 3];
plot([Scatter(x=x, y=y, mode = 'markers')])
```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:8546b612c1
## Plotly Example No. 2




*** =instructions

*** =hint

*** =pre_exercise_code
```{python}
from plotly import __version__
from plotly.offline import plot
```

*** =sample_code
```{python}
from plotly import __version__
from plotly.offline import plot
from plotly.graph_objs import *
import pandas as pd

df = pd.read_csv('https://plot.ly/~etpinard/191.csv')

plot({
    'data': [
        Scatter(x=df[continent+', x'],
                y=df[continent+', y'],
                text=df[continent+', text'],
                marker=Marker(size=df[continent+', size'], sizemode='area', sizeref=131868,),
                mode='markers',
                name=continent) for continent in ['Africa', 'Americas', 'Asia', 'Europe', 'Oceania']
    ],
    'layout': Layout(xaxis=XAxis(title='Life Expectancy'), yaxis=YAxis(title='GDP per Capita', type='log'))
}, show_link=False)
```

*** =solution
```{python}
from plotly import __version__
from plotly.offline import plot
from plotly.graph_objs import *
import pandas as pd

df = pd.read_csv('https://plot.ly/~etpinard/191.csv')

plot({
    'data': [
        Scatter(x=df[continent+', x'],
                y=df[continent+', y'],
                text=df[continent+', text'],
                marker=Marker(size=df[continent+', size'], sizemode='area', sizeref=131868,),
                mode='markers',
                name=continent) for continent in ['Africa', 'Americas', 'Asia', 'Europe', 'Oceania']
    ],
    'layout': Layout(xaxis=XAxis(title='Life Expectancy'), yaxis=YAxis(title='GDP per Capita', type='log'))
}, show_link=False)
```

*** =sct
```{python}

```

--- type:NormalExercise lang:python xp:100 skills:2 key:368be49690
## Plotly Example #3



*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
from plotly import __version__
from plotly.offline import download_plotlyjs, plot

# Create random data with numpy
import numpy as np

N = 1000
random_x = np.random.randn(N)
random_y = np.random.randn(N)

# Create a trace
trace = go.Scatter(
    x = random_x,
    y = random_y,
    mode = 'markers'
)

data = [trace]

# Plot and embed in ipython notebook!
plot(data, filename='basic-scatter')

```

*** =solution
```{python}
from plotly import __version__
from plotly.offline import download_plotlyjs, plot

# Create random data with numpy
import numpy as np

N = 1000
random_x = np.random.randn(N)
random_y = np.random.randn(N)

# Create a trace
trace = go.Scatter(
    x = random_x,
    y = random_y,
    mode = 'markers'
)

data = [trace]

# Plot and embed in ipython notebook!
plot(data, filename='basic-scatter')
```

*** =sct
```{python}

```
