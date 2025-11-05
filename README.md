
## Disclaimer

This tool is intended for educational purposes and authorized security testing only. The developer is not responsible for any illegal or unauthorized use of this tool. Using this tool against individuals without their explicit consent is illegal and unethical.

**Use this software at your own risk and responsibility.**






# Spy - Information Gathering Tool

<pre>
   _____ _____ __     __
  / ____|  __ \\ \   / /
 | (___ | |__) | \\ \\_/ / 
  \\___ \\|  __/   \\   /  
  ____) | |        | |   
 |_____/|_|        |_|   
</pre>

**Version:** 1.3.2
**Developer:** Jutt Studio
**Creator:** JS

---

## Overview

**Spy** is a powerful information gathering tool built with Flask. It is designed to collect location, device, and network information, as well as capture photos from a target's device. The tool provides a variety of social engineering templates and a comprehensive admin dashboard to view the collected data.

## Features

- **Multiple Attack Templates**: Choose from various templates like "Friendship Forever", "Zoom Meeting", "Business Scam Advisory", and more.
- **Personalizable Links**: Customize templates with names, company names, or redirect URLs to make them more convincing.
- **Rich Data Collection**: Gathers device info (OS, CPU, RAM, GPU, Screen Resolution), network info (IP, ISP, Geolocation), and location data (GPS & IP-based).
- **Photo Capture**: Captures photos from the target's camera.
- **Admin Dashboard**: A secure and modern dashboard to view all collected data, including client summaries, locations on a map, and detailed reports.
- **Data Management**: Export all collected data as a zip archive or delete it securely.

## Clone the Repository

Use the following command to clone the project. Click the copy button to copy the URL.

<div style="position: relative; background-color: #2d2d2d; border-radius: 5px; padding: 15px; margin-bottom: 15px;">
    <code id="git-url" style="color: #e0e0e0; font-family: 'Fira Code', monospace;">https://github.com/Juttstodio/Spy.git</code>
    <button onclick="copyToClipboard()" style="position: absolute; top: 10px; right: 10px; background-color: #4CAF50; color: white; border: none; border-radius: 3px; padding: 5px 10px; cursor: pointer;">Copy</button>
</div>

<script>
function copyToClipboard() {
    var text = document.getElementById('git-url').innerText;
    navigator.clipboard.writeText(text).then(function() {
        alert('Copied to clipboard!');
    }, function(err) {
        alert('Could not copy text: ', err);
    });
}
</script>

## Installation

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/Juttstodio/Spy.git
    cd Spy
    ```

2.  **Install dependencies:**
    It's recommended to use a virtual environment.
    ```bash
    pip install -r requirements.txt
    ```

3.  **Set up environment variables:**
    Create a `.env` file in the root directory and add your admin credentials and email settings for lockout notifications.
    ```
    ADMIN_USERNAME=your_admin_username
    ADMIN_PASSWORD=your_secure_password
    
    # Optional: For email notifications on admin lockout
    ADMIN_EMAIL=your_email@gmail.com
    EMAIL_PASSWORD=your_gmail_app_password
    ```

## Usage

1.  **Run the application:**
    ```bash
    python spy.py
    ```

2.  **Select an attack vector:**
    Follow the command-line prompts to choose a template. If the template is personalizable, you will be asked for additional input.

3.  **Share the link:**
    The server will start and provide a local network URL (e.g., `http://192.168.1.5:5050`). Share this link with your target.

4.  **View Results:**
    Access the admin panel by navigating to `http://<your-ip>:5050/admin`. Log in with the credentials you set in the `.env` file to see the collected data.

## Disclaimer

This tool is intended for educational purposes and authorized security testing only. The developer is not responsible for any illegal or unauthorized use of this tool. Using this tool against individuals without their explicit consent is illegal and unethical.

**Use this software at your own risk and responsibility.**