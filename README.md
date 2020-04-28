# Kitsos-Hassio

This is my setup for the Home Assistant (configuration & automations).

## Devices / Integrations (configuration.yaml)

The devices / integrations that are configured in my Home Assistant are the following:

- Text-to-speech: Used to make Home Assistant talk.
- Date & Time: Used to configure automations based on date & time.
- OASA: A telematics platform for Athens' bus schedule. It is used to track my favourite route.
- Yeelight: A smart light solution by Xiaomi.
- Xiaomi Gateway: A smart home solution with extra sensors (temp, humid, door, motion, light).
- Xiaomi router: It is used to track devices locations (home or away).
- Xiaomi appliances: Smart home devices like a fan, a vacuum cleaner and an IR remote controller.
- Vacuum workdays / holidays: It is an identifier of working days and holidays. It is used as a scheduler for the vacuum.

Exact device links: coming soon...

### How to use it

Just copy the sections you need and paste them in your configuration.yaml file. You will need to change the IP addresses with your own.

## Automations (automations.yaml)

Here you can find an automations exaple like:

### Notifications

- Welcome home: Says "welcome home" when you connect to your WiFi. It uses the router to track a smartphone. (Tracking sendor & TTS)
- It's getting cold: Shows a notification when the room temperature drops under 19 degrees Celcius. (Τemperature sensor)

### Lights & sensors

- Lights on at night: Turns on the lights 30 mins before sunset. (Sun sensor)
- Lights off night-light: Turns off the night-light on sunrise. (Sun sensor)
- Lights on on movement: Turns on the lights on movement. (Motion sensor)
- Lights off on movement: Turns off the lights if there's no movement. (Motion sensor)
- Yes movie lights: Turns the lights blue when Chromecast is on playing mode after sunset. (Sun sensor & media player condition)
- No movie lights: Turns the lights yellow when Chromecast stops playing after sunset. (Sun sensor & media player condition)

### Switches

- Normal lights on 90 degrees cube: Turns normal lights on when Xiaomi cube flips 90 degrees. (Xiaomi magic cube)
- Movie lights on 180 degrees cube: Turns movie lights on when Xiaomi cube flips 180 degrees. (Xiaomi magic cube)
- Toggle lights with switch (single press): Toggles a light with single press on switch. (Xiaomi wall/button switch)
- Toggle lights with switch (double press): Toggles a light with double press on switch. (Xiaomi wall/button switch)

### Time based

- Turn on fan every day: Turns on the fan in an exact time. (Time condition)
- Turn off fan every day: Turns off the fan in an exact time. (Time condition)
- Vaccum scheduled cleanup: Vacuum cleans up every Tuesday and Friday at 10:00 and notifies about it. (Time condition & workday sensor)

### How to use it

You need to change the entity_id of each device in order to match your own.
