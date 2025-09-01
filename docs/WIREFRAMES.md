# Wireframes - Home Service App

## Overview
This document contains wireframes for all major screens in the Home Service mobile application. The wireframes are described in detail, showing the layout, components, and user interactions for each screen.

## 1. Splash Screen

```
┌─────────────────────────────────┐
│                                 │
│                                 │
│         [APP LOGO]              │
│        Home Service             │
│                                 │
│                                 │
│                                 │
│        Loading...               │
│         ●●●○○                   │
│                                 │
│                                 │
│     Version 2.0.0               │
│                                 │
└─────────────────────────────────┘
```

**Components:**
- App logo/branding
- App name "Home Service"
- Loading indicator
- Version number at bottom

## 2. Walk-through Screens (3 screens)

### Screen 1: "Give your home a makeover"
```
┌─────────────────────────────────┐
│                Skip             │
│                                 │
│     [ROOM IMAGE]                │
│                                 │
│                                 │
│  Give your home a makeover      │
│                                 │
│  The best services that you     │
│  could find for your home, as   │
│  we have everything that you    │
│  are in need                    │
│                                 │
│         ●○○                     │
│                                 │
│              [Next]             │
└─────────────────────────────────┘
```

### Screen 2: "Qualified Professionals"
```
┌─────────────────────────────────┐
│                Skip             │
│                                 │
│     [WORKER IMAGE]              │
│                                 │
│                                 │
│  Qualified Professionals        │
│                                 │
│  Search From the list of        │
│  Qualified Professionals        │
│  around you as we bring the     │
│  best one for you              │
│                                 │
│         ○●○                     │
│                                 │
│              [Next]             │
└─────────────────────────────────┘
```

### Screen 3: "Easy & Fast Services"
```
┌─────────────────────────────────┐
│                Skip             │
│                                 │
│     [SERVICE IMAGE]             │
│                                 │
│                                 │
│    Easy & Fast Services         │
│                                 │
│  Get your services done in      │
│  the quickest way possible      │
│  with our professional team     │
│                                 │
│         ○○●                     │
│                                 │
│          [Get Started]          │
└─────────────────────────────────┘
```

## 3. Authentication Screens

### Sign In Screen
```
┌─────────────────────────────────┐
│                                 │
│         Welcome Back            │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Email or Phone              │ │
│  └─────────────────────────────┘ │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Password                 👁️ │ │
│  └─────────────────────────────┘ │
│                                 │
│              [Login]            │
│                                 │
│         Forgot Password?        │
│                                 │
│    ─────── OR ───────           │
│                                 │
│     [G] Sign in with Google     │
│                                 │
│  Don't have an account? Sign Up │
└─────────────────────────────────┘
```

### Sign Up Screen
```
┌─────────────────────────────────┐
│                                 │
│        Create Account           │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Full Name                   │ │
│  └─────────────────────────────┘ │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Email                       │ │
│  └─────────────────────────────┘ │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Phone Number                │ │
│  └─────────────────────────────┘ │
│                                 │
│  ┌─────────────────────────────┐ │
│  │ Password                 👁️ │ │
│  └─────────────────────────────┘ │
│                                 │
│  □ I agree to Terms & Conditions│
│                                 │
│           [Sign Up]             │
│                                 │
│  Already have an account? Login │
└─────────────────────────────────┘
```

### OTP Verification Screen
```
┌─────────────────────────────────┐
│          ← Back                 │
│                                 │
│      Verify Phone Number        │
│                                 │
│   We have sent verification     │
│   code to +91 9876543210        │
│                                 │
│                                 │
│      ┌─┐ ┌─┐ ┌─┐ ┌─┐           │
│      │ │ │ │ │ │ │ │           │
│      └─┘ └─┘ └─┘ └─┘           │
│                                 │
│                                 │
│           [Verify]              │
│                                 │
│   Didn't receive code?          │
│      Resend in 30s              │
│                                 │
└─────────────────────────────────┘
```

## 4. Main Dashboard (Bottom Navigation)

### Home Fragment
```
┌─────────────────────────────────┐
│ ☰  Good Morning!            🔔  │
│     John Doe                    │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ Search services...       🔍 │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │     [BANNER IMAGE]          │ │
│ │  Special Offers & Deals     │ │
│ └─────────────────────────────┘ │
│                                 │
│ Categories                   All│
│ ┌──┐ ┌──┐ ┌──┐ ┌──┐           │
│ │🔧│ │⚡│ │🎨│ │🔨│           │
│ └──┘ └──┘ └──┘ └──┘           │
│Plmb Elec Pnt Crp              │
│                                 │
│ Popular Services               │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Full House Cleaning   │ │
│ │ ⭐4.5 • From ₹299           │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────┬─────┬─────┬─────────┐   │
│ │ 🏠  │ 🔍  │ 📋  │ 👤      │   │
│ │Home │Srch │Book │Account  │   │
│ └─────┴─────┴─────┴─────────┘   │
└─────────────────────────────────┘
```

### Search Fragment
```
┌─────────────────────────────────┐
│                             🔔  │
│ ┌─────────────────────────────┐ │
│ │ Search services...       🔍 │ │
│ └─────────────────────────────┘ │
│                                 │
│ Filters: [All] [Price] [Rating] │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Michel Smith       ❤️ │ │
│ │ Plumber • ⭐3.5 • ₹330/hr   │ │
│ │ 120 jobs completed          │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] John Carter        ❤️ │ │
│ │ Electrician • ⭐4.5 • ₹250  │ │
│ │ 95 jobs completed           │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Sammy Jaine        ❤️ │ │
│ │ Painter • ⭐4.0 • ₹310/hr   │ │
│ │ 87 jobs completed           │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────┬─────┬─────┬─────────┐   │
│ │ 🏠  │ 🔍  │ 📋  │ 👤      │   │
│ │Home │Srch │Book │Account  │   │
│ └─────┴─────┴─────┴─────────┘   │
└─────────────────────────────────┘
```

### Bookings Fragment
```
┌─────────────────────────────────┐
│        My Bookings          🔔  │
│                                 │
│  [Active]    [History]          │
│  ────────    ─────────          │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Full House Cleaning   │ │
│ │ Jaylon Cleaning Services    │ │
│ │ Jan 4, 2022 • 4:00 AM      │ │
│ │ Status: In Process          │ │
│ │ ₹2,599    [Cancel] [Track]  │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Kitchen Cleaning      │ │
│ │ SJ Cleaning Services        │ │
│ │ Dec 4, 2022 • 6:00 AM      │ │
│ │ Status: Assigned            │ │
│ │ ₹3,000    [Cancel] [Call]   │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────┬─────┬─────┬─────────┐   │
│ │ 🏠  │ 🔍  │ 📋  │ 👤      │   │
│ │Home │Srch │Book │Account  │   │
│ └─────┴─────┴─────┴─────────┘   │
└─────────────────────────────────┘
```

### Account Fragment
```
┌─────────────────────────────────┐
│             Profile         🔔  │
│                                 │
│      ┌───┐                     │
│      │👤 │  John Doe           │
│      └───┘  john@email.com     │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ 👤 My Profile            > │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ ❤️ Favorite Services     > │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ 💳 Payment Methods       > │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ 🔔 Notifications         > │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ ⚙️ Settings              > │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ 🚪 Logout                   │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────┬─────┬─────┬─────────┐   │
│ │ 🏠  │ 🔍  │ 📋  │ 👤      │   │
│ │Home │Srch │Book │Account  │   │
│ └─────┴─────┴─────┴─────────┘   │
└─────────────────────────────────┘
```

## 5. Service Screens

### All Categories Screen
```
┌─────────────────────────────────┐
│ ← Back    All Categories    🔍  │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ Search categories...        │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────┬─────┬─────┬─────────┐   │
│ │ 🔧  │ ⚡  │ 🎨  │ 🔨      │   │
│ │Plmb │Elec │Pnt │Carp     │   │
│ └─────┼─────┼─────┼─────────┤   │
│ │ 🧹  │ 🚗  │ 🔧  │ 🏗️      │   │
│ │Cln  │Car  │Rep │Const    │   │
│ └─────┼─────┼─────┼─────────┤   │
│ │ 🎨  │ 📦  │ ⚡  │ +       │   │
│ │Rnv  │Cmb  │IoT │More     │   │
│ └─────┴─────┴─────┴─────────┘   │
│                                 │
│ Featured Categories             │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Emergency Plumbing    │ │
│ │ Available 24/7              │ │
│ └─────────────────────────────┘ │
│                                 │
└─────────────────────────────────┘
```

### Service Providers Screen
```
┌─────────────────────────────────┐
│ ← Back     Plumbers         ⚙️  │
│                                 │
│ Sort: [Rating] [Price] [Distance│
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Michel Smith       💝 │ │
│ │ ⭐3.5 • 120 jobs • ₹330/hr  │ │
│ │ Plumbing installation,repair│ │
│ │ [View Details] [Book Now]   │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] John Carter        💖 │ │
│ │ ⭐4.5 • 95 jobs • ₹250/hr   │ │
│ │ Expert in pipe fitting      │ │
│ │ [View Details] [Book Now]   │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Mike Johnson       💝 │ │
│ │ ⭐4.0 • 87 jobs • ₹280/hr   │ │
│ │ Bathroom & kitchen specialist│ │
│ │ [View Details] [Book Now]   │ │
│ └─────────────────────────────┘ │
│                                 │
└─────────────────────────────────┘
```

### Provider Detail Screen
```
┌─────────────────────────────────┐
│ ← Back                      💝  │
│                                 │
│      ┌─────────────────┐        │
│      │   [PROVIDER]    │        │
│      │    IMAGE        │        │
│      └─────────────────┘        │
│                                 │
│        Michel Smith             │
│     ⭐⭐⭐⭐☆ 3.5 (120 reviews)    │
│                                 │
│  💼 Plumber • 120 jobs • ₹330/hr│
│                                 │
│  📍 2.5 km away                 │
│                                 │
│  📞 [Call] 📧 [Message]         │
│                                 │
│  About                          │
│  Plumbers install and repair    │
│  plumbing systems in residential│
│  and commercial properties...   │
│                                 │
│  Services Offered               │
│  • Pipe Installation ₹500      │
│  • Tap Repair       ₹200       │
│  • Drain Cleaning   ₹300       │
│                                 │
│  Reviews (120)               📝 │
│  ┌─────────────────────────────┐│
│  │👤 John D. ⭐⭐⭐⭐⭐ Great!  ││
│  └─────────────────────────────┘│
│                                 │
│           [Book Now]            │
└─────────────────────────────────┘
```

## 6. Booking Flow Screens

### Order Summary Screen
```
┌─────────────────────────────────┐
│ ← Back    Order Summary         │
│                                 │
│ Service Details                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Pipe Installation     │ │
│ │ Michel Smith - Plumber      │ │
│ │ ⭐3.5 • ₹330/hr             │ │
│ └─────────────────────────────┘ │
│                                 │
│ Schedule                        │
│ ┌─────────────────────────────┐ │
│ │ 📅 Select Date              │ │
│ │ Jan 15, 2023 ▼             │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ 🕐 Select Time              │ │
│ │ 10:00 AM ▼                 │ │
│ └─────────────────────────────┘ │
│                                 │
│ Price Breakdown                 │
│ Service Charge         ₹500     │
│ Platform Fee           ₹50      │
│ Taxes                  ₹55      │
│ ─────────────────────────────   │
│ Total                  ₹605     │
│                                 │
│        [Proceed to Pay]         │
└─────────────────────────────────┘
```

### Payment Screen
```
┌─────────────────────────────────┐
│ ← Back      Payment             │
│                                 │
│ Amount to Pay: ₹605             │
│                                 │
│ Select Payment Method           │
│                                 │
│ UPI                             │
│ ┌─────────────────────────────┐ │
│ │ [📱] Google Pay          ✓ │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ [📱] PhonePe               │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ [📱] Paytm                 │ │
│ └─────────────────────────────┘ │
│                                 │
│ Wallets                         │
│ ┌─────────────────────────────┐ │
│ │ [💳] Amazon Pay            │ │
│ └─────────────────────────────┘ │
│ ┌─────────────────────────────┐ │
│ │ [💳] Ola Money             │ │
│ └─────────────────────────────┘ │
│                                 │
│ Credit/Debit Card               │
│ ┌─────────────────────────────┐ │
│ │ [💳] Add New Card          │ │
│ └─────────────────────────────┘ │
│                                 │
│           [Pay Now]             │
└─────────────────────────────────┘
```

## 7. Additional Screens

### Notification Screen
```
┌─────────────────────────────────┐
│ ← Back    Notifications         │
│                                 │
│ Today                           │
│ ┌─────────────────────────────┐ │
│ │ 🔔 Booking Confirmed        │ │
│ │ Your plumbing service is    │ │
│ │ confirmed for Jan 15, 10 AM │ │
│ │ 2 hours ago                 │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ 💰 Payment Successful       │ │
│ │ Payment of ₹605 completed   │ │
│ │ Transaction ID: TXN123456   │ │
│ │ 3 hours ago                 │ │
│ └─────────────────────────────┘ │
│                                 │
│ Yesterday                       │
│ ┌─────────────────────────────┐ │
│ │ ⭐ Rate Your Service        │ │
│ │ How was your experience     │ │
│ │ with Michel Smith?          │ │
│ │ 1 day ago                   │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ 🎉 Special Offer            │ │
│ │ Get 20% off on next booking │ │
│ │ Use code: SAVE20            │ │
│ │ 2 days ago                  │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
```

### My Profile Screen
```
┌─────────────────────────────────┐
│ ← Back     My Profile       ⚙️  │
│                                 │
│           ┌─────┐               │
│           │ 👤  │               │
│           │     │               │
│           └─────┘               │
│         [Change Photo]          │
│                                 │
│ Personal Information            │
│ ┌─────────────────────────────┐ │
│ │ Full Name                   │ │
│ │ John Doe                    │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ Email                       │ │
│ │ john.doe@email.com          │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ Phone                       │ │
│ │ +91 9876543210              │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ Address                     │ │
│ │ 123 Main St, City, State    │ │
│ └─────────────────────────────┘ │
│                                 │
│         [Save Changes]          │
└─────────────────────────────────┘
```

### Favorite Services Screen
```
┌─────────────────────────────────┐
│ ← Back  Favorite Services   🔍  │
│                                 │
│ Your Liked Service Providers    │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Michel Smith       💖 │ │
│ │ Plumber • ⭐3.5 • ₹330/hr   │ │
│ │ [Book Now]    [Remove]      │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] John Carter        💖 │ │
│ │ Electrician • ⭐4.5 • ₹250  │ │
│ │ [Book Now]    [Remove]      │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │ [IMG] Sarah Wilson       💖 │ │
│ │ House Cleaner • ⭐4.8 • ₹200│ │
│ │ [Book Now]    [Remove]      │ │
│ └─────────────────────────────┘ │
│                                 │
│ ┌─────────────────────────────┐ │
│ │        No more items        │ │
│ │    Browse more services     │ │
│ │       [Explore Now]         │ │
│ └─────────────────────────────┘ │
└─────────────────────────────────┘
```

## Design Guidelines

### Typography
- **Headers**: Bold, 18-24px
- **Subheaders**: Medium, 16-18px  
- **Body Text**: Regular, 14-16px
- **Caption**: Regular, 12-14px

### Colors
- **Primary**: Blue/Teal theme
- **Secondary**: Gray accents
- **Success**: Green
- **Warning**: Orange
- **Error**: Red

### Spacing
- **Margin**: 16px standard
- **Padding**: 12px for cards
- **Button Height**: 48px
- **Input Height**: 44px

### Components
- **Cards**: Rounded corners (8px), subtle shadow
- **Buttons**: Rounded (6px), primary color
- **Icons**: 24px standard size
- **Profile Images**: Circular, various sizes

### Responsive Design
- **Mobile First**: Optimized for 375px width
- **Scalable**: Adapts to different screen sizes
- **Touch Friendly**: 44px minimum touch targets

### Accessibility
- **High Contrast**: WCAG compliant color ratios
- **Font Size**: Minimum 14px for body text
- **Touch Targets**: Minimum 44px tap area
- **Focus States**: Clear focus indicators