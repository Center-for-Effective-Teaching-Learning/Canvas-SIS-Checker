# Canvas SIS Import Monitoring Script

*A Python script that automates monitoring of Canvas SIS imports, detects errors, and sends email alerts.*

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Directory Structure](#directory-structure)
- [Functions Explained](#functions-explained)
- [Customization](#customization)
- [Logging and Error Handling](#logging-and-error-handling)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)

## Overview

This script interacts with the Canvas Learning Management System (LMS) API to automate the monitoring of SIS (Student Information System) imports. It performs the following tasks:

- Retrieves recent SIS imports from Canvas.
- Checks if new imports have occurred within the last 24 hours.
- Downloads new SIS imports and their associated CSV files.
- Parses error logs to identify issues.
- Sends email notifications using SendGrid for specific events.

## Features

- **Automated Monitoring**: Periodically checks for new SIS imports without manual intervention.
- **Error Detection**: Identifies missing or incomplete data and non-enrollment errors.
- **Email Notifications**: Sends alerts for important events like missing imports or errors.
- **Data Archiving**: Stores import data and associated files locally for record-keeping.

## Prerequisites

- **Python 3.x**
- **Canvas API Access**: An API token with permissions to access SIS imports.
- **SendGrid Account**: An API key for sending emails via SendGrid.
- **Required Python Packages**:
  - `requests`
  - `pytz`
  - `sendgrid`
  - `configparser`
