# Healthcare Appointment Booking Mobile App

A comprehensive Healthcare Appointment Booking Mobile App built with Flutter, GetX for state management, MVC architecture, and Sqflite for local storage.

## 🚀 Features

### Core Features
- **Authentication System**: Login/Signup screens with dummy authentication logic
- **Doctor Directory**: Browse and search through a list of healthcare professionals
- **Doctor Profiles**: Detailed information about each doctor including specialties, experience, and ratings
- **Appointment Booking**: Select available time slots and book appointments
- **Appointment Management**: View, confirm, and manage your appointments

### Advanced Features
- **Local Database**: Sqflite integration for persistent data storage
- **Responsive Design**: Optimized for all screen sizes and orientations
- **Smooth Animations**: Lottie animations for enhanced user experience
- **Hero Animations**: Seamless transitions between doctor cards and profiles
- **Modern UI**: Clean, professional design using Google Fonts and Material Design

## 🏗️ Architecture

### MVC Pattern
- **Models**: Data classes for Doctor, User, and Appointment
- **Views**: UI screens and widgets
- **Controllers**: Business logic using GetX state management

### State Management
- **GetX**: For reactive state management, dependency injection, and routing
- **Observables**: Using `obs`, `Rx`, and `update()` for reactive UI updates
- **Bindings**: Lazy loading for controllers

### Database Structure
- **Sqflite**: Local SQLite database for data persistence
- **Tables**: Users, Doctors, Appointments, and related entities

## 📱 Screens

1. **Splash Screen**: App introduction with loading animation
2. **Login/Signup**: Authentication screens with form validation
3. **Home Screen**: Doctor listing with search and filter options
4. **Doctor Profile**: Detailed doctor information and appointment booking
5. **Appointment Confirmation**: Booking summary and confirmation
6. **My Appointments**: User's appointment history and management

## 🛠️ Tech Stack

- **Framework**: Flutter 3.7.2+
- **State Management**: GetX 4.6.6
- **Database**: Sqflite 2.3.2
- **UI/UX**: Google Fonts, Lottie Animations, Material Design
- **Architecture**: MVC Pattern
- **Routing**: GetX Navigation

## 📦 Dependencies

```yaml
# State Management
get: ^4.6.6

# Database
sqflite: ^2.3.2
path: ^1.8.3

# UI/UX
google_fonts: ^6.1.0
flutter_svg: ^2.0.9

# Utils
intl: ^0.19.0
uuid: ^4.3.3
http: ^1.1.2
shared_preferences: ^2.2.2
```

## 🚀 Getting Started

### Prerequisites
- Flutter SDK 3.7.2 or higher
- Dart SDK
- Android Studio / VS Code
- Android Emulator or Physical Device

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd hospital_management
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

### Project Structure

```
lib/
├── main.dart
├── app/
│   ├── bindings/
│   ├── controllers/
│   ├── data/
│   │   ├── models/
│   │   ├── providers/
│   │   └── repositories/
│   ├── modules/
│   │   ├── auth/
│   │   ├── home/
│   │   ├── doctor/
│   │   └── appointment/
│   ├── routes/
│   ├── themes/
│   └── utils/
└── assets/
    ├── animations/
    ├── images/
    └── icons/
```

## 📋 Features Breakdown

### Authentication Module
- User registration and login
- Form validation and error handling
- Session management with local storage
- Secure password handling

### Doctor Management
- Doctor listing with search functionality
- Filter by specialty, rating, and availability
- Detailed doctor profiles with images
- Rating and review system

### Appointment System
- Real-time slot availability
- Appointment booking with confirmation
- Appointment history and management
- Reminder notifications

### Database Schema
```sql
-- Users table
CREATE TABLE users (
  id TEXT PRIMARY KEY,
  name TEXT NOT NULL,
  email TEXT UNIQUE NOT NULL,
  password TEXT NOT NULL,
  created_at TEXT NOT NULL
);

-- Doctors table
CREATE TABLE doctors (
  id TEXT PRIMARY KEY,
  name TEXT NOT NULL,
  specialty TEXT NOT NULL,
  experience INTEGER NOT NULL,
  rating REAL NOT NULL,
  image_url TEXT,
  description TEXT
);

-- Appointments table
CREATE TABLE appointments (
  id TEXT PRIMARY KEY,
  user_id TEXT NOT NULL,
  doctor_id TEXT NOT NULL,
  date TEXT NOT NULL,
  time TEXT NOT NULL,
  status TEXT NOT NULL,
  created_at TEXT NOT NULL,
  FOREIGN KEY (user_id) REFERENCES users (id),
  FOREIGN KEY (doctor_id) REFERENCES doctors (id)
);
```

## 🎨 UI/UX Features

- **Modern Design**: Clean, professional interface
- **Responsive Layout**: Adapts to different screen sizes
- **Smooth Animations**: Lottie animations for better UX
- **Hero Transitions**: Seamless navigation between screens
- **Loading States**: Proper loading indicators
- **Error Handling**: User-friendly error messages

## 🔧 Configuration

### Environment Setup
- Configure database path and settings
- Set up asset directories
- Configure routing and navigation

### Customization
- Modify theme colors and fonts
- Add custom animations
- Configure database schema
- Update dummy data

## 📊 Performance

- **Lazy Loading**: Controllers loaded on demand
- **Efficient Database**: Optimized queries and indexing
- **Memory Management**: Proper disposal of resources
- **Smooth Animations**: 60fps animations with Lottie

## 🧪 Testing

```bash
# Run unit tests
flutter test

# Run integration tests
flutter test integration_test/
```

## 📱 Platform Support

- ✅ Android (API 21+)
- ✅ iOS (12.0+)
- ✅ Web (Chrome, Firefox, Safari)
- ✅ Desktop (Windows, macOS, Linux)

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Add tests if applicable
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- GetX for excellent state management
- Lottie for beautiful animations
- Google Fonts for typography

## 📞 Support

For support and questions:
- Create an issue in the repository
- Contact the development team
- Check the documentation


