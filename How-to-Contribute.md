## Contributing Guidelines

There are many ways in which you can participate in this project, for example:

* [Submit bugs and feature requests](https://github.com/deuteronomy-works/pyffmpeg/issues), and help us verify as they are checked in
* Review [source code changes](https://github.com/deuteronomy-works/pyffmpeg)
* Review the [documentation](https://github.com/deuteronomy-works/pyffmpeg/wiki) and make pull requests for anything from typos to additional and new content

If you are interested in fixing issues and contributing directly to the code base, 
please check out contributing guidelines [here](https://docs.github.com/articles/github-community-guidelines) 
 and then,

* Fork the project.
* Switch to the branch that has the name of the OS you are using (i.e., build-darwin: MacOS, build-linux: Linux, build-windows: Windows).
* Navigate to `pyffmpeg/pyffmpeg/static/bin/` on your computer then go to the folder with your OS name and then copy that `.py` file. (i.e., `darwin/darwin.py`: MacOS, `linux/linux.py`: Linux, `win32/win32.py`: Windows).
* Copy the file outside the repo directory, becuase you will change directory away from your build-`os` branch. So copy it somewhere, to say *your desktop*.
* Now Switch branch to the `develop` branch and create a new branch with `develop` branch as it's base branch.
* After making your changes send the pull request to the `develop` branch.
* After your pull request has been merged, delete your new branch. Switch to the develop branch and fetch upstream, then create a new branch out of the develop branch again.

## Testing
Always test your code while working with

```python local_t_est.py```

for pyffmpeg test and

```python local_probe_t_est.py```

for FFprobe test.

When you are done, test using pytest

```pytest -v```
