[![Build Status](https://travis-ci.org/zalando/nakadi.svg)](https://travis-ci.org/zalando/nakadi)

Simple Nakadi startup:

gradle run

Full development pipeline:
build -> ut/it tests (depends on access to a kafka backend) -> docker (builds docker image) -> api-tests (runs tests against the docker image)

