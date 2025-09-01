# Home Service - Book My Service App 🏠📱

A comprehensive Flutter mobile application that connects customers with qualified home service professionals. The app enables users to book various home services including plumbing, electrical work, painting, carpentry, cleaning, and car services.

## 📋 Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Screenshots](#screenshots)
- [Architecture](#architecture)
- [Getting Started](#getting-started)
- [Documentation](#documentation)
- [Technology Stack](#technology-stack)
- [Project Structure](#project-structure)
- [Contributing](#contributing)
- [License](#license)

## 🔍 Overview

**Home Service** is a Flutter-based mobile application designed to revolutionize the way people book and manage home services. The app provides a seamless platform for customers to discover, book, and track various home services while ensuring quality and reliability through a comprehensive rating and review system.

### Key Highlights
- 🎯 **7 Service Categories**: Plumbing, Electrical, Painting, Carpentry, Home Cleaning, Car Services, and Car Repair
- 👨‍🔧 **Qualified Professionals**: Verified service providers with ratings and reviews
- 💳 **Multiple Payment Options**: UPI, Wallets, Cards, and Net Banking
- 📱 **Cross-Platform**: Available for both Android and iOS
- 🌙 **Theme Support**: Light and Dark mode options
- 🔔 **Real-time Notifications**: Stay updated on booking status

## ✨ Features

### 🔐 User Management
- Secure user registration and authentication
- OTP verification for phone numbers
- Social login integration (Google)
- Comprehensive profile management
- Theme customization (Light/Dark mode)

### 🔍 Service Discovery
- **Service Categories**: Plumbers, Electricians, Painters, Carpenters, Home Cleaning, Car Services
- **Provider Search**: Find qualified professionals near you
- **Advanced Filtering**: By price, rating, distance, and availability
- **Detailed Profiles**: Provider information, ratings, reviews, and pricing

### 📅 Booking Management
- **Easy Booking**: Streamlined booking process with date/time selection
- **Active Bookings**: Track ongoing service appointments
- **Booking History**: Complete history of past services
- **Modifications**: Reschedule or cancel bookings
- **Status Updates**: Real-time booking status notifications

### 💰 Payment Integration
- **Multiple Options**: UPI (Google Pay, PhonePe, Paytm), Wallets (Amazon Pay, Ola Money), Cards
- **Secure Transactions**: Encrypted payment processing
- **Transparent Pricing**: Upfront cost estimates with breakdown
- **Payment History**: Track all transactions and receipts

### ⭐ Reviews & Ratings
- **Customer Reviews**: Read and write service reviews
- **Star Ratings**: 5-star rating system for providers
- **Photo Reviews**: Share photos with reviews
- **Quality Assurance**: Maintain service quality through feedback

### 🔔 Notifications
- **Push Notifications**: Real-time updates on bookings
- **SMS Alerts**: Important booking confirmations
- **Email Receipts**: Detailed invoices and service summaries

## 📱 Screenshots

### Onboarding & Authentication
| Splash Screen | Walk-through | Sign In | OTP Verification |
|:-------------:|:------------:|:-------:|:----------------:|
| [App Logo & Loading] | [Feature Intro] | [Login Form] | [OTP Input] |

### Main Application
| Home Screen | Search & Discovery | Bookings | Profile |
|:-----------:|:-----------------:|:--------:|:-------:|
| [Service Categories] | [Provider Listings] | [Active Bookings] | [User Profile] |

### Service Flow
| Provider Details | Order Summary | Payment | Confirmation |
|:----------------:|:-------------:|:-------:|:------------:|
| [Provider Info] | [Service Details] | [Payment Options] | [Booking Success] |

## 🏗️ Architecture

The application follows a **Component-Based Architecture** with **MobX State Management**:

```
┌─────────────────────────────────┐
│        Presentation Layer       │
│   (Screens, Fragments, Widgets) │
├─────────────────────────────────┤
│      Business Logic Layer       │
│     (MobX Stores, Models)       │
├─────────────────────────────────┤
│          Data Layer             │
│  (SharedPreferences, Assets)    │
└─────────────────────────────────┘
```

### Key Architectural Components
- **Screens**: Full-screen views (Splash, Dashboard, etc.)
- **Fragments**: Tab-based main sections (Home, Search, Bookings, Account)
- **Components**: Reusable UI elements
- **Models**: Data structures and business entities
- **Store**: MobX stores for state management
- **Utils**: Utility functions and constants

## 🚀 Getting Started

### Prerequisites
- **Flutter SDK**: Version 3.0.0 or higher
- **Dart**: Version 2.17.0 or higher
- **Android Studio** or **VS Code** with Flutter extensions
- **Android SDK**: API level 21+ (Android 5.0+)
- **iOS**: iOS 11.0+ (for iOS development)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/lstudios2018/bookmyservice.git
   cd bookmyservice
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Generate MobX files**
   ```bash
   flutter packages pub run build_runner build
   ```

4. **Run the application**
   ```bash
   # For Android
   flutter run
   
   # For iOS
   flutter run -d ios
   
   # For specific device
   flutter run -d <device_id>
   ```

### Building for Production

```bash
# Android APK
flutter build apk --release

# Android App Bundle (for Play Store)
flutter build appbundle --release

# iOS (requires Xcode)
flutter build ios --release
```

## 📚 Documentation

Comprehensive documentation is available in the `/docs` folder:

- **[Design Document](DESIGN_DOCUMENT.md)**: Complete project overview and specifications
- **[Architecture Diagrams](docs/ARCHITECTURE_DIAGRAMS.md)**: System architecture and flow diagrams
- **[Wireframes](docs/WIREFRAMES.md)**: Detailed UI wireframes for all screens
- **[Technical Specifications](docs/TECHNICAL_SPECIFICATIONS.md)**: Implementation details and code standards
- **[Features Documentation](docs/FEATURES.md)**: Comprehensive feature list and descriptions

## 🛠️ Technology Stack

### Frontend
- **Framework**: Flutter 3.0+
- **Language**: Dart
- **State Management**: MobX 2.2.0
- **UI Components**: Material Design

### Key Dependencies
- **smooth_page_indicator**: Page indicators for onboarding
- **smooth_star_rating_null_safety**: Star rating components
- **country_calling_code_picker**: Country code selection
- **intl**: Internationalization support
- **shared_preferences**: Local data storage
- **flutter_mobx**: MobX integration for Flutter

### Development Tools
- **build_runner**: Code generation
- **mobx_codegen**: MobX code generation
- **flutter_test**: Testing framework

## 📁 Project Structure

```
bookmyservice/
├── android/                     # Android-specific files
├── ios/                         # iOS-specific files
├── lib/                         # Main application code
│   ├── components/              # Reusable UI components
│   │   ├── active_booking_component.dart
│   │   ├── customer_review_component.dart
│   │   ├── service_list_component.dart
│   │   └── ...
│   ├── custom_widget/           # Custom widgets
│   │   ├── space.dart
│   │   └── text_field_widget.dart
│   ├── fragments/               # Main screen fragments
│   │   ├── home_fragment.dart
│   │   ├── search_fragment.dart
│   │   ├── bookings_fragment.dart
│   │   └── account_fragment.dart
│   ├── models/                  # Data models
│   │   ├── services_model.dart
│   │   ├── service_provider_model.dart
│   │   ├── active_bookings_model.dart
│   │   └── ...
│   ├── screens/                 # Full-screen views
│   │   ├── splash_screen.dart
│   │   ├── dashboard_screen.dart
│   │   ├── sign_in_screen.dart
│   │   └── ...
│   ├── store/                   # MobX stores
│   │   ├── appData.dart
│   │   └── appData.g.dart
│   ├── utils/                   # Utility functions
│   │   ├── colors.dart
│   │   ├── constants.dart
│   │   ├── images.dart
│   │   └── widgets.dart
│   └── main.dart               # Application entry point
├── assets/                     # Static assets
│   ├── images/                 # Image files
│   └── icons/                  # Icon files
├── docs/                       # Documentation
│   ├── ARCHITECTURE_DIAGRAMS.md
│   ├── WIREFRAMES.md
│   ├── TECHNICAL_SPECIFICATIONS.md
│   └── FEATURES.md
├── test/                       # Test files
├── pubspec.yaml               # Dependencies and metadata
├── DESIGN_DOCUMENT.md         # Main design document
└── README.md                  # This file
```

## 🤝 Contributing

We welcome contributions to improve the Home Service app! Please follow these guidelines:

### Getting Started
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Make your changes
4. Run tests (`flutter test`)
5. Commit your changes (`git commit -m 'Add amazing feature'`)
6. Push to the branch (`git push origin feature/amazing-feature`)
7. Open a Pull Request

### Development Guidelines
- Follow Dart/Flutter coding standards
- Write unit tests for new features
- Update documentation for significant changes
- Use meaningful commit messages
- Ensure code is properly formatted (`flutter format .`)

### Code Style
- Use descriptive variable names
- Add comments for complex logic
- Follow the existing architecture patterns
- Maintain consistent file organization

## 🔮 Future Enhancements

### Planned Features
- **AI-Powered Recommendations**: Smart service suggestions based on user behavior
- **Real-time Chat**: In-app messaging between customers and providers
- **Video Consultation**: Remote service consultation capabilities
- **IoT Integration**: Smart home device integration
- **Web Platform**: Browser-based version of the application
- **Multi-language Support**: Localization for different regions

### Technical Improvements
- **Backend API**: Migration from static data to dynamic API
- **Real-time Updates**: WebSocket integration for live updates
- **Enhanced Offline Support**: Comprehensive offline functionality
- **Performance Optimization**: Code splitting and lazy loading
- **Advanced Analytics**: User behavior tracking and insights

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 📞 Support

For support, questions, or feedback:

- **Email**: support@homeservice.app
- **Issues**: [GitHub Issues](https://github.com/lstudios2018/bookmyservice/issues)
- **Documentation**: [Project Wiki](https://github.com/lstudios2018/bookmyservice/wiki)

## 🙏 Acknowledgments

- **Flutter Team**: For providing an excellent cross-platform framework
- **Material Design**: For comprehensive design guidelines
- **MobX Team**: For reactive state management solution
- **Open Source Community**: For various packages and tools used in this project

---

**Made with ❤️ by the Home Service Team**

*Transforming the way people access home services, one booking at a time.*

