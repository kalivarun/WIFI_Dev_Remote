# Remote Control Tool for NFS-2018

This project allows you to remotely control a game (NFS-2018) on a desktop connected to your LAN (local area network). The tool is divided into three main components:

1. `Remote_10.py` - A Kivy-based mobile application that serves as a remote controller.
2. `multi_server.py` - A server script that manages connections and handles commands.
3. `Client.py` - A client script that runs on the target PC, receives commands from the server, and simulates key presses.

## Features

- **Remote Control:** Control the NFS-2018 game using a mobile application.
- **LAN Connectivity:** Connect multiple devices under a LAN router.
- **Email Notification:** Automatically send the IP address of the connecting device via email.

## Getting Started

### Prerequisites

Ensure you have the following installed:

- Python 3.x
- Kivy
- PyAutoGUI
- Pydroid 3 (for running the mobile app on an Android device)
- SMTP server credentials for email functionality

### Installation

1. Clone this repository to your local machine.
2. Install the required packages using `pip`:

    ```sh
    pip install -r requirements.txt
    ```

### Running the Application

1. **Server:**
    - Run `multi_server.py` on the target PC. This script will listen for incoming connections on port 5000.
    
    ```sh
    python multi_server.py
    ```

2. **Client:**
    - Run `Client.py` on the target PC. This script will connect to the server and handle incoming commands.
    
    ```sh
    python Client.py
    ```

3. **Mobile Application:**
    - Use Pydroid 3 to run `Remote_10.py` on your Android device. Make sure the mobile device is connected to the same LAN as the target PC.
    
    ```sh
    python Remote_10.py
    ```

### Configuration

- **Email Notification:**
    - Update the `to_mail_ip_address` function in `Client.py` with your email credentials to enable IP address notifications.
    
    ```python
    sender = "your_email@gmail.com"
    sender_psd = "your_email_password"
    res = "recipient_email@gmail.com"
    ```

### Basic Instructions

- Ensure that port number 5000 is free before running the program.
- Convert `Client.py` to an executable using PyInstaller for easy deployment on the target PC:

    ```sh
    pyinstaller --onefile Client.py
    ```

- Make sure `multi_server.py` is running and online before using the mobile app.

### Notes

- This tool is specifically designed for controlling the NFS-2018 game.
- Ensure all devices are connected to the same LAN for proper functionality.

## Contributing

Contributions are welcome! Please fork this repository and submit pull requests to contribute.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements

Special thanks to the open-source community for providing the tools and libraries used in this project.

---

### Visual Representation

![App Interface](docs/app_interface.png)

The above image shows the layout of the mobile application interface. The buttons are mapped to specific game controls, allowing for a seamless gaming experience.

---

### Contact

For any inquiries or support, please contact:

- **Name:** Varun Chandra
- **Email:** k.s.varunchandra@gmail.com

Enjoy controlling NFS-2018 remotely!
