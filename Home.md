Welcome to the pyffmpeg wiki!

# pyffmpeg Wiki

## Usage

### Import pyffmpeg
```python  
from pyffmpeg import FFmpeg
```
### Convert
Convert from one format or codec to other (FFmpeg works with most codecs out there).
```python
inp = 'path/to/music_folder/f.mp4'
out = 'path/to/music_folder/f.mp3'

ff = FFmpeg()
output_file = ff.convert(inp, out)
print(output_file)

```

### Options
pyffmpeg ships with its own FFmpeg executable, but it has only one prebuilt function, the ```convert``` function. So if you would like to do anything else you should use the ```options``` function and pass in all the values just as you would on command prompt except the FFmpeg path itself. For instance, if you would write this on the command prompt:
```
> ffmpeg -i /path/to/video.mp4 -vf scale -1:720 /path/to/video_hd.mp4
```

You should do:

```python
ff = FFmpeg()
ff.options("-i /path/to/video.mp4 -vf scale -1:720 /path/to/video_hd.mp4")
```

avoiding ```ffmpeg``` command and [overwrite](https://github.com/deuteronomy-works/pyffmpeg/wiki#overwrite-default-is-set-to-true) command.

## Advanced Usage
```python
from pyffmpeg import FFmpeg
```

### Use a global directory to store all converted files
```python
ff = FFmpeg('path/to/app_folder')
ff.convert('path/to/music_folder/f.mp3', 'f.wav')
```

### Overwrite (Default is set to True)
```python
ff.overwrite = False # do not overwrite but exit immediately
```

### Get ffmpeg executable
In case you want to use pyffmpeg with another library which gives you more functions and you have to provide an ffmpeg executable. Use the get_ffmpeg_bin function. It returns the full path to our ffmpeg executable.
```python
ff = FFmpeg()
ffmpeg_exe = ff.get_ffmpeg_bin()
```

