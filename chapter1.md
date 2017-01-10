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
