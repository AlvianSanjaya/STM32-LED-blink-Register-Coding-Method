# STM32 LED Blink — Register Coding Method

This repository contains a **bare-metal STM32 project** that blinks an LED on an STM32F446RET6 microcontroller by directly manipulating hardware registers — *without using HAL or CubeMX*.  
It’s designed for developers who want to understand how the MCU really works at the hardware level.

---

## 🚀 Why This Project Matters

- Shows how to control GPIO registers directly
- Demonstrates basic clock setup and digital output toggling
- Perfect for learners leveling up from HAL to **register-level programming**
- Explains the fundamentals behind what HAL does under the hood

---

## 📦 Repository Structure

```

STM32-LED-blink-Register-Coding-Method/
├── Core/
│   ├── Inc/              → Header files
│   └── Src/              → Source files
├── Drivers/              → CMSIS and startup code
├── Startup/              → Reset and interrupt vectors
├── STM32F446RETX_FLASH.ld→ Linker script
├── STM32F446RETX_RAM.ld  → RAM layout
├── .project              → IDE project settings
├── .cproject             → Compiler/build settings
├── .gitignore            → Ignored build outputs

````

> We don’t check in build artifacts like `Debug/` to keep the repo clean and portable.

---

## 🛠️ How to Build & Run

### 1. Clone the repository
```bash
git clone https://github.com/DanielRajChristeen/STM32-LED-blink-Register-Coding-Method.git
cd STM32-LED-blink-Register-Coding-Method
````

### 2. Open in STM32CubeIDE

* Open **STM32CubeIDE**
* **File → Import → Existing Projects into Workspace**
* Select this directory

> Even though this project is register-level, CubeIDE still provides the build system and debugger.

### 3. Build the project

* Click the **hammer icon** (Build)
* Confirm there are no errors

### 4. Flash to your board

* Connect the STM32 board via ST-Link
* Click **Run → Debug** or **Run → Run**
* The LED should blink!

---

## 🧠 What You Learn Here

This project teaches:

* GPIO configuration *without* HAL abstractions
* Register writes to enable clocks and set pin modes
* Why startup code and vector tables matter
* How bare-metal firmware is structured

This is the real firmware root-cause learning experience.

---

## 🧩 Key Code Concepts

In `main.c`, you’ll see:

* Enabling peripheral clocks (RCC register magic)
* Setting GPIO modes using registers
* Creating simple delay loops

👉 This is the foundation of embedded software engineering.

---

## 📌 Notes & Tips

* Register programming is powerful but less portable than HAL
* Use the datasheet and reference manual — they’re your best friends
* Blink delays here are *blocking* — suitable for demos, not production multitasking

---

## 📜 License

This code is open-source. Learn from it, remix it, reuse it!

---

## ❤️ Acknowledgements

Inspired by STM32 reference manuals and embedded learning walkthroughs.

Happy hardware hacking! ⚡
