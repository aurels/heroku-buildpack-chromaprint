# heroku-buildpack-chromaprint

Install :

    $ heroku create my-app --buildpack https://github.com/ddollar/heroku-buildpack-multi

    $ cat .buildpacks
    https://github.com/aurels/heroku-buildpack-chromaprint
    https://github.com/heroku/heroku-buildpack-ruby

    $ git push heroku master


Check if it's OK :

    $ heroku run vendor/chromaprint-fpcalc-1.1-linux-x86_64/fpcalc -version
