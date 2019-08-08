Notifier
========

This repository demonstrates the usage of Desktop Codeception Extension API.
Check it's source code to write your own extensions.

## Desktop Notification Extensions for Codeception

Extensions from this package that can be included in Codeception to receive notification of test results.

**This notifications are limited to just a few basic examples. It is recommended to get it forked and patched for your actual needs.**

Notifcation are made via [jolinotif](https://packagist.org/packages/jolicode/jolinotif) library by [JoliCode
](https://github.com/jolicode).

## Installation

Install this package

```
composer require dalamar/codeception-desktop-notifier --dev
```

Enable extensions in `codeception.yml` configuration:

Sample:

``` yaml
paths:
    tests: tests
    log: tests/_log
    data: tests/_data
    helpers: tests/_helpers
extensions:
    enabled:
      # enable desktop notifications
      - Dalamar\Codeception\Extension\DesktopNotifier # extension class name

```

If you are anything like me and executing tests from within vagrant VM, 
then you may want to proxy notifications from virtual to host machine.

To do that you need to install vagrant plugin [vagrant-notify](https://github.com/fgrehm/vagrant-notify) and follow the instructions.

-----
