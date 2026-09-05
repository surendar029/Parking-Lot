# Parking Lot System

## Description

A thread-safe, concurrency-focused **Parking Lot Management System** built with **Java 17**, designed to demonstrate scalable object-oriented design and safe resource allocation under concurrent vehicle entry and exit operations.
The system uses **`ConcurrentHashMap`**, **`AtomicBoolean`**, and **spot-level synchronized locking** to prevent race conditions and double allocation of parking spaces. A TOCTOU-safe retry mechanism ensures reliable spot assignment even when multiple vehicles attempt to park concurrently. The architecture applies established **Singleton, Strategy, Factory, and Builder design patterns** for centralized lot management, flexible fee/payment strategies, vehicle creation, and fluent configuration. UUID-based ticket generation provides unique parking session identification.

## Key Features

* **Thread-Safe Parking Allocation**: Concurrent vehicle requests are handled safely using `AtomicBoolean` and synchronized spot-level locking.
* **Race Condition Prevention**: TOCTOU-safe retry logic prevents multiple vehicles from acquiring the same parking spot.
* **Concurrent Data Structures**: `ConcurrentHashMap` enables efficient thread-safe management of parking resources.
* **Extensible Fee Strategy**: Strategy Pattern separates parking fee calculation and payment logic from core parking operations.
* **Vehicle Factory**: Factory Pattern centralizes vehicle creation and supports different vehicle types.
* **Singleton Parking Manager**: Double-checked locking provides a single parking-lot instance while maintaining thread safety.
* **Fluent Configuration**: Builder Pattern enables flexible parking-lot configuration.
* **Unique Parking Tickets**: UUID-based ticket generation provides unique identifiers for parking sessions.
* **Object-Oriented Design**: Clean separation of responsibilities using SOLID-oriented design and established design patterns.

## Tech Stack

* **Language**: Java 17
* **Concurrency**: `ConcurrentHashMap`, `AtomicBoolean`, `synchronized`, thread-safe locking
* **Design Patterns**: Singleton, Strategy, Factory, Builder
* **Data Structures**: ConcurrentHashMap, UUID
* **Build & Tools**: IntelliJ IDEA
