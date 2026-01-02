# ReactNativeapp - Product Store

A modern, cross-platform e-commerce mobile application built with React Native and Expo, featuring a beautiful product showcase with responsive design for both mobile and web platforms.

## 📱 About the App

ReactNativeapp is a product discovery and browsing application that demonstrates modern React Native development practices. The app showcases various consumer products across multiple categories, featuring:

- **Cross-platform compatibility** - Runs on iOS, Android, and Web
- **Responsive design** - Adaptive layouts for mobile and web
- **Modern UI/UX** - Clean, intuitive interface with smooth animations
- **Product categories** - Audio, Wearables, Gaming, Fitness, Tech, and more
- **Featured products** - Curated selection of popular items
- **Search functionality** - Product discovery capabilities
- **Dark/Light theme support** - Automatic theme switching

## 🚀 Features

- **Home Dashboard**: Welcome screen with hero banner, product categories, and featured/popular products
- **Product Catalog**: Browse all available products with detailed information
- **Category Filtering**: Shop by product categories
- **Responsive Layouts**: Different UI optimizations for mobile and web platforms
- **Smooth Animations**: React Native Reanimated for fluid interactions
- **TypeScript**: Full type safety throughout the application
- **Expo Router**: File-based routing system
- **Haptic Feedback**: Enhanced user experience with touch feedback

## 🛠️ Tech Stack

### Core Framework
- **React Native 0.81.5** - Cross-platform mobile framework
- **React 19.1.0** - UI library
- **Expo SDK 54** - Development platform and native modules

### Navigation & Routing
- **Expo Router 6.0** - File-based routing system
- **React Navigation 7.x** - Navigation primitives

### UI & Styling
- **React Native Reanimated 4.1** - Animation library
- **Expo Vector Icons** - Icon library
- **Custom Themed Components** - Consistent theming system

### Development Tools
- **TypeScript 5.9** - Type safety
- **ESLint** - Code linting
- **Expo CLI** - Development workflow

### Key Dependencies
- `@expo/vector-icons` - Icon components
- `@react-navigation/native` - Navigation framework
- `expo-constants` - App configuration
- `expo-font` - Font loading
- `expo-haptics` - Haptic feedback
- `expo-image` - Image optimization
- `expo-splash-screen` - Splash screen management
- `expo-status-bar` - Status bar styling
- `react-native-safe-area-context` - Safe area handling

## 📁 Project Structure

```
ReactNativeapp/
├── app/                          # Application screens (file-based routing)
│   ├── _layout.tsx              # Root layout with theme provider
│   ├── modal.tsx                # Modal screen
│   └── (tabs)/                  # Tab-based navigation
│       ├── _layout.tsx          # Tab layout configuration
│       ├── index.tsx            # Home/Dashboard screen
│       └── explore.tsx          # Products catalog screen
├── components/                  # Reusable UI components
│   ├── Dashboard.tsx            # Home screen dashboard
│   ├── ProductList.tsx          # Product catalog list
│   ├── ProductCard.tsx          # Product card (web grid)
│   ├── ProductItem.tsx          # Product item (mobile list)
│   ├── themed-text.tsx          # Themed text component
│   ├── themed-view.tsx          # Themed view component
│   ├── ui/                      # UI component library
│   └── ...
├── data/                        # Application data
│   └── products.ts              # Mock product data
├── types/                       # TypeScript type definitions
│   └── product.ts               # Product interface
├── hooks/                       # Custom React hooks
│   ├── use-color-scheme.ts      # Theme detection hook
│   └── use-theme-color.ts       # Theme color hook
├── constants/                   # Application constants
│   └── theme.ts                 # Theme configuration
├── assets/                      # Static assets
│   └── images/                  # App icons and images
├── scripts/                     # Utility scripts
│   └── reset-project.js         # Project reset script
├── app.json                     # Expo configuration
├── package.json                 # Dependencies and scripts
├── tsconfig.json                # TypeScript configuration
└── README.md                    # This file
```

## 🔄 Application Startup Flow

### 1. App Initialization
- **Entry Point**: `expo-router/entry` loads the app
- **Root Layout** (`app/_layout.tsx`):
  - Initializes theme provider (Dark/Light mode support)
  - Sets up stack navigator for modal screens
  - Configures status bar styling

### 2. Navigation Setup
- **Tabs Layout** (`app/(tabs)/_layout.tsx`):
  - **Mobile**: Bottom tab navigation with haptic feedback
  - **Web**: Top navigation bar
  - Two main tabs: "Home" (house icon) and "Products" (bag icon)

### 3. Screen Rendering
- **Home Screen** (`app/(tabs)/index.tsx`):
  - Loads Dashboard component
  - Displays hero section, categories, featured products
  - Handles user interactions (product taps, category selection, search)

- **Products Screen** (`app/(tabs)/explore.tsx`):
  - Loads ProductList component
  - Displays all products in responsive layout
  - Grid view on web, list view on mobile

### 4. Component Architecture
- **Dashboard Component**:
  - Responsive design (different layouts for web/mobile)
  - Hero banner with call-to-action
  - Horizontal scrolling categories
  - Featured and popular product sections

- **ProductList Component**:
  - Grid layout for web (ProductCard components)
  - List layout for mobile (ProductItem components)
  - FlatList for efficient scrolling on mobile

- **Product Components**:
  - ProductCard: Card-based layout for web grids
  - ProductItem: List item layout for mobile
  - Both display product name, price, description, and category

### 5. Data Flow
- Mock product data loaded from `data/products.ts`
- Product interface defined in `types/product.ts`
- Components receive data through props
- Event handlers log interactions (TODO: implement navigation to detail screens)

### 6. Theme & Styling
- Automatic light/dark theme detection
- Themed components for consistent styling
- Platform-specific optimizations
- Custom color schemes and typography

## 🏃‍♂️ Getting Started

### Prerequisites
- Node.js (v18 or later)
- npm or yarn
- Expo CLI (`npm install -g @expo/cli`)
- For mobile development: Android Studio (Android) or Xcode (iOS)

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/kartik786-git/ReactNativeapp.git
   cd ReactNativeapp
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Start the development server**
   ```bash
   npm start
   # or
   npx expo start
   ```

### Running the App

After starting the development server, you can run the app on:

- **iOS Simulator**: Press `i` in the terminal or select "iOS simulator" from the Expo Go app
- **Android Emulator**: Press `a` in the terminal or select "Android emulator" from the Expo Go app
- **Physical Device**: Scan the QR code with the Expo Go app
- **Web Browser**: Press `w` in the terminal for web preview

### Available Scripts

- `npm start` - Start the Expo development server
- `npm run android` - Run on Android emulator/device
- `npm run ios` - Run on iOS simulator/device
- `npm run web` - Run in web browser
- `npm run lint` - Run ESLint for code linting
- `npm run reset-project` - Reset to a blank Expo project

## 🔧 Development

### Code Style
- **TypeScript**: Strict type checking enabled
- **ESLint**: Configured with Expo's recommended rules
- **Prettier**: Code formatting (if configured)

### Key Architecture Decisions

1. **File-based Routing**: Expo Router provides intuitive navigation
2. **Component Composition**: Reusable components with clear separation of concerns
3. **Responsive Design**: Platform-specific layouts and optimizations
4. **Type Safety**: Full TypeScript coverage for better development experience
5. **Performance**: Optimized rendering with FlatList and efficient state management

### Adding New Features

1. **New Screens**: Add new files in the `app/` directory
2. **New Components**: Create components in the `components/` directory
3. **New Types**: Define interfaces in the `types/` directory
4. **New Data**: Add mock data to the `data/` directory

## 📦 Build & Deployment

### Building for Production

1. **Configure EAS Build** (if using Expo Application Services):
   ```bash
   npx eas build:configure
   ```

2. **Build for specific platforms**:
   ```bash
   npx eas build --platform android
   npx eas build --platform ios
   ```

### Publishing Updates

```bash
npx eas update
```

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- Built with [Expo](https://expo.dev/)
- Icons from [Expo Vector Icons](https://docs.expo.dev/guides/icons/)
- Inspired by modern e-commerce applications

## 📞 Support

For questions or issues, please open an issue on the [GitHub repository](https://github.com/kartik786-git/ReactNativeapp/issues).

---

**Happy coding! 🎉**
