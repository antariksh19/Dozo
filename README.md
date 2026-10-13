<div align="center">


  <h1>Dozo: Medication Adherence App 💊</h1>

  <p>A cloud-native Android application engineered to ensure strict medication adherence through persistent background scheduling and real-time cloud synchronization.</p>
</div>

<br/>

<div align="center">
  <img src="https://img.shields.io/badge/Kotlin-0095D5?style=for-the-badge&logo=kotlin&logoColor=white" alt="Kotlin" />
  <img src="https://img.shields.io/badge/Jetpack_Compose-4285F4?style=for-the-badge&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose" />
  <img src="https://img.shields.io/badge/Firebase-FFCA28?style=for-the-badge&logo=firebase&logoColor=black" alt="Firebase" />
  <img src="https://img.shields.io/badge/Android_Studio-3DDC84?style=for-the-badge&logo=android-studio&logoColor=white" alt="Android Studio" />
</div>

---

## 🚀 Overview

Dozo is a modern Android health utility application built entirely with Kotlin and Jetpack Compose. It leverages a clean MVVM (Model-View-ViewModel) architecture to provide users with a highly responsive, crash-resistant experience for managing daily medication schedules, tracking dosage history, and receiving reliable foreground alerts. 

### ✨ Key Technical Features

* **Persistent Alarm Scheduling:** Utilizes customized `ReminderScheduler.kt` and `NotificationReceiver.kt` implementations to guarantee precise foreground alerts, ensuring alarms persist even across system restarts.
* **Clean MVVM Architecture:** Highly decoupled codebase separating state management (`MedecineViewModel.kt`) from data operations (`MedicineRepository.kt`), ensuring scalability and testability.
* **Modern Declarative UI:** Fully built with Jetpack Compose, featuring responsive custom elements like `HorizontalCalendar.kt`, `AnimatedGradientBrush.kt`, and `ThreeDEffects.kt` for a polished user experience.
* **Cloud-Native Sync:** Pre-configured with Google Services (`google-services.json`) for seamless backend communication and secure data persistence.

## 📂 Project Architecture

The repository follows a strict package-by-feature structure to maintain an organized, scalable Android environment:

```text
Dozo/
├── app/src/main/java/com/example/dozo/
│   ├── broadcast/         # Alarm triggers and notification receivers
│   ├── data/              # Repositories and data models (Medecine.kt, DoseHistory.kt)
│   ├── ui/
│   │   ├── components/    # Reusable Compose widgets (EmptyStateView, DosageStepper)
│   │   ├── screens/       # Core app screens (Main, Dashboard, Settings)
│   │   └── theme/         # Global typography, color palettes, and theme states
│   ├── viewmodel/         # State holders and UI logic handlers
│   └── MainActivity.kt    # Application entry point
├── app/google-services.json # Firebase environment configuration
├── app/proguard-rules.pro   # R8 optimization and obfuscation rules
└── build.gradle.kts         # Kotlin DSL build scripts and dependencies
```

## 🛠 System Setup & Installation

Follow these instructions to build and run the Dozo application locally using Android Studio.

### Prerequisites
* Android Studio (Latest Stable Version)
* JDK 17+
* An Android Emulator (API Level 26+) or a physical Android device.

### Local Development

**1. Clone the repository:**
```bash
git clone [https://github.com/antariksh19/dozo.git](https://github.com/antariksh19/dozo.git)
cd dozo
```

**2. Open the Project:**
* Launch Android Studio.
* Select **Open** and navigate to the cloned `dozo` directory.
* Allow Gradle to automatically download required dependencies and sync the project (configured via the Kotlin DSL `build.gradle.kts` files).

**3. Firebase Configuration:**
* The project expects a `google-services.json` file in the `app/` directory. If you are cloning this for your own use, replace the existing file with your own Firebase project configuration to enable cloud syncing.

**4. Run the Application:**
* Select your target emulator or physical device from the device dropdown.
* Click the **Run** button (`Shift + F10`) to compile the project and deploy the APK.

## 🧪 Testing

The repository includes foundational setups for both unit and instrumented testing to validate the MVVM logic and UI components.
* Run Unit Tests: Navigate to `app/src/test/java/` and execute `ExampleUnitTest.kt`.
* Run UI Tests: Navigate to `app/src/androidTest/java/` and execute `ExampleInstrumentedTest.kt`.

## 📫 Connect

* **LinkedIn:** [Antariksh Mohapatra](https://www.linkedin.com/in/antariksh-mohapatra/)
* **Email:** [antariksh19m@gmail.com](mailto:antariksh19m@gmail.com)
* **GitHub:** [@antariksh19](https://github.com/antariksh19)

## 📄 License
Distributed under the MIT License.
