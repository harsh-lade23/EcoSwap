# EcoSwap - Smart EV Battery Swapping Hub

![Flutter](https://img.shields.io/badge/Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)
![Dart](https://img.shields.io/badge/Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)
![Firebase](https://img.shields.io/badge/firebase-ffca28?style=for-the-badge&logo=firebase&logoColor=black)

> **Note:** This project is currently in active development.

EcoSwap is a cross-platform mobile application designed to streamline the battery swapping experience for Electric Vehicle (EV) drivers. The app allows users to locate nearby swapping stations, monitor real-time battery inventory, and reserve a fully charged battery before arriving at the hub.

## Features

*   **Real-Time Station Discovery:** View a dynamic list of nearby battery swapping hubs.
*   **Live Inventory Tracking:** Monitors the exact number of 100% charged batteries available at each station using real-time database synchronization.
*   **Smart Reservation System:** Users can lock in a battery reservation with a live 15-minute countdown timer, ensuring availability upon arrival.
*   **Reactive UI:** Built with Flutter's declarative UI framework for a smooth, responsive, and cross-platform user experience.

## Tech Stack & Architecture

*   **Frontend:** Flutter & Dart
*   **Backend / BaaS:** Firebase Firestore (NoSQL Document Database)
*   **State Management & Architecture:** 
    *   Utilizing **Clean Architecture** principles to separate the UI layer from the domain and data layers.
    *   Asynchronous state handling utilizing Dart `Stream` and `Future` APIs to map real-time database snapshots directly to the UI.

## Project Structure (Planned)

```text
lib/
 ┣ data/
 ┃ ┣ models/           # Data transfer objects (Station, Reservation)
 ┃ ┗ repositories/     # Firebase Firestore implementations
 ┣ domain/
 ┃ ┗ entities/         # Core business logic models
 ┣ presentation/
 ┃ ┣ screens/          # UI Views (Home, Station Details, Active Reservation)
 ┃ ┗ widgets/          # Reusable Flutter components (StationCards, Timers)
 ┗ main.dart           # Application entry point
