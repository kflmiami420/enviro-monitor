# Config File Description
The config.json file is used to set the Enviro Monitor’s configuration. It has the following keys:

"version”: The config file’s version. Provides the ability to automate config updates

"temp_offset": Optional ability to provide a fixed temperature offset in degrees Celsius

"altitude": Sets the altitude in meters to perform air pressure compensation

"enable_display": Set to false if the optional weather cover is used, otherwise set to true

"enable_adafruit_io": Set to true to enable Adafruit IO feeds, otherwise set to false

"aio_user_name": Sets the Adafruit IO User Name. Set to “” if Adafruit Io is not enabled

"aio_key": Sets the Adafruit IO User Key. Set to “” if Adafruit IO is not enabled 

"aio_feed_window": Sets the Adafruit IO Feed Window (see Adafruit IO Support). Set to 0 if Adafruit IO is not enabled

"aio_feed_sequence": Sets the Adafruit IO Feed Sequence (see Adafruit IO Support). Set to 0 if Adafruit IO is not enabled

"aio_household_prefix": Sets the Adafruit IO Household Prefix (see Adafruit IO Support). Set to “” if Adafruit IO is not enabled

"aio_location_prefix": Sets the Adafruit IO Location Prefix (see Adafruit IO Support). Set to “” if Adafruit IO is not enabled

"aio_package": Sets the Adafruit IO Package (see Adafruit IO Support). Set to “” if Adafruit IO is not enabled

"enable_send_data_to_homemanager": Enables sending of mqtt Home Automation Data if set to true, otherwise set to false

"enable_receive_data_from_homemanager": Enables reception of mqtt Home Automation Data if set to true. Allows the use of external temp/hum and air pressure sensors, otherwise set to false

"enable_indoor_outdoor_functionality": Enables an Indoor and an Outdoor Enviro Monitor in the same household to communicate with each other via mqtt messages when set to true, otherwise set to false

"mqtt_broker_name": Sets the host name of the mqtt broker if mqtt messages are used for Home Automation and/or indoor/outdoor functionality. Set to “” if no mqtt messaging is required

"enable_luftdaten": Set to true to send data to Luftdaten, otherwise set to false

"enable_climate_and_gas_logging": Set to true to log data, otherwise set to false

"enable_particle_sensor": Set to true to enable the particle sensor, otherwise set to false

"enable_eco2_tvoc": Set to true if using the optional SGP30 eCo2/TVOC sensor that creates an “Indoor Plus” variant, otherwise set to false

"gas_daily_r0_calibration_hour": Sets the hour when daily gas sensor calibration is to performed. Default is 3 (3am)

"reset_gas_sensor_calibration": Resets the gas sensor calibration data that has been retrieved from the persistent data log on start-up, when set to true. This is rarely necessary and should normally be set to false 

"incoming_temp_hum_mqtt_topic": Sets the mqtt topic for the optional external temp/hum sensor. Set to “” if an external temp/hum sensor is not used

"incoming_temp_hum_mqtt_sensor_name": Sets the optional mqtt external temp/hum sensor’s name. Set to “” if an external temp/hum sensor is not used

"incoming_barometer_mqtt_topic": ": Sets the mqtt topic for the optional external air pressure sensor. Set to “” if an external air pressure sensor is not used

"incoming_barometer_sensor_id": Sets the optional mqtt external barometer sensor’s id number. Set to 0 if an external air pressure sensor is not used

"indoor_outdoor_function": Set to "Outdoor" for an outdoor monitor and “Indoor” for an indoor monitor

"mqtt_client_name": Sets the mqtt client name for use by the mqtt broker when using mqtt messaging. Set to “” if no mqtt messaging is required

"outdoor_mqtt_topic": Sets the mqtt topic for the outdoor monitor within the household. Suggest using “Outdoor EM” if mqtt messaging is required and “” if no mqtt messaging is required

"indoor_mqtt_topic": Sets the mqtt topic for the indoor monitor within the household. Suggest using “Indoor EM” if mqtt messaging is required and “” if no mqtt messaging is required

"city_name": Sets the city name for the monitor’s installation location that will be retrieved from the Astral module’s database

"time_zone": Set the time zone for the monitor’s installation location

"custom_locations": Adds cities that are required by “city_name” and are missing from the Astral module’s database. Format is a list of strings with each string structured as:  "city_name, country, country_time_zone, latitude, longitude"
