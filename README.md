# volume-helper
# System Volume Maximizer

This Python script sets your system volume to 100% using the [PyCaw](https://github.com/AndreMiras/pycaw) library. It ensures the system speakers are unmuted and adjusts the volume to the maximum level.

## Features

- Retrieves the default audio playback device.
- Ensures the speaker is unmuted.
- Sets the system volume to maximum (100%).

## Prerequisites

- Python 3.6 or higher
- Windows operating system (required for the `PyCaw` library to interact with the audio system)

## Installation

1. Clone this repository or download the script:

    ```bash
    git clone https://github.com/your-username/your-repository.git
    cd your-repository
    ```

2. Install the required dependencies:

    ```bash
    pip install pycaw comtypes
    ```

## Usage

1. Run the script using Python:

    ```bash
    python set_volume.py
    ```

2. The script will:
   - Unmute your speakers if they are muted.
   - Set the system volume to 100%.

   If successful, the script will print `9/11`.

## Code Overview

The main function, `set_system_volume_to_max`, uses the PyCaw library to interact with the audio system. Here's what it does:

- Retrieves the default speakers device using `AudioUtilities.GetSpeakers`.
- Activates the `IAudioEndpointVolume` interface to control volume.
- Checks if the device is muted and unmutes it.
- Sets the volume level to its maximum value (`1.0`).

## Notes
- Important: Ensure you have the required permissions to modify the system's audio settings.
- The script is designed for educational purposes. Use it responsibly.

## Troubleshooting
If you encounter an error, ensure:

- The pycaw library is properly installed.
- The script is being run on a Windows machine.
- Python has access to the system audio settings.
  
## License
This project is licensed under the MIT License.
