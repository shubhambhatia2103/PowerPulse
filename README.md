# Laptop Battery Percentage Monitor

This project provides a Python script that displays the battery percentage of a laptop, along with other battery-related information such as whether the power is plugged in and the estimated time left before the battery runs out.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Output Example](#output-example)
- [Explanation](#explanation)
- [Contributing](#contributing)

## Installation

### Windows

Install the `psutil` library using `pip`:

```bash
pip install psutil
```

### Linux
Install psutil with the following commands:

```bash
sudo apt-get install gcc python3-dev
sudo pip3 install psutil
```

### Usage
Run the script to display battery details:

```bash
python battery_percentage.py

```

### Output Example
When you run the script, you might see output similar to the following:

```bash
Battery percentage :  57
Power plugged in :  False
Battery left :  1:58:32
``` 

## battery_percentage.py Content
Here is the Python script that shows the laptop battery percentage and other related information:

```bash
# Python script showing battery details
import psutil

# Function returning time in hh:mm:ss format
def convertTime(seconds):
    minutes, seconds = divmod(seconds, 60)
    hours, minutes = divmod(minutes, 60)
    return "%d:%02d:%02d" % (hours, minutes, seconds)

# Returns a tuple containing battery information
battery = psutil.sensors_battery()

print("Battery percentage: ", battery.percent)
print("Power plugged in: ", battery.power_plugged)

# Converting seconds to hh:mm:ss format
print("Battery left: ", convertTime(battery.secsleft))

``` 
