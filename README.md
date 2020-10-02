# AirQualiSkull 💀

A Halloween decor that also tells you it's safe to go outside.


## Project requirements

1) Get a Raspberry Pi Zero W (or any other Pi, really)
2) Get an API token from https://aqicn.org/data-platform/token/ - the app will look for an `AQICN_API_KEY` env variable on startup. 
3) Get a balena.io account (you can setup your Pi any other way really - I just find this the most convenient, as it allows me to push upgrades to the Pi without doing a literal skull surgery to dig it out 🤷‍)


## Deploying

Once the device is on your balena.io account, you can deploy it with:
```
balena login && balena push <project name> --source .
```

## How it works

The device will use the current location (based on IP) to determine where to fetch air quality from.

https://api.waqi.info/feed/here/?token=e54debcc9d22b5c5f7e31a5ae12f7e3048ec34bc
