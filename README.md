# Description
I forked this when looking at how to get http4s to serve scalajs output in an idiomatic fashion. The specified docker base image was no longer resolving, and updating it fixed this issue at the time of writing.

# scalajs-react-http4s-starter
[![Build Status](https://travis-ci.org/oen9/scalajs-react-http4s-starter.svg?branch=master)](https://travis-ci.org/oen9/scalajs-react-http4s-starter)

# Libs

## backend
1. scala
1. cats
1. http4s
1. pureconfig

## frontend
1. scalajs
1. reactjs\
  [scalajs-slinky-http4s-starter](https://github.com/oen9/scalajs-slinky-http4s-starter) for `slinky`
1. diode

# DEV

## js
`fastOptJS::webpack`\
`~fastOptJS`\
http://localhost:12345/js/target/scala-2.12/classes/index-dev.html

## server
`reStart`\
http://localhost:8080/

## js + server (dev conf)
Run server normally `reStart`.\
Connect your js api to http://localhost:8080 (e.g. change some baseUrl in js project).\
Run js: `fastOptJS::webpack` and `fastOptJS`.\
Open http://localhost:12345/js/target/scala-2.12/classes/index-dev.html in browser.\
When server changed run `reStart`.\
When js changed run `fastOptJS`.

## hints
Remember to run `fastOptJS::webpack` after e.g. `npmDependencies` changes.
