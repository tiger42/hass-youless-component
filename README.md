# youless
Home Assistant custom sensor for youless LS120

Based on the version of [Gerben Jongerius](https://bitbucket.org/jongsoftdev/youless) and the aditions of pdwonline.

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
