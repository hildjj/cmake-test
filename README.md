[![Build Status](https://travis-ci.org/hildjj/cmake-test.svg?branch=master)](https://travis-ci.org/hildjj/cmake-test)

This repo shows how to use a late-model cmake on
[travis-ci](https://travis-ci.org/) **without** impact to your build times.
The important piece in your ``.travis.yml` file:

    addons:
      apt:
        sources:
          - george-edison55-precise-backports
        packages:
          - cmake
          - cmake-data

[Nathan Osman](https://launchpad.net/~george-edison55) hooked us up with his
[precise-backports](https://launchpad.net/~george-edison55/+archive/ubuntu/precise-backports) PPA,
which is on the
[list](https://github.com/travis-ci/apt-source-whitelist/blob/master/ubuntu.json)
that Travis trusts. Thanks, Nathan!
