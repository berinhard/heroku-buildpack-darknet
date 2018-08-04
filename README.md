# heroku-buildpack-darknet

This buildpack downloads and extracts [Darknet](https://github.com/pjreddie/darknet).


## Add the Buildpack

Just add the buildpack to your heroku app by executing:

```bash
heroku buildpacks:add https://github.com/berinhard/heroku-buildpack-darknet.git
```

## Usage

The darknet project will be available stored in `/app/darknet/`.
You can just execute `/app/darknet/darknet ...` from your app.

## Integrating with other applications

If you're running this buildpack with a Python application, you can run from your python code:

```python
import subprocess, shlex

command = './darknet detect cfg/yolov3.cfg yolov3.weights data/dog.jpg'
detect = subprocess.Popen(
    shlex.split(command),
    cwd='/app/darknet/',
)
detect.wait()
```

Inspired by [heroku-buildpack-wkhtmltopdf](https://github.com/turicas/heroku-buildpack-wkhtmltopdf/blob/master/bin/compile).
