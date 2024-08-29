# Laptop Battery Percentage Monitor

This project provides a Python script that displays the battery percentage of a laptop, along with other battery-related information such as whether the power is plugged in and the estimated time left before the battery runs out.



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

## Usage
Run the script to display battery details:

```bash
python battery_percentage.py

```

## Output Example
When you run the script, you might see output similar to the following:

```bash
Battery percentage :  57
Power plugged in :  False
Battery left :  1:58:32
``` 

 

## Explanation

The `psutil` library is a cross-platform library for retrieving information on running processes and system utilization (CPU, memory, disks, networks, sensors) in Python. This script uses `psutil.sensors_battery()` to get battery details:

- **percent**: Power left in percentage.
- **secsleft**: Approximate seconds left before the power runs out. It is set to `psutil.POWER_TIME_UNLIMITED` if it is on charging. If this value can’t be determined, it is set to `psutil.POWER_TIME_UNKNOWN`.
- **power_plugged**: `True` if power is plugged in, `False` if it isn’t charging, or `None` if it can’t be determined.

