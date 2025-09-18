# Activity For Results Demo

A simple Android application demonstrating the `startActivityForResult()` pattern for inter-activity communication.

## Overview

This Android application showcases how to:
- Start an activity and wait for a result
- Pass data between activities
- Handle activity results with proper request and result codes
- Implement bidirectional communication between activities

## Features

- **Two-Activity Architecture**: Demonstrates navigation between FirstActivity and SecondActivity
- **Result Handling**: Shows how to return data from a child activity to its parent
- **User Interaction**: Provides buttons for starting activities and returning results
- **Toast Notifications**: Displays returned data or cancellation messages to the user

## Technical Details

### Architecture

The application consists of two main activities:

1. **FirstActivity**:
   - Main launcher activity
   - Initiates SecondActivity using `startActivityForResult()`
   - Handles returned results in `onActivityResult()`
   - Displays Toast messages based on the result

2. **SecondActivity**:
   - Child activity launched by FirstActivity
   - Provides two options: return a result or cancel
   - Uses `setResult()` to send data back to FirstActivity
   - Finishes itself after setting the result

### Key Components

- **Intent Communication**: Uses Intent extras to pass data between activities
- **Request Codes**: Implements request code (1) to identify the result source
- **Result Codes**: Utilizes `RESULT_OK` and `RESULT_CANCELED` for different outcomes
- **Data Passing**: Demonstrates string data transfer via Intent extras

### Layout

- **activity_first.xml**: Contains a TextView title and a button to start the second activity
- **activity_second.xml**: Features a TextView title and two buttons (Cancel and Return Results)
- Both layouts use RelativeLayout with a custom background

## Requirements

- Android SDK 14+ (minSdkVersion: 14)
- Target SDK: 17
- Android Studio or compatible IDE
- Gradle build system

## Installation

1. Clone this repository
2. Open the project in Android Studio
3. Build the project using Gradle
4. Run on an Android device or emulator

## Usage

1. Launch the application
2. Click "Start Activity 2" button on the first screen
3. In the second activity, choose either:
   - "Return Results" to send back a success message
   - "Cancel" to return without data
4. Observe the Toast message displaying the result

## Code Structure

```
app/
├── src/
│   └── main/
│       ├── java/
│       │   └── com/example/activitytest/
│       │       ├── FirstActivity.java
│       │       └── SecondActivity.java
│       ├── res/
│       │   ├── layout/
│       │   │   ├── activity_first.xml
│       │   │   └── activity_second.xml
│       │   └── values/
│       │       ├── strings.xml
│       │       ├── styles.xml
│       │       └── dimens.xml
│       └── AndroidManifest.xml
└── build.gradle
```

## Key Methods

### FirstActivity
- `onCreate()`: Sets up the UI and button click listener
- `onActivityResult()`: Processes results returned from SecondActivity

### SecondActivity
- `onCreate()`: Initializes UI and sets up button listeners
- Button listeners: Handle result return and cancellation

## Learning Points

This project is ideal for understanding:
- Android activity lifecycle
- Inter-activity communication patterns
- Result handling mechanisms
- Intent-based data passing
- User interaction feedback

## License

This project is provided as-is for educational purposes.

## Contributing

Feel free to fork this repository and submit pull requests for improvements or bug fixes.

## Author

Example Android Activity Test Application