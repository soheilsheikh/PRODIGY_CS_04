#PRODIGY_CS_04

### Cybersecurity Monitoring and Reporting Tool

**Introduction:**
This program aims to develop a comprehensive cybersecurity monitoring and reporting tool that collects various system activities and sends encrypted reports via email. It includes features such as keylogging, system information gathering, clipboard monitoring, audio recording, screenshot capture, and secure file encryption before transmission.

**Features and Functionality:**

1. **Keylogging:**
   - Monitors keystrokes and saves them to a file (`key_log.txt`). This helps in capturing user input which can be crucial for security audits and forensic investigations.

2. **System Information Gathering:**
   - Retrieves system details (`syseminfo.txt`) including hostname, IP addresses (public and private), processor information, operating system details, and machine architecture. This information provides insights into the system's configuration and potential vulnerabilities.

3. **Clipboard Monitoring:**
   - Captures clipboard contents (`clipboard.txt`) to track copied data. This can reveal sensitive information such as passwords or confidential messages.

4. **Audio Recording:**
   - Records audio (`audio.wav`) from the microphone for a specified duration. This feature aids in capturing ambient sound or potential conversations in the vicinity of the monitored system.

5. **Screenshot Capture:**
   - Takes screenshots (`screenshot.png`) of the desktop. This visual data helps in understanding user activities and the system's operational context.

6. **Email Reporting:**
   - Encrypts and sends collected data securely via email using SMTP. This ensures that sensitive information is protected during transmission (`e_key_log.txt`, `e_systeminfo.txt`, `e_clipboard.txt`).

7. **Encryption:**
   - Uses symmetric encryption (Fernet encryption from the `cryptography` library) to secure collected files (`system_information`, `clipboard_information`, `keys_information`). Encrypted files are sent as attachments to mitigate unauthorized access during transit.

8. **Operational Control:**
   - Allows configuration of email credentials (`email_address` and `password`), recipient address (`toaddr`), file paths (`file_path`), and encryption key (`key`) for customization and operational control.

9. **Automated Execution:**
   - Implements a time-based iteration loop to execute monitoring activities at specified intervals (`time_iteration` and `number_of_iterations_end`). This ensures continuous data collection and reporting over extended periods.

10. **Cleanup Mechanism:**
    - Deletes temporary files (`system_information`, `clipboard_information`, `keys_information`, `screenshot_information`, `audio_information`) after successful transmission to maintain operational stealth and minimize traces.

**Conclusion:**
This cybersecurity monitoring and reporting tool provides a robust mechanism for capturing, encrypting, and transmitting critical system activities for security analysis. It serves as a proactive measure against potential threats and unauthorized activities, making it suitable for both educational purposes and real-world cybersecurity applications. By integrating multiple monitoring techniques and encryption methods, it ensures data integrity and confidentiality throughout the monitoring and reporting process.
