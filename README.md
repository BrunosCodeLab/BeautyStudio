# Beauty Studio Application ![Project Views](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2FBrunosCodeLab%2FBeautyStudio&count_bg=%235C9CFF&title_bg=%23008FC9&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)

The **Beauty Studio Application** is a mobile app developed in Flutter, designed to streamline the operations of beauty salons by providing an intuitive platform for customers to book services and for salon owners to manage their appointments efficiently.

<br>
<div align="center">
    <img src="https://raw.githubusercontent.com/BrunosCodeLab/Images/refs/heads/main/BeautyStudioApp/Interface2.png" alt="Interface1" width="720" />
</div>
<br>

## Features

### User Features
- **Service Browsing:** Explore a wide range of salon services with detailed descriptions.
- **Real-time Booking:** Book appointments with an integrated calendar and clock for personalized scheduling.
- **User Authentication:** Secure login and registration powered by Firebase Authentication.
- **Preference Storage:** Save user preferences locally with the `shared_preferences` package.

<br>
<div align="center">
    <img src="https://github.com/BrunosCodeLab/Images/blob/main/BeautyStudioApp/user_5fps.gif?raw=true" alt="gif" width="250" />
</div> 
<br>


### Admin Features
- **Booking Management:** View and manage appointments in real-time (pressing 'Done' deletes the appointment from the database).
- **User Data Management:** Access customer booking details securely.

<br>
<div align="center">
    <img src="https://github.com/BrunosCodeLab/Images/blob/main/BeautyStudioApp/admin_7fps.gif?raw=true" alt="gif" width="250" />
</div> 
<br>

## Backend
The application uses **Firebase** as its backend to ensure a secure and scalable platform.

### Key Firebase Services
- **Cloud Firestore:** A real-time database for efficient data storage and retrieval.
- **Firebase Authentication:** Secure user login and registration.
- **Google Analytics:** Gain insights into user behavior and app performance.

## Technologies and Packages
- **Flutter:** Cross-platform mobile app development.
- **Firebase Core:** For initializing Firebase services.
- **cloud_firestore:** Enables real-time communication with Firestore.
- **firebase_auth:** Handles user authentication.
- **shared_preferences:** Stores simple data locally, such as login status and user preferences.
- **random_string:** Generates unique identifiers for user and booking data.

<br>

<br>
<div align="center">
    <img src="https://raw.githubusercontent.com/BrunosCodeLab/Images/refs/heads/main/BeautyStudioApp/Interface1.png" alt="Interface2" width="720" />
</div>
<br>


## Setup and Configuration

### Prerequisites
- **Flutter SDK** installed on your development machine.
- **Firebase Project:** Configure Firebase for both iOS and Android platforms.

### Firebase Configuration
1. **Create a Firebase Project:**
   - Open [Firebase Console](https://console.firebase.google.com/).
   - Create a project named `BeautySalon`.
   - Enable Google Analytics and set the location to your preference.

2. **iOS Setup:**
   - Retrieve the `Bundle Identifier` from `Xcode` (
     `ios/Runner/Signing & Capabilities`).
   - Download `GoogleService-Info.plist` from Firebase and place it in the `ios/Runner` directory.

3. **Android Setup:**
   - Locate the `applicationId` in `android/app/build.gradle`.
   - Download `google-services.json` from Firebase and place it in the `android/app` directory.
   - Modify the `build.gradle` files to include Firebase dependencies.

## Database Integration

### SharedPreferences
A `SharedPreferencesHelper` class manages local storage for user data, such as:
- User ID
- Username
- Email

Reason why `SharedPreferences` is implemented is to remember the login state (fast retrieval since it's stored directly on the device), so users don’t need to log in every time they reopen the app and so that Admin can see services even while offline

### Firestore Integration
- **User Data Storage:** Stores user details in the `users` collection.
- **Booking Management:** Handles booking operations in the `Booking` collection.
  - `addUserBooking`: Saves booking details such as services, date, and time.
  - `getBookings`: Retrieves real-time booking updates via a data stream.
  - `DeleteBooking`: Deletes specific bookings by document ID.


##
`This is a Flutter application I developed on my final year at Uni. Inspired by my fiancée's passion for all things beauty related.`


