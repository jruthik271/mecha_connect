# 🛠️ Mecha Connect

A premium, feature-rich Flutter application designed to connect vehicle owners with local on-demand mechanic services, emergency fuel delivery, and a comprehensive marketplace for authentic spare parts and accessories. Whether you're stranded with a flat tire, running low on fuel, or looking to purchase genuine vehicle components, **Mecha Connect** has you covered.

---

## 🚀 Key Features

*   **✨ Interactive Onboarding & Splash Screen**: Experience a smooth entry animation and visual guides highlighting the core features of the platform.
*   **🔑 Secure Authentication**: Clean user login screen for seamless account verification and persistent sessions.
*   **📍 Mechanic Locator (Roadside Assist)**: 
    *   Dynamic service forms to detail your vehicle type and specific breakdown issue.
    *   Interactive maps powered by `flutter_map` and OpenStreetMap to automatically detect and display your position with a pulsing marker.
    *   Find, filter, and view nearby mechanics with direct access to contact info and addresses.
*   **⛽ Petrol Assist (Fuel On-Demand)**:
    *   Emergency fuel delivery (Petrol/Diesel) straight to your coordinates.
    *   Interactive sliders to customize your fuel order by either Litres or Rupees.
    *   Find nearby stations and track your delivery on the map.
*   **🛒 Spare Parts Marketplace**:
    *   Browse genuine vehicle accessories and components categorized by function (Engines, Brakes, Batteries, Accessories).
    *   Interactive search functionality to find components quickly.
    *   Detailed view panels with specifications and pricing.
    *   Fully functional shopping cart with quantity management, automatic total calculation, and order placement.
*   **💬 AI Assistant Chat**: An in-app support chatboard helping users troubleshoot vehicle issues and navigate app features.
*   **📦 Order Tracking**: Keep logs of all your ordered parts, fuel deliveries, and service requests.

---

## 📂 Project Structure

Here is an overview of the codebase organization:

*   [lib/main.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/main.dart) - Main entry point of the app; configures app themes, splash animations, and core route definitions.
*   [lib/Starting_screen/](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen) - Manages onboarding flows and initial screen routes.
    *   [screens.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/screens.dart) - [OnboardingScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/screens.dart#L6) and walkthrough content.
    *   [Login.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/Login.dart) - Handles [UserLoginScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/Login.dart#L7) interface and validation.
    *   [home.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/home.dart) - The [ServiceSelectionScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/Starting_screen/home.dart#L6) showcasing roadside assistance options.
*   [lib/bottom_bar/](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar) - Bottom navigation hub.
    *   [bottom_navigation.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/bottom_navigation.dart) - Custom navigation bar wrapper ([BottomNavigation](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/bottom_navigation.dart#L32)) built using `google_nav_bar`.
    *   [chatboard.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/chatboard.dart) - Features the AI interactive [ChatBot](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/chatboard.dart#L8) view.
    *   [OrderScreen.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/OrderScreen.dart) - Lists active and past service/parts requests via the [Orderscreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/bottom_bar/OrderScreen.dart#L6) widget.
*   [lib/homescreen/](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen) - Central service maps and location hubs.
    *   [mechanic_screen.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/mechanic_screen.dart) - GPS mechanic locator app screens ([VehicleFormPage](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/mechanic_screen.dart#L38) and [MechanicMapScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/mechanic_screen.dart#L155)).
    *   [petrol_page.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/petrol_page.dart) - On-demand fuel locator and order parameters ([FuelSelectionPage](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/petrol_page.dart#L32)).
    *   [drawerscreen.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/homescreen/drawerscreen.dart) - Side drawer navigation drawer containing user profile details.
*   [lib/parts/](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts) - Spare parts store components.
    *   [parts_screen.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts/parts_screen.dart) - Main store display for parts catalogs ([PartsScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts/parts_screen.dart#L14)).
    *   [cart_screen.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts/cart_screen.dart) - Checkout cart module with item quantity management ([CartScreen](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts/cart_screen.dart#L9)).
    *   [order_data.dart](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/lib/parts/order_data.dart) - Tracks store ordering states.
*   [assets/](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/assets) - Curated set of images and icons representing batteries, engines, accessories, maps, and UI elements.

---

## 🛠️ Tech Stack & Dependencies

*   **Framework**: [Flutter SDK](https://flutter.dev) (Dart SDK v3.7.2+)
*   **Maps & Navigation**: 
    *   `flutter_map` - Robust OpenStreetMap layers integration.
    *   `flutter_map_cancellable_tile_provider` - Fast, cancellable map tiles rendering.
    *   `flutter_map_tile_caching` - Offline tile indexing and caching support.
    *   `geolocator` - Precise user GPS querying and status tracking.
    *   `latlong2` - Latitude/Longitude math helpers.
*   **User Interface**: 
    *   `google_nav_bar` - Modern sliding bottom navigation bar.
    *   `device_preview` - Virtual multi-screen sizing simulation for developers.
*   **Configuration**:
    *   `flutter_dotenv` - Safe management of API endpoints and keys.

---

## ⚡ Getting Started

Follow these steps to set up and run the project locally on your machine:

### 1. Prerequisites
Ensure you have the following installed:
*   [Flutter SDK](https://docs.flutter.dev/get-started/install) (version `>=3.7.2`)
*   Dart SDK
*   An Android Emulator, iOS Simulator, or physical device connected
*   An IDE such as VS Code or Android Studio with Flutter extensions

### 2. Clone and Setup
```bash
# Clone the repository
git clone https://github.com/jruthik271/mecha_connect.git

# Navigate into the project folder
cd mecha_connect-1

# Fetch project dependencies
flutter pub get
```

### 3. Configure Environment
Create a `.env` file in the root directory if you need custom API URLs or key mappings:
```env
# Example environment parameters
API_BASE_URL=https://api.mechaconnect.com
MAP_STYLE_URL=https://tile.openstreetmap.org/{z}/{x}/{y}.png
```

### 4. Run the Project
Launch the application on your running device:
```bash
flutter run
```
To run and test on a specific target device:
```bash
flutter run -d <device_id>
```

---

## 🤝 Contribution Guidelines
We welcome contributions to Mecha Connect! Please follow these steps to contribute:
1. Fork the Repository.
2. Create a feature branch (`git checkout -b feature/NewFeature`).
3. Commit your changes (`git commit -m 'Add NewFeature'`).
4. Push to the branch (`git push origin feature/NewFeature`).
5. Open a Pull Request.

---

## 📄 License
This project is proprietary and is not licensed for public distribution. Check [pubspec.yaml](file:///c:/Desktop/Sumanth_Folder/PROJECTS/mecha_connect-1/pubspec.yaml) for specific package terms and credentials.
