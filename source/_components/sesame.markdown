---
layout: page
title: "Sesame Smart Lock"
description: "Instructions on how to integrate Sesame by CANDY HOUSE into Home Assistant."
date: 2017-05-02 12:00
sidebar: true
comments: false
sharing: true
footer: true
logo: sesame.png
ha_category:
  - Lock
ha_iot_class: Cloud Polling
ha_release: 0.47
redirect_from:
 - /components/lock.sesame/
---

The `sesame` platform allows you to control your [Sesame](https://candyhouse.co/) smart locks made by CANDY HOUSE, Inc.

## Configuration

Your Sesame needs to be paired with a mobile device running the app in *virtual station* mode, or a standalone [Wi-Fi Access Point](https://candyhouse.co/collections/frontpage/products/wi-fi-access-point).

You will also need to generate an API key from [my.candyhouse.co](https://my.candyhouse.co/#/credentials).

Once you have remote access enabled using one of the above AND the Integration - cloud option enabled on the Sesame app for that lock settings, add the following to your `configuration.yaml` file:

```yaml
# Example configuration.yaml entry
lock:
  - platform: sesame
    api_key: YOUR_SESAME_API_KEY
```

{% configuration %}
api_key:
  description: The API key for your Sesame account.
  required: true
  type: string
{% endconfiguration %}
