# MitraStar_GPT-2541GNAC_HA
### MitraStar GPT-2541GNAC (Movistar Spain  Router) Component(Device Tracker) for Home Assistant

## Configuration variables:
**host (Required):** The hostname/IP address of the MitraStar Router. <br />
**username (Required):** Username for MitraStar Router. 1234 is the default username <br />
**password (Required):** Password for MitraStar Router. <br />
The rest of variables are optional and Home Assistant default variables...

## Installation:

1. Download and place **MitraStar_GPT-2541GNAC** folder in the home-assistant custom components folder like this:
```
 .homeassistant/custom_components/MitraStar_GPT-2541GNAC/*.*
```

2. Add the new platform in the **configuration.yaml**:
```
device_tracker:
  - platform: MitraStar_GPT-2541GNAC
    host: 192.168.1.1
    username: 1234
    password: router_password
    interval_seconds: 120
    consider_home: 200
    new_device_defaults:
      track_new_devices: False
      hide_if_away: False

```

       
 3. **Restart** the home assistant service.
 
 ## To-DO
 
 Extend current compontent adding a sensor that retrieves Fiber Power Value (in DBm) 
 
 I have a internet metric system that shows some instability, for that reason I have been thinking to take advantage of Movistar Router Fiber Power metrics in order to be able to get a better picture of connectivity.
 
 
 
 [Router installation parameters url][http://192.168.1.1/installation_ontpw.html]
 
 Parameters to parse:
 ```
<span class="sub">Router: <br>Conectado a Internet </span>

<span class="sub">Potencia óptica recibida[dBm]: <br>-18.9962945488244</span>
```
