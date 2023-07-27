# Pwned Password Check

## Introduction

The Pwned Password Check is a Python script designed to help users ascertain whether their passwords have been leaked or exposed in any data breaches. This is achieved by leveraging the "Have I Been Pwned" API, a free service that aggregates data breaches and makes them searchable.

## Features

- **Password Leak Checker**: This script enables users to check if their passwords have been leaked in any known data breaches.

- **Multiple Passwords**: The script supports the checking of multiple passwords in one run.

- **Hash-based Checks**: Passwords are not sent in plain text. Instead, they are hashed using SHA1 and only the first five characters of the hash are sent to the API to retrieve potential matching hash tails.

## Getting Started

### Prerequisites

- Python 3.6 or higher
- Python's `requests` library. If not already installed, use pip to install:
    ```
    pip install requests
    ```

### Setup and Running

1. Clone this repository or download the script.

2. Store your passwords in a text file, with one password per line.

3. Open a terminal or command prompt, navigate to the location of the script and run the script along with the file name as an argument like so:
    ```
    python pwned_check.py passwords.txt
    ```

**NOTE**: The filename `passwords.txt` should be replaced with the name of your file.

## Expected Output

The script will output a message for each password, indicating whether the password has been found in the data breaches database, and if so, how many times.

Here is a sample output:

    ```
    password123 was found 4736 times, you should probably change your password
    qwerty was not found, all good
    ```

## Security

This script does not store your passwords or send them over the internet in plaintext. However, it does send the first five characters of your password's SHA1 hash to a third-party API. Please ensure you understand the security implications of this.

## Disclaimer

Please remember that it is generally not a good practice to store passwords in plaintext files, and it is highly recommended to use a password manager.
