# Mashape Analytics jQuery Agent

> for more information on Mashape Analytics, please visit [apianalytics.com](https://www.apianalytics.com)

## About

The Mashape jQuery Analytics agent reports API traffic passing through jQuery ajax calls. Works in all browsers where jQuery is supported and Node.js

## Requirements

- jQuery `1.7+`

## Installation

##### Download

Download the [latest release](https://github.com/Mashape/analytics-agent-jquery/releases)

##### Clone the repo

```bash
$ git clone https://github.com/mashape/analytics-agent-jquery.git
```

##### Install with [Bower](http://bower.io) 

```bash
$ bower install jquery-analytics
```

##### Install with [npm](https://www.npmjs.com)

```bash
$ npm install jquery-analytics
```

##### Install with [SPM](http://spmjs.io)

```bash
spm install jquery-analytics
```

### What's included

```
analytics-agent-jquery/
└── js/
    ├── jquery.analytics.js
    └── jquery.analytics.min.js
```

## Usage

Include `Mashape Analytics Agent` after `jQuery`.

```js
// Basic usage
$.Analytics('SERVICE_TOKEN')

// Advanced usage
$.Analytics('SERVICE_TOKEN', {
  ... options ...
})
```

Done. Now every `global` ajax request will be logged in Mashape Analytics.

## Options

| Option          | Description                                                                       | Required      | Default |
| --------------- | --------------------------------------------------------------------------------- | ------------- | ------------------------------ |
|`serviceToken`   | Mashape Analytics service token, *required when token is not first argument*.     | **Required**  | `-`                            |
|`environment`    | Analytics environment data is stored under                                        | *Optional*    | `-`                            |
|`analyticsHost`  | Mashape Analytics hostname,                                                       | *Optional*    | `socket.analytics.mashape.com` |
|`httpVersion`    | HTTP Version                                                                      | *Optional*    | `HTTP/1.1`                     |
|`fallbackIp`     | Fallback IP for Client / Server when not fetched                                  | *Optional*    | `127.0.0.1`                    |
|`hostname`       | Server hostname                                                                   | *Optional*    | `window.location.hostname`     |
|`fetchServerIp`  | Flag to disable fetching server A Record                                          | *Optional*    | `true`                         |
|`fetchClientIp`  | Flag to disable fetching client address                                           | *Optional*    | `true`                         |
|`debug`          | Debug mode                                                                        | *Optional*    | `false`                        |
|`ssl`            | Flag to enable SSL support                                                        | *Optional*    | `false`                        |

### Disable analytics for request

To disable analytics logging for specific requests when making an ajax request
via jQuery set `global` option to `false`.

## Copyright and license

Copyright Mashape Inc, 2015.

Licensed under [the MIT License](https://github.com/Mashape/analytics-agent-jquery/blob/master/LICENSE)
