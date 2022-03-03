# FFprobe
Provides FFprobe functions and values

## Usage
### import statement
```python
from pyffmpeg import FFprobe
```



### \_\_init\_\_()
This is the default method when you call the FFprobe class

```python
input_file = 'path/to/music.mp3'
fp = FFprobe(input_file)
```

The probing is done when the class is called this way. The object now
contains the various values stored under their names eg

```python
print(fp.duration)
```
will print
```shell
> 00:04:32:32
```
NB: The above is just for illustration




### get_album_art
expects either a `filename` or `None`.

`filename` - the filename will be used as the name for the image to be stored on disk.<br/>
It can either be a full path or just a filename (meaning the current directory will be used to store the file).

`None` - return the bytes. The bytes will be value returned from the method.

Using a filename
```python
input_file = 'path/to/music.mp3'
fp = FFprobe(input_file)
fp.get_album_art('cover_art.png')
```
`cover_art.png` will be created in the current directory containing the album art

Using None

```python
input_file = 'path/to/music.mp3'
cover_art_bin = FFprobe(input_file).get_album_art()
print(cover_art_bin)
```
will print
```shell
> \x01e\xof4\x01e\xo4e\x03e\x01e\xof4\x01e\xo4e\x03e\x01e\xof4\x01e\xo4e\x03e\x01e\xof4\x01e\xo4e\x03e\x01e\xof4\x01e\xo4e\x03e\xof4\x01e\xo4e\x03e
...
```
NB: The above bytes output is just for illustration



## Values

`duration` -

`fps` -

`bitrate` -

`metadata` - all the metadata info. Use this to access all the metadata of all the various streams. More on metadata [here]("https://github.com/deuteronomy-works/pyffmpeg/wiki/Metadata")