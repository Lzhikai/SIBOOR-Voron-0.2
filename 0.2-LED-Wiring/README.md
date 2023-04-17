## Setting the LED switch：

### Install the LED Effects Library
This will install the LED Effects for Klipper plugin from [here](https://github.com/julianschill/klipper-led_effect)

SSH into your Fly Gemini

```shell
cd ~
git clone https://github.com/julianschill/klipper-led_effect.git
cd klipper-led_effect
./install-led_effect.sh
```


### Add to printer.cfg  
```
[output_pin LED]
pin: !PB1
pwm: False
```

## Setting the RGB strip:
### Add to printer.cfg 
```
[neopixel my_neopixel]  
pin:PA9 # Main Board Pin Definitions  
chain_count:24 # Number of RGB's   
color_order: GRB # Colour order  
initial_RED: 0.2 # Red Light on default value is 1 max.  
initial_GREEN: 0.2 # Green Light on default value is 1 max.  
initial_BLUE: 0.2 # Blue Light on default value is 1 max.  
  ```
```
[led_effect rainbow]   
leds:    
    neopixel:my_neopixel  
layers:  
  gradient 0.50 0.50 top (1,0,0),(0,1,0),(0,0,1) 
frame_rate: 24  
  
[led_effect extruder_temp]  
leds:  
    neopixel:my_neopixel  
layers:  
    heater 0.50 0.50 top (0.0,1.0,0.0),(1.0,0.0,0.0),(0.0,0.0,1.0)  
frame_rate: 24  
heater: extruder  
autostart: true  
  
[led_effect bed_heating]  
leds:  
    neopixel:my_neopixel  
layers:  
    heater 0.50 0.50 top (0.0,1.0,0.0),(1.0,0.0,0.0),(0.0,0.0,1.0)  
frame_rate: 24  
heater: heater_bed  
autostart: true  
  ```

<img src="https://github.com/Lzhikai/SIBOOR-Voron-0.2/blob/main/0.2-LED-Wiring/0.2-LED-Wiring.jpg" width="800" height="550">
