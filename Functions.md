# Functions

### \_\_init\_\_:

### convert:

### options:

### get_ffmpeg_bin:

### log_level

Set the log level to control how much info and errors are display in the console.

```python
ff = FFmpeg()
ff.loglevel = 'info'
ff.convert('path/to/music_folder/f.mp3', 'f.wav')
```

#### Default
Default value is ```fatal```

#### Possible values
Corresponds with FFmpeg loglevel flags

* 'quiet'
* 'panic'
* 'fatal'
* 'error'
* 'warning'
* 'info'
* 'verbose'
* 'debug'
* 'trace'
