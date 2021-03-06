# Open Weather

[![CircleCI](https://circleci.com/gh/aquinofb/open_weather.svg?style=svg)](https://circleci.com/gh/aquinofb/open_weather)
[![codebeat badge](https://codebeat.co/badges/31b1c182-d480-4cd0-bc62-8c7c021bbc6a)](https://codebeat.co/projects/github-com-aquinofb-open_weather)
[![Code Climate](https://codeclimate.com/github/aquinofb/open_weather/badges/gpa.svg)](https://codeclimate.com/github/aquinofb/open_weather)
[![Issue Count](https://codeclimate.com/github/aquinofb/open_weather/badges/issue_count.svg)](https://codeclimate.com/github/aquinofb/open_weather)
[![Test Coverage](https://codeclimate.com/github/aquinofb/open_weather/badges/coverage.svg)](https://codeclimate.com/github/aquinofb/open_weather/coverage)

App that consumes the API from [Open Weather Map](http://openweathermap.org/) and show 16 days forecast.

## Configuration

Get your Open Weather's API Key on this [link](http://openweathermap.org/appid) and export an `environment var` called `OPENWEATHER_KEY`.

```shell
$ export OPENWEATHER_KEY=YOUR_API_KEY
$ bundle install
$ rails s
```

## API

#### GET /forecasts(.format)
```ruby
filter: {
  city: String # Name of the city
}
```

#### GET /forecasts_daily/:id(.format)
```ruby
{
  id: Int, # ID(dt) from forecast_daily
  city: String # Name of the city
}
```

## Tests

The app uses **RSpec** to run the automated tests. Run the following command:

```shell
rake spec
```
