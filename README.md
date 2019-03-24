# BashWeather
A bash script to get the weather from OpenWeatherMap and output to the terminal, Openbox, or HTML


## Contents
 1. [About](#1-about)
 2. [License](#2-license)
 3. [Prerequisites](#3-prerequisites)
 4. [How to use](#4-how-to-use)

***

## 1. About

Weather report written in Bash.

`weather.sh` gets the current weather from 
[OpenWeatherMap](http://openweathermap.org/) and displays the 
results to the terminal, HTML, or for an OpenBox pipe menu. It will 
calculate (if appropriate) the "feel like" weather by calculating the
wind chill or heat index. A great deal of basis for this script comes 
from [BashWeather](https://github.com/jdotjdot/BashWeather),
[bash-weather](https://github.com/szantaii/bash-weather),
and many more that I forgot to save the URLs of.

## 2. License

This project is licensed under the MIT license. For the full license, see `LICENSE`.

## 3. Prerequisites

 * OpenWeatherMap API key ([http://openweathermap.org/appid](http://openweathermap.org/appid)).
 * Bash shell ≥ 4.2.
 * `bc` basic calculator for floating point arithmetic. Can be found in the `bc` package on major Linux distributions.
 * `curl` command-line tool for getting data using HTTP protocol. cURL can be found in the `curl` package on major Linux distributions.
 * `grep` command-line tool used for parsing downloaded XML data. `grep` can be found in the `grep` package on major Linux distributions.

## 4. How to use

### Options

At the beginning of the script is a place for your default location and 
API key. These will be moved to an `rc` or `ini` file later. You may 
also specify them on the commandline.

### Command-line options

`weather.sh` can be started with the following command line options:

 * `-k` Specifies OpenWeatherMap API key from the command-line.
 * `-l city_name` Sets the city for manual weather lookup.
 * `-t` Output to the terminal/stdout (default if no output is specified)
 * `-h` Output HTML formatted text
 * `-o` Output OpenBox output
 * `-f` Use imperial (farenheit, inches Hg, mph) units; default is metric

_Note: If the OpenWeatherMap API key is specified from the command-line, it will override the API key set in the file._
