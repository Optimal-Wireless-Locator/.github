<div align="center">
  <h1>Optimal Wireless Locator (OWL)</h1>
  <p>
    <strong>An internal positioning system (IPS) of low cost and high precision, developed by students of Systems Development.</strong>
  </p>
  <p>
    <img src="https://img.shields.io/badge/Status-Academic%20Project-blue" alt="Status: Projeto Acadêmico">
    <img src="https://img.shields.io/badge/Tech-ESP32%20%7C%20BLE%20%7C%20Node.js-green" alt="Tecnologias">
    <img src="https://img.shields.io/badge/Database-MongoDB-blueviolet" alt="Banco de Dados">
  </p>
</div>

---

<div>

## 1. About The Project

**Optimal Wireless Locator (OWL)** is an academic project focused on developing an accessible, low-cost, and efficient indoor positioning system (IPS). Standard GPS signals are ineffective inside buildings, creating significant challenges for asset tracking in environments like schools, hospitals, factories, and warehouses.

This initiative was born from a direct need to enhance security at the **ETEC Bento Quirino - Maker Space** following a series of notebook thefts. Unlike expensive and complex commercial solutions, OWL leverages affordable hardware and open-source software to provide a viable, real-time tracking platform, proving its potential for application in educational institutions and other budget-constrained environments.

## 2. System Architecture

The OWL ecosystem is built on a modern, scalable stack to provide real-time location data, from hardware sensors to a web-based interface.

* **Data Collection (Hardware):** Fixed **ESP32** modules are installed at strategic points to act as receivers. They continuously scan for **Bluetooth Low Energy (BLE) tags** attached to assets.
* **Signal Processing:** Each ESP32 measures the **RSSI (Received Signal Strength Indicator)** from the tags. This signal strength is then converted into an estimated distance using a propagation model calibrated specifically for the environment.
* **Positioning Algorithm:** The system uses **Trilateration** to calculate the asset's (x, y) coordinates from at least three known reference points (the ESP32s). To refine accuracy, we utilize the **Levenberg-Marquardt** non-linear optimization algorithm (`ml-levenberg-marquardt`) to minimize the error in distance estimations.
* **Backend (Server):** A **Node.js** and **Express** server acts as the central API. It receives processed data from the ESP32s, performs the final positioning calculations, and persists the data.
* **Database:** A cloud-hosted **MongoDB Atlas** instance stores location history, sensor data, and asset information.
* **Frontend (Client):** A dynamic web interface displays the asset locations in real-time on an SVG map of the environment.
* **Firmware:** The ESP32 modules are programmed in **C++**.

## 3. Repositories

This organization hosts the different components of the OWL ecosystem.

* **[connections](https://github.com/Optimal-Wireless-Locator/connections):** Connections of OWL members.

## 4. The Team

This project is developed by students of Systems Development.

* **Jônatas Santos Gandra**
* **Leonardo Arruda Ferreira**
* **Victor de Toledo Rodrigues Silva**

</div>
