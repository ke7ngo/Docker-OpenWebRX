![](https://images.microbadger.com/badges/image/thomx/openwebrx.svg)
![](https://images.microbadger.com/badges/version/thomx/openwebrx.svg)

# Docker-OpenWebRX

OpenWebRX docker image

# Requirements
- Docker
- RTL-SDR DVBT USB Dongle (RTL2832)

Now the next step is to customize the parameters of your server in config_webrx.py, further information on [https://github.com/simonyiszk/openwebrx](https://github.com/simonyiszk/openwebrx).

# Install from image
Run : 
```
docker run -d -p 8073:8073 \
--device=/dev/bus/usb:/dev/bus/usb \
-v path/to/your/config_webrx.py:/opt/openwebrx/config_webrx.py \
thomx/openwebrx
```

# Install from source
Run : 
```
docker-compose up -d
```

# Usage
Go to http://dockerhost:8073
