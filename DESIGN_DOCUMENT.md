# Home Service - Design Document

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features and Functionality](#features-and-functionality)
3. [Application Architecture](#application-architecture)
4. [User Interface Design](#user-interface-design)
5. [Data Models](#data-models)
6. [User Flow Diagrams](#user-flow-diagrams)
7. [Wireframes](#wireframes)
8. [Technical Specifications](#technical-specifications)
9. [Third-Party Integrations](#third-party-integrations)
10. [Security Considerations](#security-considerations)

## Project Overview

### Application Name
**Home Service** (package: home_hub)

### Description
A comprehensive mobile application built with Flutter that connects customers with qualified home service professionals. The app enables users to book various home services including plumbing, electrical work, painting, carpentry, cleaning, and car services.

### Target Platform
- **Primary**: Mobile (Android & iOS)
- **Framework**: Flutter 3.0+
- **Language**: Dart

### Version
Current Version: 2.0.0

## Features and Functionality

### Core Features

#### 1. User Authentication & Profile Management
- **User Registration**: Email/phone-based signup
- **Login System**: Secure authentication with OTP verification
- **Profile Management**: User can view and edit personal information
- **Social Login**: Integration with Google and other social platforms

#### 2. Service Categories
The application offers the following service categories:
- **Plumbers**: Plumbing installation, repair, and maintenance
- **Electricians**: Electrical installation, repair, and troubleshooting
- **Painters**: Interior and exterior painting services
- **Carpenters**: Furniture repair, installation, and carpentry work
- **Home Cleaning**: Full house, kitchen, bedroom, and specialized cleaning
- **Car Washers**: Vehicle cleaning and detailing services
- **Car Repairing**: Automotive repair and maintenance

#### 3. Service Provider Features
- **Provider Listings**: Browse qualified service providers
- **Provider Profiles**: Detailed information including:
  - Professional photos
  - Service descriptions
  - Hourly rates
  - Job completion count
  - Customer ratings and reviews
- **Provider Services**: Detailed service offerings with pricing
- **Availability Status**: Real-time provider availability

#### 4. Booking Management
- **Service Booking**: Easy booking process with date/time selection
- **Active Bookings**: Track ongoing service appointments
- **Booking History**: Complete history of past services
- **Booking Cancellation**: Cancel bookings with appropriate policies
- **Order Summary**: Detailed breakdown of services and costs

#### 5. Search and Discovery
- **Service Search**: Search for specific services or providers
- **Category Browsing**: Browse services by category
- **Filter Options**: Filter by price, rating, availability
- **Popular Services**: Highlighted trending services
- **Favorites**: Save preferred service providers

#### 6. Payment Integration
- **Multiple Payment Options**: Support for various payment methods:
  - UPI payments
  - Paytm
  - Amazon Pay
  - Free Charge
  - Ola Money
- **Secure Transactions**: Encrypted payment processing
- **Payment History**: Track all payment transactions

#### 7. Reviews and Ratings
- **Customer Reviews**: Read and write service reviews
- **Star Ratings**: 5-star rating system
- **Review Components**: Detailed review display with photos
- **Provider Feedback**: Bidirectional rating system

#### 8. Notifications
- **Push Notifications**: Real-time updates on bookings
- **Booking Reminders**: Automated appointment reminders
- **Status Updates**: Service progress notifications
- **Promotional Offers**: Special deals and offers

#### 9. User Experience Features
- **Onboarding**: Interactive walkthrough for new users
- **Dark/Light Theme**: Theme customization options
- **Responsive Design**: Optimized for different screen sizes
- **Offline Support**: Basic functionality without internet

### Advanced Features

#### 10. Specialized Services
- **Home Construction**: Large-scale construction services
- **Home Renovation**: Complete home makeover services
- **Combo Services**: Bundled service packages
- **Subscription Services**: Recurring service plans

#### 11. Apartment-Specific Features
- **Apartment Size Selection**: Services based on apartment size
- **Building Services**: Services for entire buildings
- **Community Features**: Neighborhood service sharing

## Application Architecture

### Architecture Pattern
The application follows a **Component-Based Architecture** with **MobX State Management**.

### Directory Structure
```
lib/
├── components/           # Reusable UI components
├── custom_widget/        # Custom widgets
├── fragments/           # Main screen fragments
├── models/             # Data models
├── screens/            # Application screens
├── store/              # MobX stores for state management
└── utils/              # Utility functions and constants
```

### State Management
- **MobX**: Used for reactive state management
- **Shared Preferences**: Local data persistence
- **Observer Pattern**: Reactive UI updates

### Key Architectural Components

#### 1. Presentation Layer
- **Screens**: Full-screen views (login, dashboard, etc.)
- **Fragments**: Tab-based main sections (home, search, bookings, account)
- **Components**: Reusable UI elements
- **Custom Widgets**: Application-specific widgets

#### 2. Business Logic Layer
- **MobX Stores**: Centralized state management
- **Models**: Data structures and business entities
- **Services**: API integration and business logic

#### 3. Data Layer
- **Local Storage**: Shared Preferences for user settings
- **Static Data**: Hardcoded service and provider data
- **Asset Management**: Images, icons, and media files

### Navigation Architecture
- **Bottom Navigation**: Main app navigation with 4 tabs
- **Screen Navigation**: Standard Flutter navigation
- **Deep Linking**: Support for direct screen access

## User Interface Design

### Design Principles
- **Material Design**: Following Google's Material Design guidelines
- **Consistency**: Uniform design patterns across the app
- **Accessibility**: Support for different user needs
- **Responsive**: Adaptive layouts for various screen sizes

### Color Scheme
- **Primary Colors**: Defined in `colors.dart`
- **Theme Support**: Light and dark theme variants
- **Brand Colors**: Consistent brand identity

### Typography
- **Font Hierarchy**: Clear text size hierarchy
- **Readability**: Optimized for mobile reading
- **Localization Ready**: Support for different languages

### UI Components
- **Bottom Navigation Bar**: 4-tab navigation system
- **Cards**: Service and provider information display
- **Lists**: Scrollable content presentation
- **Forms**: User input collection
- **Dialogs**: Modal interactions
- **Page Indicators**: Smooth page transitions

## Data Models

### Core Data Models

#### 1. ServicesModel
```dart
class ServicesModel {
  int id;
  String serviceName;
  String subName;
  String shortDescription;
  String serviceImage;
  IconData serviceIcon;
  List<ServiceProviderModel> serviceProviders;
  bool isSelected;
}
```

#### 2. ServiceProviderModel
```dart
class ServiceProviderModel {
  int id;
  String name;
  String providerImage;
  String occupation;
  String star;
  String detailDescription;
  String jobs;
  String perHourPrice;
  bool isLiked;
  List<ProviderServicesModel> providerServices;
}
```

#### 3. ActiveBookingsModel
```dart
class ActiveBookingsModel {
  int id;
  String serviceName;
  String serviceImage;
  String name;
  String date;
  String time;
  String status;
  int price;
}
```

#### 4. CustomerReviewModel
```dart
class CustomerReviewModel {
  String customerName;
  String customerImage;
  String reviewText;
  String rating;
  String date;
}
```

#### 5. WalkThroughModel
```dart
class WalkThroughModel {
  String title;
  String subTitle;
  String imagePath;
}
```

### Supporting Models
- **ProviderServicesModel**: Individual service offerings
- **CustomerDetailsModel**: Customer information
- **LastBookingsModel**: Historical booking data
- **CommonModel**: Shared data structures
- **UpiPaymentModel**: Payment processing data
- **HomeConstructionModel**: Construction service data
- **RenovateServicesModel**: Renovation service data
- **CombosServicesModel**: Combo service packages
- **ApartmentSizeModel**: Apartment-specific data

## User Flow Diagrams

### 1. User Onboarding Flow
```
App Launch → Splash Screen → Walk-through Screens (3) → Sign In/Sign Up → Dashboard
```

### 2. Service Booking Flow
```
Home → Browse Categories → Select Service → Choose Provider → View Details → 
Book Service → Select Date/Time → Payment → Confirmation → Active Booking
```

### 3. Authentication Flow
```
Sign In Screen → Enter Credentials → OTP Verification → Dashboard
                ↓
Sign Up Screen → Enter Details → OTP Verification → Dashboard
```

### 4. Search and Discovery Flow
```
Search Tab → Enter Query → Filter Results → Select Provider → View Details → Book Service
```

### 5. Booking Management Flow
```
Bookings Tab → Active Bookings → View Details → Cancel/Modify
             → Booking History → View Past Services → Rate/Review
```

## Wireframes

### 1. Splash Screen
- App logo and branding
- Loading indicator
- Version information

### 2. Walk-through Screens (3 screens)
- **Screen 1**: "Give your home a makeover"
- **Screen 2**: "Qualified Professionals"  
- **Screen 3**: "Easy & Fast Services"
- Page indicators
- Skip/Next navigation

### 3. Authentication Screens
#### Sign In Screen
- Email/phone input field
- Password input field
- Login button
- Sign up link
- Social login options

#### Sign Up Screen
- Personal information fields
- Contact details
- Password setup
- Terms and conditions
- Create account button

#### OTP Verification
- Phone number display
- OTP input fields
- Resend OTP option
- Verify button

### 4. Main Dashboard (Bottom Navigation)

#### Home Fragment
- Header with notifications icon
- User greeting
- Search bar
- Banner carousel
- Service categories grid
- Popular services section
- Customer reviews section
- Special offers/combos

#### Search Fragment
- Search input field
- Category filters
- Service provider listings
- Sort and filter options
- Map view toggle

#### Bookings Fragment
- Tab navigation (Active/History)
- Booking cards with status
- Action buttons (Cancel/Reschedule)
- Empty state handling

#### Account Fragment
- User profile information
- Menu options:
  - My Profile
  - Favorite Services
  - Payment Methods
  - Notifications
  - Settings
  - Logout

### 5. Service Screens

#### All Categories Screen
- Grid layout of service categories
- Category icons and names
- Search functionality
- Featured categories

#### Service Providers Screen
- List of providers for selected service
- Provider cards with:
  - Profile image
  - Name and rating
  - Price per hour
  - Favorite button
- Filter and sort options

#### Provider Detail Screen
- Provider profile image
- Name, rating, and reviews count
- Service description
- Services offered list
- Pricing information
- Contact options
- Book now button

### 6. Booking Screens

#### Order Summary Screen
- Selected service details
- Provider information
- Date and time selection
- Price breakdown
- Total cost
- Proceed to payment button

#### Payment Screen
- Payment method selection
- UPI options
- Wallet options
- Card payment
- Apply coupon
- Pay now button

### 7. Additional Screens

#### Notification Screen
- List of notifications
- Timestamp information
- Read/unread status
- Action buttons

#### My Profile Screen
- Editable user information
- Profile image upload
- Contact details
- Save changes button

#### Favorite Services Screen
- Grid of liked providers
- Remove from favorites option
- Quick booking access

## Technical Specifications

### Development Environment
- **Flutter SDK**: >=3.0.0 <4.0.0
- **Dart**: Latest stable version
- **IDE**: Android Studio / VS Code
- **Version Control**: Git

### Dependencies

#### Core Dependencies
- `flutter`: Flutter SDK
- `cupertino_icons`: iOS-style icons

#### UI Dependencies
- `smooth_page_indicator`: ^1.0.0+2 (Page indicators)
- `smooth_star_rating_null_safety`: ^1.0.4+2 (Star ratings)
- `country_calling_code_picker`: ^2.0.1 (Country code selection)

#### State Management
- `mobx`: 2.2.0 (State management)
- `flutter_mobx`: 2.0.6+5 (Flutter MobX integration)

#### Utilities
- `intl`: ^0.18.1 (Internationalization)
- `shared_preferences`: ^2.1.2 (Local storage)

#### Development Dependencies
- `flutter_test`: Testing framework
- `build_runner`: 2.4.5 (Code generation)
- `mobx_codegen`: 2.3.0 (MobX code generation)

### Build Configuration
- **Android**: API level 21+ (Android 5.0+)
- **iOS**: iOS 11.0+
- **Target**: Mobile devices
- **Orientation**: Portrait only

### Performance Considerations
- Lazy loading for large lists
- Image caching and optimization
- Efficient state management with MobX
- Memory management for page controllers

## Third-Party Integrations

### Payment Gateways
- **UPI**: Direct UPI integration
- **Paytm**: Paytm wallet integration
- **Amazon Pay**: Amazon payment services
- **Free Charge**: Free Charge wallet
- **Ola Money**: Ola wallet integration

### Social Authentication
- **Google**: Google Sign-In integration
- **Instagram**: Social media integration

### Notification Services
- **Firebase Cloud Messaging**: Push notifications
- **Local Notifications**: App-based notifications

### Maps and Location
- **Location Services**: Provider location mapping
- **Address Selection**: Service location input

## Security Considerations

### Authentication Security
- Secure OTP verification
- Token-based authentication
- Session management
- Biometric authentication support

### Payment Security
- Encrypted payment processing
- PCI DSS compliance
- Secure API communication
- Transaction verification

### Data Protection
- User data encryption
- Secure local storage
- Privacy policy compliance
- GDPR considerations

### API Security
- HTTPS communication
- API key management
- Rate limiting
- Input validation

## Future Enhancements

### Planned Features
1. **Real-time Chat**: Communication between customers and providers
2. **Video Consultation**: Remote service consultation
3. **AI Recommendations**: Personalized service suggestions
4. **IoT Integration**: Smart home device integration
5. **Multi-language Support**: Localization for different regions
6. **Advanced Analytics**: User behavior tracking
7. **Loyalty Program**: Reward system for frequent users
8. **Service Marketplace**: Platform for service providers to list services

### Technical Improvements
1. **Backend API**: Migration from static data to dynamic API
2. **Real-time Updates**: WebSocket integration
3. **Offline Capability**: Enhanced offline functionality
4. **Performance Optimization**: Code splitting and lazy loading
5. **Testing**: Comprehensive test coverage
6. **CI/CD Pipeline**: Automated deployment process

## Conclusion

The Home Service application provides a comprehensive platform for connecting customers with qualified service providers. The Flutter-based architecture ensures cross-platform compatibility while maintaining native performance. The component-based design promotes code reusability and maintainability.

The application successfully addresses the core needs of home service booking with features like provider discovery, secure booking, payment integration, and review systems. The MobX state management ensures reactive and efficient UI updates.

Future enhancements will focus on real-time capabilities, AI-driven recommendations, and expanded service offerings to create a more comprehensive home service ecosystem.

---

*Document Version: 1.0*  
*Last Updated: September 2024*  
*Created by: Development Team*