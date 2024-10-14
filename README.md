# SIA Scraper - Universidad Nacional de Colombia

## Overview

SIA Scraper is a Python-based project designed to automate the process of checking the availability of seats (quotas) in specific subjects offered by the Universidad Nacional de Colombia through its SIA platform -"Buscador de cursos". This tool is helpful for students who want to monitor seat availability in their desired courses and receive timely updates without manually checking the SIA website.

## Features

- **Automated Seat Availability Checks**: Automatically scrapes the SIA platform to check if a specific subject has available quotas.
- **Real-time Monitoring**: Runs regularly to monitor seat changes in real-time.
- **Subject Tracking**: Allows the user to specify which subjects to follow and monitors them for updates.
- **Notifications (future feature)**: Can be extended to send notifications

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/norjuelas/siaScraping.git
    cd sia-scraper
    ```

2. Install required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

1. **Edit the configuration file**: 
    Update the `subjects_to_follow.json` file with the subjects you want to track. Each subject should have the course code, name, and additional details you may need to identify it.

2. **Run the scraper**:
   To start the scraper, use the following command:
    ```bash
    python sia_scraper.py
    ```

3. **Optional - Set up a scheduler**: 
    You can automate the scraper to run at regular intervals using tools like `cron` on Linux or Task Scheduler on Windows.

## Example Output

The script will output a log of the subjects being tracked and whether seats are available:

```
Checking availability for course: MATH001
No available quota for MATH001.

Checking availability for course: PHYS101
Quota available for PHYS101: 5 seats left!
```

## Configuration

You can customize the scraper to your needs by editing the configuration files:

- **subjects_to_follow.json**: This file holds the information about the subjects you wish to monitor. You can add course codes and names here.
  
- **.env**: This file stores sensitive data, like your SIA login credentials, and any API keys if you're using notification services.

## Requirements

- Python 3.8 or higher
- Selenium (for web scraping)

## Future Improvements

- Add support for notifications via email or SMS.
  
## Contributing

If you'd like to contribute to this project, feel free to fork the repository and submit a pull request with your improvements.
