---
# This page was generated from the add-on.
title: Automation Framework - URL Presence Job Tests
type: userguide
weight: 16
---

# Automation Framework - URL Presence Job Test

URL Presence tests are supported by all the jobs. These tests can be used to validate the presence/absence of a URL and it's specific expressions in the HTTP response/request. The expressions are specified in the YAML file as regular expressions. The test will pass if the URL or the specified expression is found in the response/request depending upon the operator selection.


A job can have tests for multiple expressions, and multiple tests can be created for expressions having the same URL.

## YAML

```
  jobs:
  - type: something
    tests:
      - name: 'test one'                      # Name of the test, optional
        type: url                             # Specifies that the test is of type 'url'
        url: http://www.example.com/path      # String: The URL to be tested.
        operator: 'and'                       # One of 'and', 'or', default is 'or'
        requestHeaderRegex:                   # String: The regular expression to be matched in the request header, optional
        requestBodyRegex:                     # String: The regular expression to be matched in the request body, optional
        responseHeaderRegex:                  # String: The regular expression to be matched in the response header, optional
        responseBodyRegex:                    # String: The regular expression to be matched in the response body, optional
        onFail: 'info'                        # String: One of 'warn', 'error', 'info', mandatory
```
