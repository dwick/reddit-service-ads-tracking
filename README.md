# reddit_service_ads_tracking

[![Build Status](https://travis-ci.org/reddit/reddit-service-ads-tracking.svg?branch=master)](https://travis-ci.org/reddit/reddit-service-ads-tracking)

This service provides endpoints for tracking ad clicks, impressions, and conversions.

## prereqs

- vagrant (https://www.vagrantup.com/downloads.html)
- virtualbox (https://www.virtualbox.org/wiki/Downloads)

## installation

    vagrant up

## run the tests

    vagrant ssh -c "cd src; nosetests"

## development

Please install the git hooks for development:

    chmod +x hooks/*
    cp hooks/* .git/hooks
