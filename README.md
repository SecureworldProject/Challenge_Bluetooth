# Challenge_Bluetooth

This challenge checks if a device is located nearby the pc. The challenge returns the 'name+MAC' address of the target device if it is near and 0000 otherwise.

This allows to control if the PC is close to a specific device for security reasons. For example, it could monitor if an employee is next to a fixed device at the office or any other specific location, or if he is carrying a security device with him.

It uses bluetooth, in particular `pybluez` library.

## Install pybluez in Windows 10

First, install [Windows SDK](https://developer.microsoft.com/en-us/windows/downloads/windows-sdk/)

Second, download and install windows 10 [build tools](https://www.microsoft.com/es-ES/download/confirmation.aspx?id=48159)

Third, Clone [pybluez repo](https://github.com/pybluez/pybluez)

Fourth, run as administrator, within the repo: `python setup.py install`

