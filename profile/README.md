<div align="center">
  <h1>Optimal WirelessLocator (OWL)</h1>
  <p>
    <strong>An internal positioning system (IPS) of low cost and high precision, developed by students of Systems Development.</strong>
  </p>
  <p>
    <img src="https://img.shields.io/badge/Status-Development-blue" alt="Status: Development">
    <img src="https://img.shields.io/badge/Concept-Indoor%20Tracking-green" alt="Concept: Indoor Tracking">
    <img src="https://img.shields.io/badge/Tech-Wireless%20%7C%20BLE%20%7C%20IoT-blueviolet" alt="Technologies">
  </p>
</div>

---

<div>

## 1. About The Project

**Optimal Wireless Locator (OWL)** is a project focused on developing an accessible, low-cost, and efficient indoor positioning system (IPS). Standard GPS signals are ineffective inside buildings, creating significant challenges for asset tracking in environments like schools, hospitals, factories, and warehouses.

This initiative was born from a direct need to enhance security at the **ETEC Bento Quirino - Maker Space** following a series of notebook thefts. Unlike expensive and complex commercial solutions, OWL leverages affordable hardware and open-source software to provide a viable, real-time tracking platform, proving its potential for application in educational institutions and other budget-constrained environments.

## 2. General System Architecture

As a general concept, an Indoor Positioning System (IPS) like OWL is typically composed of several key layers. Our specific technological choices and implementations for each layer are detailed within our project repositories.

* **Sensor Layer (Hardware):** The foundation of any IPS. This layer uses fixed wireless receivers (like ESP32s) to read signals from mobile tags (like BLE beacons) attached to assets. It collects raw data, such as the Received Signal Strength Indicator (RSSI).
* **Positioning Engine (Backend):** The "brain" of the system. This layer ingests the raw sensor data and applies mathematical models (e.g., trilateration, fingerprinting, or lateration) to calculate a precise (x, y) coordinate for the asset.
* **Application Layer (API):** A server (e.g., built with Node.js) that exposes the location data to clients. It handles business logic, asset management, and user authentication.
* **Visualization Layer (Client):** A user-facing interface (typically a web or mobile app) that consumes data from the API and displays the live location of assets on a digital map of the environment.

## 3. Repositories

This organization hosts the different components of the OWL ecosystem. Specific implementation details are contained within each repository.

* **[demo-1.0](https://github.com/Optimal-Wireless-Locator/demo-1.0):** The first functional, end-to-end demonstration (v1.0) of the OWL system. This repository contains the specific implementation and source code for our v1.0 build (Server, Client, and Firmware).
* **[connections](https://github.com/Optimal-Wireless-Locator/connections):** A repository with team member profiles.

## 4. The Team

This project is developed by students of Systems Development.

* **Jônatas Santos Gandra**
* **Leonardo Arruda Ferreira**
* **Victor de Toledo Rodrigues Silva**

</div>