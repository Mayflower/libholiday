# libholiday

[![Build Status](https://travis-ci.org/mayflower/libholiday.svg?branch=master)](https://travis-ci.org/mayflower/libholiday)

A library to calculate holidays.

Supported countries and states

* America
* Germany and all constituent states
* Sweden
* Netherlands

Installation

```composer require mayflower/holiday```

Usage

```php
<?php

require_once __DIR__ . '/vendor/autoload.php';

$holidays = new Holiday\Germany();

// Returns array of Holiday objects, if any between the given dates.
$holidays->between(
     new \DateTime('01.01.2018'),
     new \DateTime('31.12.2018')
);

// isHoliday calls ->between with the given date to both parameters.
$holidays->isHoliday(new \DateTime('01.05.2018'))
```
