# Youless LS120 Custom Component for Home Assistant

## Installation
1) Create a folder named ```custom_components``` into your Home Assistant configuration folder, if not existing
2) Copy the folder ```custom_components/youless``` (including its contents) from this project into the newly created folder
3) Restart Home Assistant

## Available sensors

 Sensor | Description | Measure
  --- | --- | --- 
  pwr | Current Power usage | W 
  net | Net Power usage | kWh 
  p1 | Power Meter Low | kWh 
  p2 | Power Meter High | kWh 
  n1 | Power Delivery Low | kWh
  n2 | Power Delivery High | kWh
  cs0 | Power Meter Extra | kWh
  ps0 | Current Power usage Extra | W
  gas | Gas consumption | m3


## Configuration example

```yaml
  - platform: youless
    name: Youless
    host: <your youless IP address>
    monitored_variables:
      - pwr
      - net
      - p1
      - p2
      - n1
      - n2
      - cs0
      - ps0
      - gas
```
You can configure multiple Youless devices by duplicating the configuration block and giving each device a unique ```name```.
