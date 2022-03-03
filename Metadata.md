# Metadata info

```python
ff = FFprobe(input_file)
meta = ff.metadata
```

Metadata variable contains two mainstream information.

1 - Index 0: For the output streams<br/>
2 - Index 1 or -1: For the input stream

So to access the input stream metadata you can do
`inp_meta = ff.metadata[-1]`

## Input metadata
The input metadata is the juiciest of all. It contains all the publicly known metadata, the artist name, album title, etc.
```python
ff = FFprobe('song.mp3')
artist_name = ff.metadata[-1]['artist']
```


## Output metadata
The output metadata mostly contains two streams also;

1 - Index 0: Contains the main stream, for a video input this contains the video, and for an audio input this contains the audio<br/>
2 - Index 1: Contains the second stream if available, for a video input this contains the audio, and for an audio input this contains possibly the album art.

```python
ff = FFprobe('movie.mp4')
codec = ff.metadata[0][0]['codec']  // might return h264
```

```python
ff = FFprobe('movie.mp4)
codec = ff.metadata[0][1]['codec']  // might return aac
```

