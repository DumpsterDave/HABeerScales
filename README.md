# HABeerScales

For quite a while I used the Plaato Keg scales in my kegerator.  For the most part, I really liked them.  Unfortunately, they recently announced that they were killing off the API that I used to get information about my keg levels.  I also spoke with a friend of mine that said he was looking for a solution, but had trouble finding something that was low enough profile.  I decided it was time to replace the Plaato Kegs and create something as low profile as possible.  What I ended up with was a scale that can support a full keg and is only 13mm in height which is actually thinner than the Plaato Keg.  These are also quite a bit cheaper than the Plaato Keg and clock in at just over $260 for the whole setup if done as a single set, compared to about $100 per scale for Plaatos.

## License

This work is shared under the Creative Commons BY-NC-SA 4.0 license.  You are free to share and adapt under the following terms:

* Attribution — You must give appropriate credit , provide a link to the license, and indicate if changes were made . You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
* NonCommercial — You may not use the material for commercial purposes .
* ShareAlike — If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC_BY--NC--SA_4.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

## The Main Components

There are two main components to this.  The scales, and the controller.  The controller is powered via an ESP32, specifically, an esp32-s3-devkitc-1-n8r2.  The controller (as built) supports 5 scales (4 kegs + CO2 tank), a drain sensor, and a pressure sensor.

## Required Tools

You will need the following tools to assemble the scales and controller as detailed.

- 2.5mm Hex Allen Key
- T20 Torx Bit
- #1 Phillips Screwdriver
- Soldering Iron
- Terminal Crimping Tools
- M3x0.5mm Tap
- M4x0.7mm Tap

You will also need access to a 3D printer (or someone with one) that has a build plate capable of printing a 190x210mm object to build the enclosure.  An alternative is to purchase an enclosure from your local big box store and modify it as required.

## Bill of Materials and Cost

The quantities of parts listed below is for 4 keg scales and the controller.  It does not include the pressure senor or load cell for the CO2 tank, however, if you want to utilize one of these scales for your CO2 tank, you just need to add those parts.  The STLs that are part of this repo make use of the parts listed below.  Changing parts may require you to modify the STLs accordingly.

|Part|Part Number|Qty Needed|Used For|Approx Unit Cost|Subtotal|
|-|-|-|-|-|-|
|Meanwell 25W 5v Power Supply|RS-25-5|1|Controller|12.73|12.73|
|C-13 Fused Power Inlet|FN9260SB-2-06-30|1|Controller|14.48|14.48|
|#6 Crimp Fork Terminals|[generic](https://a.co/d/jd4sUM7)|5|Controller|9.94|9.94|
|14ga Female Spade Connector|varies|3|Controller|-|-|
|ESP32 S3 DevKitC 1|ESP32-S3-DevKitC-1-N8R2|1|Controller|5.96|5.96|
|Prototype Board|[generic](https://a.co/d/2vtq4lW)|1|Controller|8.49|8.49|
|Molex SL 4 Circuit Panel Mount Housing|70107-5038|5|Controller|0.85|4.25|
|Molex SL 3 Circuit Panel Mount Housing|70107-5037|1|Controller|1.39|1.39|
|Molex SL 2 Circuit Panel Mount Housing|70107-5036|1|Controller|1.23|1.23|
|Molex SL 4 Circuit WireToWire Housing|70107-0003|4|Cables|0.45|1.80|
|Molex SL 4 Circuit Plug|70066-0388|8|Cables, Scales|0.32|2.56|
|Molex SL 22-30ga Crimp Socket|16-02-0069|50|Cables, Scales|0.08|4.00|
|Molex SL 22-30ga Crimp Pin|16-02-0105|50|Controller, Cables|0.09|4.50|
|Molex 4P TPA|73838-0004|17|Controller, Cables, Scales|0.20|3.40|
|Molex 3P TPA|73838-003|1|Controller|0.17|0.17|
|Molex 2P TPA|73838-002|1|Controller|0.24|0.24|
|Harwin M20 22-30ga Crimp Terminals|M20-1180046|30|Controller|0.09|2.70|
|Harwin M20 Polarising Key|M20-003|5|Controller|0.28|1.4|
|Harwin M20 1pos Housing|M20-1060100|1|Controller|0.12|0.12|
|Harwin M20 2pos Housing|M20-1060200|2|Controller|0.13|0.13|
|Harwin M20 4pos Housing|M20-1060400|5|Controller|0.20|1.00|
|Harwin M20 5pos Housing|M20-1060500|1|Controller|0.24|0.24|
|Harwin M20 6pos Housing|M20-1060600|5|Controller|0.28|1.40|
|Harwin M20 10pos DR Housing|M20-1070500|5|Controller|0.41|2.05|
|Harwin M20 22pos Socket|M20-7822046|2|Controller|2.20|4.40|
|Harwin M20 8pos Header|M20-9730846|1|Controller|0.35|0.35|
|Harwin M20 4pos Header|M20-9730446|1|Controller|0.19|0.19|
|Harwin M20 2pos Header|M20-9730246|6|Controller|0.10|0.60|
|Harwin M20 4pos DR Header|M20-9720246|1|Controller|0.25|0.25|
|Scale Tops from Send-Cut-Send|0.125" 304 Stainless Steel|4|Scales|27.45|109.80|
|M3x0.5x05mm SHCS|91292A123|4 (Sold in packs of 100)|Controller|8.18|8.18|
|M3x0.5x5mm SHCS|91292A110|32 (Sold in packs of 100)|Scales|6.00|6.00|
|M4x0.7x10mm BHCS|90991A122|4 (Sold in packs of 100)|Scales|6.64|6.64|
|M3x0.5x4mm Heat Insert|[generic](https://a.co/d/2Yv5wxr)|4|Controller|9.39|9.39|
|28ga 4 pair Silicone Wire|[generic](https://a.co/d/as6JnqN)|1|Cables|19.98|19.98|
|50kg Load Cells|[generic](https://a.co/d/htYuJL1)|1|Controller, Scales|9.99|9.99|
|Extra HX711|[generic](https://a.co/d/774xzos)|1|Controller|9.49|9.49|
|||||||
|**Subtotal:**|||||**$269.44**|

> [!NOTE]
> Some of these items have volume discounts that may not be reflected in the above list.  For the Harwin M20 connectors, people may opt to use generic dupont clones that you can find on any mass retail site.  Using generic connectors can bring your costs down a little bit and give you plenty of spares, however I personaly prefer to get genuine parts when I can.  I do not recommend that you purchase the Meanwell power supply or power inlet off of Amazon due to the high rate of fakes.  The ones that I've seen sell for pretty much the same price, so it's best to get those from a reputable source like Digikey or Mouser.  You can get a large pack of screws from Amazon as well.  I find the socket formation on their screws to be a bit suspect at times, but they should suffice for our purposes.

If you can find other people that want scales, your per-part price from Send-Cut-Send can come down considerably.  For example, when going from 4 scales to 8, the unit price drops by $4 to 23.29.  The more people you get in on the purchase, the cheaper the indiviual pieces will be and you can split up some of the bulk items like screws and such.  Another alternative is to 3D print scale tops.  For my prototype, I printed a 6MM thick plate out of ABS.  It held up perfectly fine with a standard corny keg.  Using 3D printed scale tops can drop your per-scale cost down to almost nothing and really bring the project cost down.  Plastic does flex though, so I cannot say how a 3D printed top might hold up over the long run.

## Controller

For the controller, you'll first need to print out the top and one of the bottoms.  For the top, I recommend supports for the recessed area for the USB ports.  Everything else can be printed without supports.  I printed my cases with Polymaker PolyLite Silver PETG.

1. Solder the headers onto your ESP32.  You'll want to solder the headers to the back side of the ESP32.
2. Solder the two Harwin M20 22-position sockets (M20-7822046) on the Back of the breadboard.  Viewing the above picture, the front has individual solder points as opposed to joined traces.  Be sure that the right side of the board indicates negative as our wiring assumes the far right pin will be ground.  It can be helpful for soldering to insert your ESP32 into the sockets before soldering the sockets to the board to help hold them in alignment.  You sockets should be soldered into holes A7-28 and I7-28.
3. To the front, headers as shown in the [Header Locations](PDF/Header%20Locations.pdf).
4. Add a jumper wire from F8 to the + rail and from I28 to the - rail.
5. Once complete, it should look something like the following:
![Breadboard Wiring](images/solder-breadboard.png)
6. Next, wire the ESP32 to the HX711s and then the HX711s to the panel mount connectors.  They should be wired up similar to how is illustrated in the [Scale Wiring](PDF/Scale%20Wiring.pdf), however there's no guarantee that the HX711's that you get will have the same pinout so be sure to wire them appropriately.  From the HX711s to the panel mount SL connectors, use the six position M20 connector to join the A and B channels (+ to +, - to -).  This will allow you to select any gain level without re-wiring the connectors.  A channel supports a gain of 128 or 64.  B channel supports 32.  A lower gain decreases the sensitivity of the scales which can be helpful if there's too much variation or noise.

## Scales

1. I had SendCutSend produce my scale tops.  You can use the [9in Scale Platform](STEP/9in%20Scale%20Platform.step) file to get a set.  I did not have them tap the holes, but you may opt to have them do so.  I went with 1/8" Stainless Steel for mine.  Another option is to print a set of tops.  If you opt to print a set of tops, you'll need to use M3x4x5mm heat inserts which are not included in the BoM.  I recommend ABS.
2. If you opted for the SendCutSend plates and did not also opt for the tapping service, you will need to tap each of the holes with M3 or M4 taps.  Each top should have 8 M3 threaded holes, and a single M4 threaded hole.
3. Next, print (or get printed) 8 each of the Sensor Mount and Sensor Support as well as 4 of the Support Legs.
4. When opening the load cells, they should be paired and have similar numbers written on them.  Be sure to keep the paired cells together for each scale.  For each cell, create a sandwich with the mount, the cell, and the support.  Attach it to the scale top with the M3 screws.
5. For wiring, crimp together the White and Black of opposite cells to a single pin.  This should result in four pins for the SL connector.  Pin 1 (Cell 1 White, Cell 2 Black), Pin 2 (Cell 1 Black, Cell 2 White), Pin 3 (Cell 1 Red), and Pin 4 (Cell 2 Red).  Pin 1 will be your E+, Pin 2 is E-, Pin 3 to A+, and Pin 4 to A-.
6. Attach the support leg to the top with one of the M4 screws.  Use a small zip-tie to secure the wires from the load cells.   Don't pull them fully tight.
![Scales Built](images/scale-connections.png)

## Home Assistant Setup

There's a few "phases" to get the device up and running with Home Assistant.

1. In Home Assistant, go to Settings -> Devices & Services -> Helpers
2. Create the Helpers for the following:
    1. Keg 1 Tare (kg)
    2. Keg 2 Tare (kg)
    3. Keg 3 Tare (kg)
    4. Keg 4 Tare (kg)
3. Make sure ESPHome is installed and working.
4. Using a paperclip or something similar, depress the boot button on the ESP32 and hold it while it's plugged into the computer.
5. From the ESPHome add a New Device.  ESPHome should detect the device type automatically.
6. In the YAML editor, update the first few lines to be as follows

    ```yaml
    esphome:
      name: <device-name>
      friendly_name: <Device Friendly Name>
      on_boot:
        priority: -100.0
        then:
          - light.turn_on:
              id: onboard_led
              brightness: 100%
              red: 0%
              green: 100%
              blue: 0%
              transition_length: 0s
          - delay: 2s
          - light.turn_off: onboard_led

    esp32:
      board: esp32-s3-devkitc-1
      variant: ESP32S3
      framework:
        type: esp-idf

    psram:
      mode: quad
      speed: 80MHz
    ```

    The important part is to update the framework to use esp-idf instead of arduino.  

> [!CAUTION]
> Note, that the above assumes that the board is the exact same one in the BoM.  If it's different, confirm the settings and adjust as nessecary.  The psram section may need to be altered or ommitted entirely.

7. Upload the first batch of firmware and make sure the device returns logs.
8. Edit the yaml again and add the following after the `captive_portal:` section.

    ```yaml
    time:
      - platform: homeassistant
        id: update_timer
        on_time: 
          - seconds: 0,10,20,30,40,50
            minutes: /1
            then:
              - light.turn_on:
                  id: onboard_led
                  brightness: 100%
                  red: 0%
                  green: 0%
                  blue: 100%
                  transition_length: 0s
              - component.update: scale_one_raw
              - light.turn_off: onboard_led
          - seconds: 2,12,22,32,42,52
            minutes: /1
            then:
              - light.turn_on:
                  id: onboard_led
                  brightness: 100%
                  red: 0%
                  green: 0%
                  blue: 100%
                  transition_length: 0s
              - component.update: scale_two_raw
              - light.turn_off: onboard_led
          - seconds: 4,14,24,34,44,54
            minutes: /1
            then:
              - light.turn_on:
                  id: onboard_led
                  brightness: 100%
                  red: 0%
                  green: 0%
                  blue: 100%
                  transition_length: 0s
              - component.update: scale_three_raw
              - light.turn_off: onboard_led
          - seconds: 6,16,26,36,46,56
            minutes: /1
            then:
              - light.turn_on:
                  id: onboard_led
                  brightness: 100%
                  red: 0%
                  green: 0%
                  blue: 100%
                  transition_length: 0s
              - component.update: scale_four_raw
              - light.turn_off: onboard_led
          - seconds: 8,18,28,38,48,58
            minutes: /1
            then:
              - light.turn_on:
                  id: onboard_led
                  brightness: 100%
                  red: 0%
                  green: 0%
                  blue: 100%
                  transition_length: 0s
              - component.update: scale_co2_raw
              - light.turn_off: onboard_led

    light:
      - platform: esp32_rmt_led_strip
        rgb_order: GRB
        pin: 48
        num_leds: 1
        rmt_channel: 0
        chipset: WS2812
        name: "Onboard LED"
        id: onboard_led
        
    #####################
    # Beer Drain Sensor #
    #####################
    binary_sensor:
      - platform: gpio
        pin:
          number: 9
          inverted: true
          mode:
            input: true
            pullup: true
        id: beer_drain_full
        name: "Beer Drain Full"

    ###############################
    # Scales and Pressure Sensors #
    ###############################
    sensor:
      ######################
      # Diagnostic Sensors #
      ######################
      - platform: wifi_signal
        name: "WiFi Signal dB"
        id: wifi_signal_db
        update_interval: 60s
        entity_category: "diagnostic"
        unit_of_measurement: dBm
      - platform: copy
        source_id: wifi_signal_db
        name: "WiFi Signal Strength"
        id: wifi_signal_strength
        filters:
          - lambda: return (((90.0 - abs(x)) / 60.0) * 100.0);
        unit_of_measurement: "Signal %"
        entity_category: "diagnostic"
      #########
      # Keg 1 #
      #########
      - platform: homeassistant
        entity_id: input_number.keg_1_tare_kg
        id: keg_1_tare_kg
        name: "Keg 1 Tare (Kg)"
        internal: True
        accuracy_decimals: 3
      - platform: hx711
        clk_pin: 5
        dout_pin: 4
        gain: 64
        filters:
          - median: 
              window_size: 3
              send_every: 3
              send_first_at: 3  
        id: scale_one_raw
        update_interval: never
        name: "Scale One Raw"
      - platform: copy
        source_id: scale_one_raw
        unit_of_measurement: kg
        filters:
          - calibrate_linear:
            - 49135 -> 0.0
            - -83849 -> 10.002
          - lambda: return x - id(keg_1_tare_kg).state;
        accuracy_decimals: 2
        id: scale_one_kg
        name: "Scale One Kg"
      - platform: copy
        source_id: scale_one_kg
        unit_of_measurement: Oz
        filters:
          - multiply: 33.814
        id: scale_one_oz
        name: "Scale One Remaining Beer (Oz)"
      #########
      # Keg 2 #
      #########
      - platform: homeassistant
        entity_id: input_number.keg_2_tare_kg
        id: keg_2_tare_kg
        name: "Keg 2 Tare (Kg)"
        internal: True
        accuracy_decimals: 3
      - platform: hx711
        clk_pin: 7
        dout_pin: 6
        gain: 64
        filters:
          - median: 
              window_size: 3
              send_every: 3
              send_first_at: 3  
        id: scale_two_raw
        update_interval: never
        name: "Scale Two Raw"
      - platform: copy
        source_id: scale_two_raw
        unit_of_measurement: kg
        filters:
          - calibrate_linear:
            - -33834 -> 0.0
            - 115053 -> 10.002
          - lambda: return x - id(keg_2_tare_kg).state;
        accuracy_decimals: 2
        id: scale_two_kg
        name: "Scale Two Kg"
      - platform: copy
        source_id: scale_two_kg
        unit_of_measurement: Oz
        filters:
          - multiply: 33.814
        id: scale_two_oz
        name: "Scale Two Remaining Beer (Oz)"
      #########
      # Keg 3 #
      #########
      - platform: homeassistant
        entity_id: input_number.keg_3_tare_kg
        id: keg_3_tare_kg
        name: "Keg 3 Tare (Kg)"
        internal: True
        accuracy_decimals: 3
      - platform: hx711
        clk_pin: 16
        dout_pin: 15
        gain: 64
        filters:
          - median: 
              window_size: 3
              send_every: 3
              send_first_at: 3  
        id: scale_three_raw
        update_interval: never
        name: "Scale Three Raw"
      - platform: copy
        source_id: scale_three_raw
        unit_of_measurement: kg
        filters:
          - calibrate_linear:
            - 281137 -> 0.0
            - 425363 -> 10.002
          - lambda: return x - id(keg_3_tare_kg).state;
        accuracy_decimals: 2
        id: scale_three_kg
        name: "Scale Three Kg"
      - platform: copy
        source_id: scale_three_kg
        unit_of_measurement: Oz
        filters:
          - multiply: 33.814
        id: scale_three_oz
        name: "Scale Three Remaining Beer (Oz)"
      #########
      # Keg 4 #
      #########
      - platform: homeassistant
        entity_id: input_number.keg_4_tare_kg
        id: keg_4_tare_kg
        name: "Keg 4 Tare (Kg)"
        internal: True
        accuracy_decimals: 3
      - platform: hx711
        clk_pin: 18
        dout_pin: 17
        gain: 64
        filters:
          - median: 
              window_size: 3
              send_every: 3
              send_first_at: 3  
        id: scale_four_raw
        update_interval: never
        name: "Scale Four Raw"
      - platform: copy
        source_id: scale_four_raw
        unit_of_measurement: kg
        filters:
          - calibrate_linear:
            - -140124 -> 0.0
            - -286031 -> 10.002
          - lambda: return x - id(keg_4_tare_kg).state;
        accuracy_decimals: 2
        id: scale_four_kg
        name: "Scale Four Kg"
      - platform: copy
        source_id: scale_four_kg
        unit_of_measurement: Oz
        filters:
          - multiply: 33.814
        id: scale_four_oz
        name: "Scale Four Remaining Beer (Oz)"
    ```

> [!NOTE]
> You can name the helpers in step 2 whatever you like.  Be sure to update the yaml file with the correct device id of the helpers that you create.

9. Upload the new firmware and watch the logs.  The scales should all be connected and should start reporting values.
10. Allow each sensor to rest for a bit with no weight on the scale.  Go to Settings -> Devices -> ESPHome -> <Your Device>.  View the raw values for each scale and note the current values.  Depending on the gain, you may need to take a median or average of a few readings.
    
    ![Scale Raw Example](images/scale-raw.png)

11. Add a known weight onto one of the scales and let it rest for 15-20 minutes.  This will allow enough datapoints to account for noise.  I used 10kg for mine.  A full keg would be even better so that we can calibrate both ends of the measurement range.  Regardless, ensure you know the weight of the object on the scale down to at least 0.02kg.  This level of precision will allow us to measure roughly a one ounce pour.
12. Once values for zero and the known weight for each scale has been obtained, go back and edit the yaml.  Update the `scale_x_kg` filters with the new raw values and expected values.

    ```yaml
    filters:
      - calibrate_linear:
        - 49135 -> 0.0
        - -83849 -> 10.002
    ```

13. The scales should be all set and can be used to build dashboards

    ![HA Dashboard Example](images/tap-example.png)

14. They can also now be used to feed other things such as live updating tap handles:

    ![Connected Tap Handles](images/tap-handles.png)
