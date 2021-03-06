---
layout: page
title: "qBittorrent Sensor"
description: "Instructions on how to integrate qBittorrent sensors within Home Assistant."
date: 2018-11-21 00:00
sidebar: true
comments: false
sharing: true
footer: true
logo: qbittorrent.png
ha_category:
  - Downloading
ha_release: 0.84
ha_iot_class: Local Polling
redirect_from:
 - /components/sensor.qbittorrent/
---

The `qbittorrent` platform allows you to monitor your downloads with [qBittorrent](https://www.qbittorrent.org/) from within Home Assistant and setup automations based on the information.

## Setup

This sensor requires the qBittorrent Web UI enabled. The [official reference](https://github.com/qbittorrent/qBittorrent/wiki#webui-related) describes how to set up the Web UI.

## Configuration

To enable this sensor, add the following lines to your `configuration.yaml`:

```yaml
# Example configuration.yaml entry
sensor:
  - platform: qbittorrent
    url: 'http://<hostname>:<port>'
    username: YOUR_USERNAME
    password: YOUR_PASSWORD
```

{% configuration %}
url:
  description: The URL of the Web UI of qBittorrent.
  required: true
  type: string
name:
  description: The name to use when displaying this qBittorrent instance.
  required: false
  type: string
username:
  description: The username of the Web UI of qBittorrent.
  required: true
  type: string
password:
  description: The password of the Web UI of qBittorrent.
  required: true
  type: string
{% endconfiguration %}
