# Weather Station
This template provides a complete implementation of the [Losant Walkthrough](https://docs.losant.com/getting-started/walkthrough/). Weather data is periodically requested from an external API and recorded to a [Losant Device](https://docs.losant.com/devices/overview/). The recorded weather data is then presented on your own personal weather dashboard.

## Setup
1. Navigate to your [Application Globals](https://app.losant.com/applications/~losant-application-weatherStation-0~/globals) and configure the following fields:
	1. `gps_location`—Location (latitude, longitude) that will be used when requesting weather data.
	1. `dark_sky_api_key`—Dark Sky API key. [Dark Sky](https://darksky.net/dev) is a separate, paid service, that you'll have to sign up for (one key per company). With this key, the first 1,000 forecasts per day are free, which is enough for this application.
2. Enable the [Weather Grabber](https://app.losant.com/applications/~losant-application-weatherStation-0~/workflows/~losant-flow-weatherGrabber-0~/develop) workflow.

## Weather Grabber Workflow
The [Weather Grabber](https://app.losant.com/applications/~losant-application-weatherStation-0~/workflows/~losant-flow-weatherGrabber-0~/develop) workflow has a timer that runs every two minutes to request weather data from the Dark Sky API. It uses the API key and location that you configured above.

## Weather Station Dashboard
The [Weather Station](https://app.losant.com/dashboards/~losant-dashboard-weatherStation-0~) dashboard displays a variety of live and historical weather data. This data is displayed from the [Weather](https://app.losant.com/applications/~losant-application-weatherStation-0~/devices/~losant-device-weather-0~) device, which is updated by the Weather Grabber workflow.

## Resources
The following list contains resources related to how this template is implemented:

* [Losant Walkthrough](https://docs.losant.com/getting-started/walkthrough)
* [Workflows](https://docs.losant.com/workflows/overview/)
* [Devices](https://docs.losant.com/devices/overview/)
* [Dashboards](https://docs.losant.com/dashboards/overview/)

---

This template was created by Losant. For license details, or to submit feature requests or bugs, visit the [GitHub repository](https://github.com/Losant/application-templates). If you have general questions or comments, let us know on the [Losant Forums](https://forums.losant.com).

Copyright (c) 2020 Losant IoT, Inc

https://www.losant.com