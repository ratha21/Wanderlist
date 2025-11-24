🌍 WanderList

A modern travel planning & expense-tracking Android app built with Jetpack Compose, Room, and MVVM architecture.

✨ Overview

WanderList is a clean, modern, and feature-rich mobile app designed to help travellers organise their itinerary, manage bookings, track expenses, and view real-time exchange rates — all inside a smooth, animated UI.

This project was developed for my CP3406 mobile development assignment, following clean architecture, MVVM, StateFlow, and Jetpack Compose best practices.

🎥 Promotional Video

👉 3–5 minute demo showcasing UI, features, animations, API usage, and navigation.
(Insert your YouTube / Google Drive video link here.)

📱 Core Features
🏠 1. Home Screen

Animated entry transitions

Quick access to major features

Clean Material 3 design

📅 2. Itinerary Management

Add and store bookings locally

Displays flights, stays, and activities

Auto-updating list using Room + Flow

Beautiful card-based layout

➕ 3. Add Booking

Add a destination, date, and notes

Stored persistently in Room

Real-time UI update (no refresh needed)

💸 4. Expenses + Live Exchange Rate

Real-time EUR → SGD exchange rate

API fetched from exchangerate.host

Loading animation + error handling

Material 3 cards with smooth transitions

⚙️ 5. Settings

Dark mode toggle (demo feature)

Refresh exchange rate

Animated visibility + scaling transitions

🏗️ Architecture

WanderList follows a clean MVVM architecture:

UI (Jetpack Compose)
        ↓
ViewModel (StateFlow, business logic)
        ↓
Repository (API + Room)
        ↓
Local Database (Room)

✔ Tech Stack

Kotlin

Jetpack Compose

Material 3

Room Database

StateFlow + Coroutines

Navigation Compose

MVVM Architecture

REST API Integration

🛠️ Project Structure
com.ratha.wanderlist
│
├── data
│   ├── local
│   │   ├── TravelDao
│   │   ├── TravelDatabase
│   │   ├── BookingEntity
│   │   └── ExpenseEntity
│   └── remote
│       └── ExchangeRateApi
│
├── repository
│   └── TravelRepository
│
├── ui
│   ├── screens
│   │   ├── HomeScreen
│   │   ├── ItineraryScreen
│   │   ├── AddBookingScreen
│   │   ├── ExpensesScreen
│   │   └── SettingsScreen
│   ├── navigation
│   │   ├── Screen
│   │   └── WanderListNavHost
│   └── theme
│
├── ui.viewmodel
│   ├── TravelViewModel
│   └── TravelViewModelFactory
│
└── MainActivity.kt

🌐 API Integration

The app uses the ExchangeRate Host API:

https://api.exchangerate.host/latest?base=EUR&symbols=SGD


Fetched inside the repository using HttpURLConnection + Coroutines.

💾 Local Database

Room handles all persistent booking data:

BookingEntity – destination, date, notes

DAO returns a Flow<List<BookingEntity>>

Compose UI updates automatically when the database changes

🎨 UI/UX Design

Material You color scheme

Animated bottom navigation icons

Fade + slide transitions

Card-based layout with rounded shapes

Responsive, clean, professional design

🧪 Testing

All screens and flows tested on:

Pixel Emulator API 34

Real Samsung device

Cold boot & live reload scenarios

🔄 Version Control

GitHub commits include:

UI development

Database integration

Architecture improvements

Bug fixes and crash resolutions

API changes

Navigation restructuring

(Commit regularly to show progress.)

🧠 Reflection

A full 500-word Gibbs Reflective Cycle reflection is included separately as part of the assessment.

📌 How to Run

Clone the repository

Open in Android Studio (Giraffe or newer)

Allow Gradle sync

Run on emulator or physical device

🚀 Future Improvements

Multi-currency support

More animations

Real dark-mode implementation

Expense categories & charts

Cloud sync with Firebase
