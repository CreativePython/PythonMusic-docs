# Automate

PythonMusic supports automation through the Automate class.

Automate allows repeated calls of functions (animating graphics, sweeping a volume or filter, stepping through data, and so on).  It uses a single master clock, so everything stays in sync. 

For more customizable automation, see the [Timer](../timer/index.md) class.

## Creating an Automation

To automate the repeated calling of a function use [Automate.add()](add.md):

```python
Automate.add(moveCircle)
```

Automation starts as soon as the first function is added.  

Automation rate is measured in frames (or function calls) per second.  The default is 60 frames per second.

For example:

```python title="randomlyMovingCircle.py"
--8<-- "examples/_snippets/randomlyMovingCircle.py"
```

## Functions

The following Automate functions are available:

| Function | Description |
|---|---|
| [`add(action)`](add.md) | Calls a function repeatedly based on automation rate (see [setRate()](setRate.md)). |
| [`remove(action)`](remove.md) | Stop calling a registered function. |
| [`resume()`](resume.md) | Resume automation after a pause. |
| [`pause()`](pause.md) | Pause automation. |
| [`getRate()`](getRate.md) | Return how often automation runs.  Default is 60 frames per second. |
| [`setRate()`](setRate.md) | Set how often automation runs. |
| [`addWithValues(action, values)`](addWithValues.md) | Step a function through a list of values, evenly spaced over time. |
| [`addWithTimedValues(action, values, times)`](addWithTimedValues.md) | Step a function through a list of values, each delivered at its own time. |
