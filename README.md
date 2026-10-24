# Laboratory Activity 9: ESP32 Wi-Fi Manager

Name: Abigil Queen Casas

Assigned Number: 2024-2088


## Results Table

| Task | What I did | What I observed |
|---|---|---|
| 1. Wrong password | Entered a wrong password on the setup page. | The ESP32 failed to connect to the network, and the setup page stayed available so the correct password could be entered again. The board did not get stuck. |
| 2. Reset settings | Held the BOOT button for 3 seconds while the board was running. | The saved Wi-Fi settings were erased, the board restarted, and the `BCA188-ESP32-2024-2088` setup network appeared again in the phone's Wi-Fi list. |
| 3. Change the name | Changed the network name in the code, uploaded it, and checked the phone's Wi-Fi list. | The new network name appeared in the Wi-Fi list, and the old name was no longer shown. |
| 4. Different network | Reset the board, then connected it to my phone hotspot through the setup page. | The ESP32 connected to the phone hotspot successfully and the Serial Monitor showed a new IP address, without any change to the code. |

# Screenshots

## 1. Setup page on my phone

<img width="720" height="1604" alt="image" src="https://github.com/user-attachments/assets/805fe5c7-26a7-40db-9e80-fa03fba26c3e" />
<img width="720" height="1604" alt="image" src="https://github.com/user-attachments/assets/e13cf2e6-ea5f-4ec9-ba2d-b9c427518d6b" />


2. Serial Monitor showing a connected state with an IP address

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e8ec468b-f156-44b4-b5bc-f14b3352e1b2" />


## Why did the board connect to a different network without a code change?

WiFiManager saves the Wi-Fi name and password entered on the setup page in the ESP32's flash memory instead of hardcoding them in the sketch, so the network can be changed at runtime through the setup page without editing or re-uploading the code.
