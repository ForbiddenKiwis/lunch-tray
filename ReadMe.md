# 🍽️ Lunch Tray App – Navigation UI with Jetpack Compose

The **Lunch Tray App** is a simple Android application that demonstrates how to build a multi-step ordering interface using **Jetpack Compose Navigation** and **Kotlin**. It uses a structured navigation flow with a dynamic AppBar that adapts to the current screen and navigation state.

---

## 📱 Screens Overview

The app consists of the following screens, each with a dedicated title defined via an `enum` and string resources:

- 🏁 **Start**
- 🍽️ **Entree Menu**
- 🥗 **Side Dish Menu**
- 🧂 **Accompaniment Menu**
- 💳 **Checkout**

---

## 🚀 Key Features

### 📌 Enum-Based Screen Management
- An `enum class` defines constants for each screen.
- Each screen is associated with a title from the app’s `strings.xml` resource file.

### 🧭 Jetpack Compose Navigation
- The app uses a `NavHostController` for managing screen transitions.
- The current screen is dynamically detected from the navigation back stack.

### 🧱 Scaffold and AppBar Integration
- The `Scaffold` composable wraps the screen content with a top `AppBar`.
- The `AppBar` displays the title of the current screen.
- A back (up) button is shown **only** when backward navigation is available (i.e., not on the Start screen).

---

## 🔄 Navigation Flow

```plaintext
Start Screen
    ↓ [Start Order]
Entree Menu
    ↓ [Next]
Side Dish Menu
    ↓ [Next]
Accompaniment Menu
    ↓ [Next]
Checkout
    → [Submit] returns to Start
    → [Cancel] returns to Start