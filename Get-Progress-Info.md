## Handle Progress
*NB: For now progress works with only audio files*
* self.report_progress - This should be set to True
* self.onProgressChanged - This should be set to a name of a function
eg.
```python
def handle_progress(progress):
    print(f'{progress}% complete')

ff = FFmpeg()
ff.report_progress = True
ff.onProgressChanged = handle_progress
```
It will print
```shell
10% complete
11% complete
...
100% complete
```