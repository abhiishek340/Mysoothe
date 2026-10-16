<div align="center">

# MySoothe

A wellness-app home screen built with Jetpack Compose, based on Google's Basic Layouts in Compose codelab.

<img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat-square&logo=kotlin&logoColor=white" alt="Kotlin"/>
<img src="https://img.shields.io/badge/Jetpack%20Compose-4285F4?style=flat-square&logo=jetpackcompose&logoColor=white" alt="Jetpack Compose"/>
<img src="https://img.shields.io/badge/Material%203-757575?style=flat-square&logo=materialdesign&logoColor=white" alt="Material 3"/>
<img src="https://img.shields.io/badge/Android-34A853?style=flat-square&logo=android&logoColor=white" alt="Android"/>
<img src="https://img.shields.io/badge/License-Apache%202.0-blue?style=flat-square" alt="Apache 2.0 License"/>

</div>

## Overview

This project is my implementation of Google's [Basic Layouts in Compose](https://developer.android.com/codelabs/jetpack-compose-layouts) codelab. The starter code and assets come from the Android Open Source Project. I filled in the composables step by step. The result is the home screen of "MySoothe", a sample meditation and wellness app. It practices modifiers, slot APIs, lazy layouts, scrolling and Material 3 scaffolding.

## Features

- **Search bar**: a Material 3 `TextField` with a leading search icon and themed colors.
- **"Align your body" row**: a horizontally scrolling `LazyRow` of circular image items with captions.
- **"Favorite collections" grid**: a two-row `LazyHorizontalGrid` of image cards.
- **Reusable sections**: a `HomeSection` composable that takes a title and a content slot.
- **Scrollable home screen**: the sections are stacked in a vertically scrolling `Column`.
- **Bottom navigation**: a `Scaffold` with a Material 3 `NavigationBar` (Home and Profile).
- **Landscape layout (prepared)**: `SootheNavigationRail` and `MySootheAppLandscape` composables use a `NavigationRail` instead of a bottom bar.
- **Custom theme**: `MySootheTheme` with custom colors, shapes and typography, plus `@Preview`s for each component.

## Tech stack

| Layer | Technology |
| --- | --- |
| Language | Kotlin 2.1 |
| UI | Jetpack Compose (BOM 2025.05.00), Material 3, Material Icons Extended |
| Build | Gradle 8.14 (Groovy DSL), AGP 8.10, Compose compiler plugin |
| Platform | Android, `minSdk 23`, `compileSdk 35`, `targetSdk 33` |

## Project structure

```
Mysoothe/
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── java/com/codelab/basiclayouts/
│       │   ├── MainActivity.kt      # All screen composables and sample data
│       │   └── ui/theme/            # Color.kt, Shape.kt, Theme.kt, Type.kt
│       └── res/drawable/            # Collection and "Align your body" images
├── spotless/copyright.kt            # License header template
├── build.gradle
├── LICENSE                          # Apache 2.0
└── ASSETS_LICENSE                   # SIL OFL (fonts) / Apache 2.0 (other assets)
```

## Getting started

### Prerequisites

- Android Studio (a recent version with Compose support)
- JDK 17 or newer
- An emulator or device running Android 6.0 (API 23) or higher

### Run

```bash
git clone https://github.com/abhiishek340/Mysoothe.git
cd Mysoothe
./gradlew installDebug
```

Or open the folder in Android Studio and run the `app` configuration. The individual components can also be inspected in the Compose Preview pane.

## Notes

- `MainActivity` always shows the portrait layout (`MySootheApp`). The landscape composables exist, but they are not yet chosen based on window size.
- The navigation items and search field are UI only. They do not navigate or filter content.

## License

Code is licensed under the [Apache License 2.0](LICENSE). Copyright 2022 The Android Open Source Project. Fonts are licensed under the SIL Open Font License, and other assets under Apache 2.0. See [ASSETS_LICENSE](ASSETS_LICENSE).

## Image asset attributions

| Image | Photographer |
| --- | --- |
| [fc1_short_mantras.jpg](https://www.pexels.com/photo/body-of-water-view-1825206/) | Elizaveta Kozorezova |
| [fc2_nature_meditations.jpg](https://www.pexels.com/photo/photo-of-green-leaves-3571551/) | Nothing Ahead |
| [fc3_stress_and_anxiety.jpg](https://www.pexels.com/photo/aerial-view-of-body-of-water-1557238/) | Jim |
| [fc4_self_massage.jpg](https://www.pexels.com/photo/photography-of-stones-1029604/) | Scott Webb |
| [fc5_overwhelmed.jpg](https://www.pexels.com/photo/white-clouds-3560044/) | Ruvim |
| [fc6_nightly_wind_down.jpg](https://www.pexels.com/photo/time-lapse-photo-of-stars-on-night-924824/) | Jakub Novacek |
| [ab1_inversions.jpg](https://www.pexels.com/photo/low-angle-view-of-woman-relaxing-on-beach-against-blue-sky-317157/) | Chevanon Photography |
| [ab2_quick_yoga.jpg](https://www.pexels.com/photo/photo-of-woman-stretching-her-body-1812964/) | Agung Pandit Wiguna |
| [ab3_stretching.jpg](https://www.pexels.com/photo/photo-of-women-stretching-together-4056723/) | Cliff Booth |
| [ab4_tabata.jpg](https://www.pexels.com/photo/fashion-man-people-art-4662438/) | Elly Fairytale |
| [ab5_hiit.jpg](https://www.pexels.com/photo/man-wearing-white-pants-under-blue-sky-999309/) | The Lazy Artist Gallery |
| [ab6_pre_natal_yoga.jpg](https://www.pexels.com/photo/woman-doing-yoga-396133/) | freestocks.org |

All images are from [Pexels](https://www.pexels.com).

---

Built by [Abhishek Yadav](https://github.com/abhiishek340)
