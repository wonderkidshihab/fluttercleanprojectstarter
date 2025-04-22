# fluttercleanprojectstarter

> A new Flutter project template preconfigured with Clean Architecture principles, designed to help you skip boilerplate and focus on feature development.

---

## 🚀 Features

* **Layered Architecture** : Network, Data, Domain, Presentation, and Core layers preconfigured.
* **Dependency Injection** : Integrated with `get_it` & `injectable` for easy service management.
* **Networking** : `dio` setup with logging using `pretty_dio_logger`.
* **State Management** : Ready-to-use `flutter_bloc` & `bloc` patterns.
* **Immutable Models** : Use `equatable` and FP constructs via `fpdart`.
* **Local Persistence** : Offline-first support with `sqflite` for local storage.
* **Connectivity Handling** : Managed by `connectivity_plus`.
* **Utilities** : File paths (`path` & `path_provider`), responsive design (`flutter_screenutil`), and logging (`logger`).
* **Example Module** : Demonstrates the end-to-end flow of a feature.

---

## 📂 Folder Structure

```
lib/
├── core/                  # Shared utilities, constants, and helpers
├── features/              # Feature modules
│   └── example/           # Example feature implementation
│       ├── data/          # Repository, data sources, models
│       ├── domain/        # Entities, repositories, use cases
│       └── presentation/  # BLoC, widgets, pages
├── injection/             # Service locator setup
└── main.dart              # Application entry point
```

---

## 📖 Getting Started

### Prerequisites

* Flutter SDK (>= 3.0.0)
* Dart SDK (>= 2.17.0)
* A code editor (VS Code, Android Studio)

### Installation

1. **Clone the repository** :

```bash
   git clone https://github.com/wonderkidshihab/fluttercleanprojectstarter.git
   cd fluttercleanprojectstarter
```

1. **Optional: Rename the project base name** (replace `fluttercleanprojectstarter` with your project name, e.g., `todo_maker`):
   ```bash
   NEW_NAME="todo_maker"
   grep -rl 'fluttercleanprojectstarter' . | xargs sed -i '' -e "s/fluttercleanprojectstarter/${NEW_NAME}/g"
   ```
2. **Create Flutter project with custom organization** :

```bash
   flutter create . --org com.your_org_name
```

1. **Update package identifiers** (replace `com.example.fluttercleanprojectstarter` with your org and project name):
   ```bash
   grep -rl 'com.example.fluttercleanprojectstarter' . | xargs sed -i '' -e "s/com.example.fluttercleanprojectstarter/com.your_org_name.${NEW_NAME}/g"
   ```
2. **Install dependencies** :

```bash
   flutter pub get
```

1. **Generate code** :

```bash
   flutter pub run build_runner build --delete-conflicting-outputs
```

1. **Run the app** :

```bash
   flutter run
```

---

## 📦 Dependencies

This project uses the following key dependencies (see `pubspec.yaml` for full list):

| Package                | Version  | Purpose                               |
| ---------------------- | -------- | ------------------------------------- |
| `flutter_bloc`       | ^9.1.0   | State management                      |
| `bloc`               | ^9.0.0   | Bloc core library                     |
| `equatable`          | ^2.0.7   | Value equality for Dart objects       |
| `fpdart`             | ^1.1.1   | Functional programming tools          |
| `dio`                | ^5.8.0+1 | HTTP client                           |
| `pretty_dio_logger`  | ^1.4.0   | Dio logger interceptor                |
| `get_it`             | ^8.0.3   | Service locator                       |
| `path_provider`      | ^2.1.5   | File system paths                     |
| `path`               | ^1.9.0   | File path utilities                   |
| `connectivity_plus`  | ^6.1.3   | Network connectivity monitoring       |
| `sqflite`            | ^2.4.1   | SQLite database for local persistence |
| `flutter_screenutil` | ^5.9.3   | Responsive UI utility                 |
| `logger`             | ^2.5.0   | Structured logging                    |

---

## 🏗 Architecture Overview

1. **Presentation** : Widgets, navigation, and state management (BLoC/Cubit).
2. **Domain** : Business logic via Use Cases and Entities.
3. **Data** : Repository implementations, remote/local data sources.
4. **Core** : Networking, error handling, and shared utilities.
5. **Injection** : Dependency registration and service locator setup.

---

## 💡 How to Add a New Feature

1. Copy the `lib/features/example/` module and rename it.
2. Update the folder names and class identifiers.
3. Define domain entities and use cases in `domain/`.
4. Implement data sources and repositories in `data/`.
5. Create BLoCs/Cubits and UI pages in `presentation/`.
6. Register dependencies in `injection/injection.config.dart`.
7. Run the build runner to generate necessary code.

---

## 🤝 Contributing

Contributions are welcome! To contribute:

1. Fork the repo
2. Create a branch (`git checkout -b feature/MyFeature`)
3. Commit changes (`git commit -m "Add MyFeature"`)
4. Push (`git push origin feature/MyFeature`)
5. Open a PR

Please open issues for bugs or feature requests.
