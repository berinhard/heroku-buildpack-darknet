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

Inspired by [heroku-buildpack-wkhtmltopdf](https://github.com/turicas/heroku-buildpack-wkhtmltopdf/blob/master/bin/compile).
