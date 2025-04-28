# SavedStateHandleApp

This project demonstrates the use of **SavedStateHandle** in Android to persist and restore **UI-related state** during process death (e.g., screen rotations or app backgrounding). It highlights how **SavedStateHandle** can be used to save small pieces of UI data that need to survive configuration changes.

## Key Concepts Covered

### 1. **What is SavedStateHandle?**
**SavedStateHandle** is a bundle provided by Android to save and restore UI-related state in a **ViewModel**. It is particularly useful for saving simple state data, such as form inputs or selection states, that need to be restored after process death.

#### Responsibilities:
- Stores key-value pairs for temporary UI state.
- Restores state after **process death**.
- Available per **Navigation Back Stack Entry**.

**Analogy**: **SavedStateHandle** is like a **temporary notepad** for storing UI-related information that Android keeps for you during process death.

### 2. **Process Death in Android**
**Process death** happens when Android kills your app’s process to reclaim system resources. When this occurs, in-memory **ViewModels** are cleared. **SavedStateHandle** helps to persist the necessary state to restore UI data upon process restart.

### 3. **Use Cases for SavedStateHandle**
- **Form inputs**: Save the user’s input data when the activity is recreated after process death.
- **Navigation arguments**: Retain the arguments passed during navigation between fragments.
- **UI-related data**: Store simple UI data that doesn’t require complex storage mechanisms.

---

## Features

- **State Persistence**: Demonstrates how **SavedStateHandle** retains UI state, even when the app is killed and restarted.
- **ViewModel Integration**: Shows how to use **SavedStateHandle** in combination with **ViewModels** to manage state.
- **Jetpack Compose**: The app integrates Jetpack Compose for UI management, binding **SavedStateHandle** to Composables.

---

## Key Libraries Used

- `androidx.lifecycle.ViewModel`: To manage UI-related data lifecycle-aware.
- `androidx.lifecycle.SavedStateHandle`: To save and restore UI-related state across process death.
- Jetpack Compose for UI development.

---

## Getting Started

### 1. Clone the Repository:
To clone the repository, run the following command:

```bash
git clone https://github.com/tashafdev/SavedStateHandleApp.git
