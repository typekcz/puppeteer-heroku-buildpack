# puppeteer-heroku-buildpack

Installs dependencies needed in order to run puppeteer on heroku. Be sure to include `{ args: ['--no-sandbox'] }` in your call to `puppeteer.launch`

# Why forked?
This fork adds Chromium packages and Puppeteer env. vars to use installed Chromium. This was done so that Chromium will be installed with ffmpeg support. Use this buildpack if you want to deploy [BeepBoop](https://github.com/typekcz/beepboop-steam) on Heroku.

## Usage

To use the latest stable version run:

```sh-session
$ heroku buildpacks:set typekcz/puppeteer
```

Or use the source code in this repository:

```sh-session
$ heroku buildpacks:set https://github.com/typekcz/puppeteer-heroku-buildpack.git
```

### Additional language support
If you need support for Japanese, Chinese, or Korean fonts, a fork of this buildpack has been made to include those as well: https://github.com/CoffeeAndCode/puppeteer-heroku-buildpack

## Issues

If you run into any issues with this buildpack, please open an issue on this repo and/or submit a PR that resolves it. Different versions of chrome have different dependencies and so some issues can creep in without me knowing. Thanks!
