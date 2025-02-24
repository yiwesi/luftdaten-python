Fork from https://github.com/corny/luftdaten-python

Restructured Skript, added Socket to provide data to own local Homepage and added upload to openSenseMap

Configuration and systemd unit not needed. Run it with "nohup python3 main.py &"

New Dependencies: A Webserver
Put the index.php in the www-document location or use the socket api to include the values in your existing webpage.

# dusty-python

Python 3 program for the [luftdaten.info](http://luftdaten.info/) sensor network.


## Supported Hardware

* [Nova Fitness SDS011](http://aqicn.org/sensor/sds011/) or compatible connected via `ttyUSB` for dust
* [Bosch BME 2280](https://www.bosch-sensortec.com/bst/products/all_products/bme280) connected via I²C for temperature, humidity and pressure


## Used libraries

* https://gitlab.com/frankrich/sds011_particle_sensor
* https://github.com/adafruit/Adafruit_Python_BME280


## Dependencies

    apt install python3-numpy python3-requests python3-yaml python3-serial

You also need to install [Adafruit_Python_BME280](https://github.com/adafruit/Adafruit_Python_BME280):

    apt-get update
    apt-get install build-essential python-pip python-dev python-smbus git
    git clone https://github.com/adafruit/Adafruit_Python_GPIO.git
    cd Adafruit_Python_GPIO
    python3 setup.py install


## Configuration

Copy the `config.yml.default` to `config.yml` and adjust the settings.


## Running a systemd unit

Take a look at the [dusty.unit](contrib/dusty.unit).
