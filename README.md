### FarmConnect: From Farm to Plate
FarmConnect is an Android application designed to empower farmers by providing an intuitive platform for listing products, managing orders, and communicating directly with consumers. 
The farmer side of the app focuses on enabling farmers to easily create and maintain their listings, engage in price negotiations, and manage incoming orders from consumers.
Features
## Core Farmer Features
 Product Listings: Farmers can add, update, and delete products they wish to sell. Each product can have details such as name, price, and unit of measurement (kg, quintal, tons).
 Pricing and Negotiation: Consumers can propose prices for listed items, which farmers can accept, reject, or counter. This feature supports a flexible pricing structure to help farmers engage in real-time negotiations.
Order Management: View and manage all incoming orders, including status updates, and handle order fulfillment efficiently.
Chat Support: Direct messaging feature to communicate with consumers for any inquiries, negotiations, or updates on product availability.
User Authentication: Firebase-based phone verification for secure access to the platform
## Planned Features for Farmers
Location-Based Listings: Option to prioritize consumers from nearby areas, enabling more localized business opportunities.
Analytics Dashboard: A simplified dashboard to show sales insights, popular products, and earnings over time (future enhancement).
## Technologies Used
Android Studio: Primary development environment.
Java: Main programming language for Android development.
Firebase: Used for Authentication, Realtime Database, and Storage
### Technical Requirements 🛠️
Android Studio Ladybug | 2024.2.1 Patch 1
JDK 11 or higher
Gradle 8.9
Minimum SDK: API 24 (Android 7.0)
Target SDK: API 34 (Android 14)
Java version: 11 or higher
### Dependencies
plugins {
    alias(libs.plugins.android.application)
}

android {
    namespace = "com.agronexus.farmconnect"
    compileSdk = 34

    defaultConfig {
        applicationId = "com.agronexus.farmconnect"
        minSdk = 26
        targetSdk = 34
        versionCode = 1
        versionName = "1.0"

        testInstrumentationRunner = "androidx.test.runner.AndroidJUnitRunner"
    }

    buildTypes {
        release {
            isMinifyEnabled = false
            proguardFiles(
                getDefaultProguardFile("proguard-android-optimize.txt"),
                "proguard-rules.pro"
            )
        }
    }
    compileOptions {
        sourceCompatibility = JavaVersion.VERSION_1_8
        targetCompatibility = JavaVersion.VERSION_1_8
    }
}

dependencies {

    implementation(libs.appcompat)
    implementation(libs.material)
    implementation(libs.activity)
    implementation(libs.constraintlayout)
    testImplementation(libs.junit)
    androidTestImplementation(libs.ext.junit)
    androidTestImplementation(libs.espresso.core)
}

Installation and Setup 🚀
Prerequisites
Install Android Studio Ladybug | 2024.2.1 Patch 1
Install Java Development Kit (JDK) 11 or higher
Set up an Android device or emulator with API level 24 or higher
Steps
Clone the repository:
git clone https://github.com/AyushmaanKapri/Farm_Connect.git
Open Android Studio Ladybug
Select "Open an Existing Project"
Navigate to the cloned directory and click "OK"
Wait for Gradle sync to complete

### Configuration
Create a local.properties file in the project root directory
Add the following properties:
sdk.dir=YOUR_ANDROID_SDK_PATH

### Debug Build
Select your target device (emulator or physical device running Android 7.0 or higher)
Click the "Run" button (green play icon) or press Shift + F10
Wait for the app to build and install on your device
Release Build
Open terminal in project root
Execute:
./gradlew assembleRelease
Find the APK in app/build/outputs/apk/release/
