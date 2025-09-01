# Architecture Diagrams - Home Service App

## System Architecture Overview

```mermaid
graph TB
    A[Mobile App - Flutter] --> B[Presentation Layer]
    B --> C[Business Logic Layer]
    C --> D[Data Layer]
    
    B --> E[Screens]
    B --> F[Fragments]
    B --> G[Components]
    B --> H[Custom Widgets]
    
    C --> I[MobX Store]
    C --> J[Models]
    C --> K[Services]
    
    D --> L[Shared Preferences]
    D --> M[Static Data]
    D --> N[Assets]
    
    E --> E1[Splash Screen]
    E --> E2[Auth Screens]
    E --> E3[Dashboard]
    E --> E4[Service Screens]
    E --> E5[Booking Screens]
    
    F --> F1[Home Fragment]
    F --> F2[Search Fragment]
    F --> F3[Bookings Fragment]
    F --> F4[Account Fragment]
    
    G --> G1[Service Components]
    G --> G2[Booking Components]
    G --> G3[Review Components]
    G --> G4[Payment Components]
```

## Data Flow Architecture

```mermaid
graph LR
    A[User Interaction] --> B[UI Layer]
    B --> C[MobX Store]
    C --> D[Business Logic]
    D --> E[Data Models]
    E --> F[Local Storage]
    
    C --> G[State Updates]
    G --> H[Observer Widgets]
    H --> I[UI Re-render]
    
    D --> J[Static Data]
    D --> K[Asset Management]
```

## Component Hierarchy

```mermaid
graph TD
    A[MyApp] --> B[MaterialApp]
    B --> C[SplashScreen]
    B --> D[WalkThroughScreen]
    B --> E[AuthScreens]
    B --> F[DashboardScreen]
    
    F --> G[BottomNavigationBar]
    F --> H[PageView]
    
    H --> I[HomeFragment]
    H --> J[SearchFragment]
    H --> K[BookingsFragment]
    H --> L[AccountFragment]
    
    I --> M[HomeServiceComponent]
    I --> N[PopularServiceComponent]
    I --> O[CustomerReviewComponent]
    I --> P[CombosSubscriptionsComponent]
    
    J --> Q[SearchComponent]
    J --> R[ServiceListComponent]
    
    K --> S[ActiveBookingComponent]
    K --> T[BookingHistoryComponent]
    
    L --> U[ProfileWidget]
    L --> V[MenuItems]
```

## Booking Process Flow

```mermaid
sequenceDiagram
    participant User
    participant App
    participant ServiceProvider
    participant Payment
    participant Notification
    
    User->>App: Browse Services
    App->>User: Display Categories
    User->>App: Select Service
    App->>User: Show Providers
    User->>App: Select Provider
    App->>User: Show Provider Details
    User->>App: Book Service
    App->>User: Order Summary
    User->>Payment: Process Payment
    Payment-->>App: Payment Success
    App->>ServiceProvider: Booking Confirmed
    App->>Notification: Send Confirmation
    Notification-->>User: Booking Notification
    App->>User: Active Booking Created
```

## Authentication Flow

```mermaid
graph TD
    A[Start] --> B{User Type}
    B -->|New User| C[Sign Up]
    B -->|Existing User| D[Sign In]
    
    C --> E[Enter Details]
    E --> F[OTP Verification]
    F --> G{OTP Valid?}
    G -->|No| H[Resend OTP]
    H --> F
    G -->|Yes| I[Create Account]
    I --> J[Dashboard]
    
    D --> K[Enter Credentials]
    K --> L{Valid Credentials?}
    L -->|No| M[Show Error]
    M --> K
    L -->|Yes| N[OTP Verification]
    N --> O{OTP Valid?}
    O -->|No| P[Resend OTP]
    P --> N
    O -->|Yes| J
```

## Payment Integration Flow

```mermaid
graph TD
    A[Order Summary] --> B[Select Payment Method]
    B --> C{Payment Type}
    
    C -->|UPI| D[UPI Payment]
    C -->|Wallet| E[Wallet Payment]
    C -->|Card| F[Card Payment]
    
    D --> G[UPI Apps List]
    G --> H[Process UPI Payment]
    
    E --> I{Wallet Type}
    I -->|Paytm| J[Paytm Integration]
    I -->|Amazon Pay| K[Amazon Pay Integration]
    I -->|FreeCharge| L[FreeCharge Integration]
    I -->|Ola Money| M[Ola Money Integration]
    
    F --> N[Card Details Form]
    N --> O[Process Card Payment]
    
    H --> P{Payment Success?}
    J --> P
    K --> P
    L --> P
    M --> P
    O --> P
    
    P -->|Yes| Q[Booking Confirmed]
    P -->|No| R[Payment Failed]
    R --> B
    
    Q --> S[Generate Receipt]
    S --> T[Update Booking Status]
    T --> U[Send Notifications]
```

## Service Discovery Flow

```mermaid
graph TD
    A[User Opens App] --> B[Home Screen]
    B --> C[Browse Categories]
    B --> D[Search Services]
    B --> E[Popular Services]
    
    C --> F[Select Category]
    F --> G[View Service Providers]
    
    D --> H[Enter Search Query]
    H --> I[Apply Filters]
    I --> G
    
    E --> J[Featured Services]
    J --> G
    
    G --> K[Sort Results]
    K --> L[Provider List]
    L --> M[Select Provider]
    M --> N[View Provider Details]
    N --> O[Check Reviews]
    N --> P[View Services]
    N --> Q[Check Availability]
    
    O --> R[Read Customer Reviews]
    P --> S[Service Pricing]
    Q --> T[Available Time Slots]
    
    R --> U[Make Decision]
    S --> U
    T --> U
    
    U --> V[Book Service]
    V --> W[Proceed to Payment]
```

## Navigation Flow

```mermaid
graph TD
    A[App Launch] --> B{First Time?}
    B -->|Yes| C[Walk Through]
    B -->|No| D{Logged In?}
    
    C --> E[Sign In/Up]
    D -->|No| E
    D -->|Yes| F[Dashboard]
    E --> F
    
    F --> G[Home Tab]
    F --> H[Search Tab]
    F --> I[Bookings Tab]
    F --> J[Account Tab]
    
    G --> K[Service Categories]
    G --> L[Popular Services]
    G --> M[Banners]
    
    H --> N[Search Results]
    H --> O[Filters]
    
    I --> P[Active Bookings]
    I --> Q[Booking History]
    
    J --> R[Profile]
    J --> S[Settings]
    J --> T[Logout]
    
    K --> U[Service Providers]
    U --> V[Provider Details]
    V --> W[Book Service]
    W --> X[Payment]
    X --> Y[Confirmation]
```