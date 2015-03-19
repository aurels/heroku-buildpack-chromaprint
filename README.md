# heroku-buildpack-chromaprint

## About

Buildpack to run [Chromaprint](https://acoustid.org/chromaprint) on [Heroku](https://heroku.com).

## Installation

Use `heroku-buildpack-multi` in order to have multiple buildpacks applied.

    $ heroku create --buildpack https://github.com/ddollar/heroku-buildpack-multi

    $ cat .buildpacks
    https://github.com/aurels/heroku-buildpack-chromaprint
    https://github.com/heroku/heroku-buildpack-ruby

    $ git push heroku master

You should see something like this in the output :

    remote: -----> Fetching custom git buildpack... done
    remote: -----> Multipack app detected
    remote: =====> Downloading Buildpack: https://github.com/aurels/heroku-buildpack-chromaprint
    remote: =====> Detected Framework: Chromaprint
    remote:        Adding fpcalc to PATH
    remote: =====> Downloading Buildpack

To check if it has been applied :

    $ heroku run fpcalc -version
