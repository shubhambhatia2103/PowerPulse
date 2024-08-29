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
