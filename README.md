# Voting-Machine-using-Arduino-

## 📌 Overview

This project is an **Electronic Voting Machine (EVM)** built using **Arduino UNO, LCD display, and push buttons**.
The system allows users to vote for **four candidates (A, B, C, D)** and shows the results on the LCD screen.

When the **Result button** is pressed:

* The votes are counted.
* The candidate with the maximum votes is declared **Winner**.
* In case of equal votes, a **Tie / No Result** message is displayed.
* After results are displayed, all votes reset for the next round.

This project is a great example of **microcontroller-based embedded systems**, **decision making with Arduino**, and **real-time LCD interfacing**.

---

## 🛠️ Components Used

* Arduino UNO (or compatible board)
* 16x2 LCD Display
* 5 Push Buttons (4 for voting, 1 for result)
* Resistors (10kΩ pull-down / use Arduino’s internal pull-up)
* Breadboard & Jumper Wires

---

## ⚡ Circuit Connections

| Component  | Arduino Pin |
| ---------- | ----------- |
| LCD RS     | 13          |
| LCD EN     | 12          |
| LCD D4     | 11          |
| LCD D5     | 10          |
| LCD D6     | 9           |
| LCD D7     | 8           |
| Button A   | 7           |
| Button B   | 6           |
| Button C   | 5           |
| Button D   | 4           |
| Result Btn | 3           |

> Note: Use **internal pull-ups** (`pinMode(pin, INPUT_PULLUP)`) or connect buttons with pull-down resistors to avoid floating values.

---

## 📜 Code Explanation

* **Setup**

  * Initializes LCD and pins.
  * Displays project title for 4 seconds.
  * Shows candidate labels (A, B, C, D) on the LCD.

* **Loop**

  * Continuously displays vote count for each candidate.
  * If a button is pressed, corresponding candidate’s vote is incremented.
  * If the **Result button** is pressed, the system:

    * Counts votes.
    * Declares the winner.
    * Handles tie/no result cases.
    * Resets votes for next round.

---

## 📊 Example LCD Output

```
A  B  C  D
2  5  1  3
```

* If **B has the highest votes**, the LCD will display:

  ```
  B is Winner
  ```

* If no votes are given:

  ```
  No Voting....
  ```

* If votes are equal:

  ```
  Tie Up Or
  No Result
  ```

---

## 🚀 How to Run

1. Connect the circuit as per wiring table.
2. Upload the code to Arduino UNO using Arduino IDE.
3. Press the respective button to vote for a candidate.
4. Press the **Result button** to view the winner on the LCD.
5. System resets automatically after result display.

---

## 📂 Repository Structure

```
📁 Electronic-Voting-Machine
 ┣ 📜 VotingMachine.ino      # Arduino Source Code
 ┣ 📜 README.md              # Documentation (this file)
 ┣ 📁 images/                # Circuit diagram & LCD screenshots
 ┣ 📜 LICENSE                # (Optional) Open-source license
```

---

## 🎯 Applications

* Demonstration of **digital voting** system.
* Useful for **college projects, exhibitions, and learning**.
* Can be expanded with **authentication (RFID/Biometric)** for real-world scenarios.

---

## 📌 Future Improvements

* Add **EEPROM** support to save votes after reset/power loss.
* Include **buzzer/LED indicators** for confirmation.
* Upgrade to **touchscreen TFT display** instead of push buttons.
* Implement **IoT-based remote voting** using ESP32/ESP8266.

---

## 📜 License

This project is open-source under the **MIT License**.
Feel free to use and modify for learning and academic purposes.



👉 Kapil, do you also want me to make a **circuit diagram (Fritzing style)** for the repo so that your GitHub looks professional?
