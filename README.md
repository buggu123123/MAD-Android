# Android Practicals 1–8

A collection of Android Studio practical programs developed using **Java and XML**.

## Requirements

Before starting, install:

* Android Studio
* Android SDK
* Android SDK Platform
* Android Emulator **or** a physical Android phone
* Java/JDK (Android Studio normally provides the required JDK)

---

# General Procedure

The following procedure can be used for each practical.

## Step 1 — Open Android Studio

1. Open **Android Studio**.
2. Select **New Project**.
3. Select **Empty Views Activity**.
4. Click **Next**.

> Make sure you select **Empty Views Activity**, not the Compose template, because these practicals use XML layouts.

---

## Step 2 — Create the Project

Enter the project details.

Example:

```text
Name: Practical1
Package name: com.example.myinfo
Language: Java
Minimum SDK: API 23 or above
```

Click **Finish**.

Wait for Android Studio to finish **Gradle Sync**.

---

# Step 3 — Understand the Project Structure

After creating the project, the important folders are:

```text
Practical1/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/example/...
│           │       └── MainActivity.java
│           │
│           ├── res/
│           │   ├── layout/
│           │   │   └── activity_main.xml
│           │   │
│           │   └── menu/
│           │       └── color_menu.xml
│           │
│           └── AndroidManifest.xml
│
└── build.gradle
```

Not every practical needs every file.

---

# Step 4 — Create the XML File

Open:

```text
app
└── src
    └── main
        └── res
            └── layout
                └── activity_main.xml
```

Open `activity_main.xml`.

Delete the existing XML code and paste the XML code from the corresponding practical TXT file.

Save the file.

---

# Step 5 — Create the Java File

Go to:

```text
app
└── src
    └── main
        └── java
```

Open the package folder and select:

```text
MainActivity.java
```

Replace the existing Java code with the code from the corresponding practical TXT file.

Save the file.

---

# Step 6 — Additional Files

Some practicals require additional files.

## Practical 2

Practical 2 requires:

```text
activity_main.xml
activity_home.xml
MainActivity.java
HomeActivity.java
```

Create `HomeActivity.java` in the same Java package.

Create `activity_home.xml` inside:

```text
res/layout/
```

---

## Practical 4

Practical 4 requires a menu XML file.

Create the following directory if it does not already exist:

```text
res/menu/
```

Then create:

```text
color_menu.xml
```

The structure becomes:

```text
res/
├── layout/
│   └── activity_main.xml
│
└── menu/
    └── color_menu.xml
```

The practical uses the options menu to change the activity background color.

---

## Practical 7

Practical 7 requires:

```text
MainActivity.java
MyService.java
activity_main.xml
AndroidManifest.xml
```

Create:

```text
MyService.java
```

in the same Java package as `MainActivity`.

Then add the Service inside the `<application>` section of `AndroidManifest.xml`:

```xml
<service
    android:name=".MyService"
    android:enabled="true"
    android:exported="false" />
```

## The service displays `"Service is running..."` every 5 seconds after starting and displays `"Service Stopped"` when stopped.

# Practical 8

Practical 8 requires:

```text
MainActivity.java
PrimeService.java
activity_main.xml
AndroidManifest.xml
```

Create:

```text
PrimeService.java
```

inside the same Java package as `MainActivity`.

Add the Service to `AndroidManifest.xml`:

```xml
<service
    android:name=".PrimeService"
    android:exported="false" />
```

Practical 8 also requires the notification permission:

```xml
<uses-permission
    android:name="android.permission.POST_NOTIFICATIONS" />
```

## The application accepts a lower and upper bound, searches for prime numbers using a background service, displays the results, and sends a notification when the search is completed.

# Practical 1 — Basic Android App

## Files Required

```text
activity_main.xml
MainActivity.java
```

## Steps

1. Create an Android Studio project.
2. Open `activity_main.xml`.
3. Replace the XML with the Practical 1 XML code.
4. Open `MainActivity.java`.
5. Replace the Java code with the Practical 1 Java code.
6. Save all files.
7. Click **Run ▶**.
8. Select an emulator or connected Android phone.

The application displays the name, qualification, contact, email and address information on the screen.

---

# Practical 2 — Login Check

## Files Required

```text
activity_main.xml
activity_home.xml
MainActivity.java
HomeActivity.java
```

## Steps

1. Create a new Android Studio project.
2. Add the `activity_main.xml` code.
3. Create `activity_home.xml`.
4. Add the home screen XML code.
5. Replace `MainActivity.java`.
6. Create `HomeActivity.java`.
7. Add the `HomeActivity` Java code.
8. Run the application.

## Test Login

Use:

```text
Username: admin
Password: 1234
```

If the credentials are correct, the application opens the Home Activity and displays a welcome message.

If the credentials are incorrect, an invalid username/password message is displayed.

---

# Practical 3 — Email Authentication

## Files Required

```text
activity_main.xml
MainActivity.java
```

## Steps

1. Create a new Android Studio project.
2. Replace `activity_main.xml`.
3. Replace `MainActivity.java`.
4. Save the project.
5. Run the application.

## Test

Enter:

```text
Email: abc@gmail.com
Password: 1234
```

The Login button becomes enabled when the email is valid and the password contains at least 4 characters.

Click **Login** to display:

```text
Login Successful
```

The supplied practical uses `Patterns.EMAIL_ADDRESS` for email validation.

---

# Practical 4 — Options Menu / Color Menu

## Files Required

```text
activity_main.xml
color_menu.xml
MainActivity.java
```

## Steps

1. Create a new Android Studio project.
2. Replace `activity_main.xml`.
3. Right-click `res`.
4. Select:

```text
New
→ Android Resource Directory
```

5. Select:

```text
Resource type: menu
```

6. Click **OK**.
7. Right-click the new `menu` folder.
8. Select:

```text
New
→ Menu Resource File
```

9. Name it:

```text
color_menu
```

10. Paste the Practical 4 menu XML.
11. Replace `MainActivity.java`.
12. Run the application.

## Available Colors

```text
Red
Green
Blue
Yellow
White
```

Selecting a color changes the activity background.

---

# Practical 5 — Handler and Threads

## Files Required

```text
activity_main.xml
MainActivity.java
```

## Steps

1. Create a new Android Studio project.
2. Replace `activity_main.xml`.
3. Replace `MainActivity.java`.
4. Save the project.
5. Run the application.

## Working

Click:

```text
Start
```

The counter starts increasing.

Click:

```text
Stop
```

The counter stops increasing.

The supplied program uses a `Handler`, `Runnable`, and a 1-second delay.

---

# Practical 6 — Asynchronous Task / Progress Bar

## Files Required

```text
activity_main.xml
MainActivity.java
```

## Steps

1. Create a new Android Studio project.
2. Replace `activity_main.xml`.
3. Replace `MainActivity.java`.
4. Save the project.
5. Run the application.
6. Click:

```text
Start Task
```

## Output

The progress bar increases from:

```text
0%
```

to:

```text
100%
```

After completion, the application displays:

```text
Task Completed Successfully!
```

The program performs the increment on a background thread and uses a `Handler` to update the UI.

---

# Practical 7 — Android Service

## Files Required

```text
activity_main.xml
MainActivity.java
MyService.java
AndroidManifest.xml
```

## Steps

1. Create a new Android Studio project.
2. Replace `activity_main.xml`.
3. Replace `MainActivity.java`.
4. Create `MyService.java`.
5. Paste the Practical 7 service code.
6. Open `AndroidManifest.xml`.
7. Add:

```xml
<service
    android:name=".MyService"
    android:enabled="true"
    android:exported="false" />
```

8. Save the project.
9. Run the application.

## Test

Click:

```text
Start Service
```

Every 5 seconds, a Toast appears:

```text
Service is running...
```

Click:

```text
Stop Service
```

The service stops and displays:

```text
Service Stopped
```

The practical specifically uses a background Service with a Handler and `postDelayed()`.

---

# Practical 8 — Notifications / Prime Range

## Files Required

```text
activity_main.xml
MainActivity.java
PrimeService.java
AndroidManifest.xml
```

## Steps

1. Create a new Android Studio project.
2. Use the package:

```text
com.example.primerange
```

3. Replace `activity_main.xml`.
4. Replace `MainActivity.java`.
5. Create:

```text
PrimeService.java
```

6. Paste the Practical 8 `PrimeService.java` code.
7. Open `AndroidManifest.xml`.
8. Add the notification permission:

```xml
<uses-permission
    android:name="android.permission.POST_NOTIFICATIONS" />
```

9. Inside `<application>`, add:

```xml
<service
    android:name=".PrimeService"
    android:exported="false" />
```

10. Save the project.
11. Click **Run ▶**.

## Test

Enter a lower bound:

```text
2
```

Enter an upper bound:

```text
100
```

Click:

```text
Find Primes
```

The application searches the range and displays prime numbers.

When the operation finishes, a notification is generated:

```text
Prime search finished
```

## The supplied practical uses `PrimeService` to perform the search in the background and `ResultReceiver` to send progress/results back to the activity.

# How to Run the Application

After creating the files for any practical:

## Option 1 — Android Emulator

1. Open **Device Manager** in Android Studio.
2. Create an Android Virtual Device if you don't already have one.
3. Start the emulator.
4. Select the emulator from the device dropdown.
5. Click:

```text
Run ▶
```

6. Wait for Gradle to build the application.
7. Android Studio installs and launches the application.

---

## Option 2 — Physical Android Phone

1. Enable **Developer Options** on your Android phone.
2. Enable **USB Debugging**.
3. Connect the phone to your computer using USB.
4. Accept the debugging permission on the phone.
5. Select your phone from Android Studio's device dropdown.
6. Click:

```text
Run ▶
```

7. Android Studio will build and install the application.

---

# Common Errors

## 1. `R.id` not found

Check that the ID in Java exactly matches the ID in XML.

Example:

```xml
android:id="@+id/btnStart"
```

must be referenced as:

```java
R.id.btnStart
```

---

## 2. Package name error

The package declaration at the top of the Java file must match your project's package.

Example:

```java
package com.example.myserviceapp;
```

If you create the project with a different package name, update the Java package declarations consistently.

---

## 3. Activity not found

If an additional Activity such as `HomeActivity` is used, make sure the Java class exists and is registered if required by your project configuration.

---

## 4. Service not found

For Practical 7 and Practical 8, make sure the Service is declared inside the `<application>` section of `AndroidManifest.xml`.

---

## 5. Notification does not appear

For Practical 8 on Android 13 or newer, allow the application's notification permission when Android asks for it.

The practical explicitly requests `POST_NOTIFICATIONS` on Android 13+.

---

# Recommended Repository Structure

For this GitHub repository, keep the TXT files organized like this:

```text
Android-Practicals/
│
├── README.md
│
├── Practical_1_Basic_Android_App.txt
├── Practical_2_Login_Check.txt
├── Practical_3_Email_Authentication.txt
├── Practical_4_Color_Menu.txt
├── Practical_5_Handler_and_Threads.txt
├── Practical_6_Asynchronous_Task.txt
├── Practical_7_Android_Service.txt
└── Practical_8_Notifications.txt
```

Each TXT file contains the source code required for that practical.

---

# Quick Reference

| Practical | Main Concept                       | Additional Files                                   |
| --------- | ---------------------------------- | -------------------------------------------------- |
| 1         | Basic Android App                  | —                                                  |
| 2         | Login Check                        | `activity_home.xml`, `HomeActivity.java`           |
| 3         | Email Authentication               | —                                                  |
| 4         | Options Menu                       | `color_menu.xml`                                   |
| 5         | Handler and Threads                | —                                                  |
| 6         | Asynchronous Task                  | —                                                  |
| 7         | Android Service                    | `MyService.java`, Manifest entry                   |
| 8         | Notifications + Background Service | `PrimeService.java`, Manifest permission + service |

---

## Source Code

The complete source code for all practicals is available in the `.txt` files in this repository.

Clone or download the repository, open Android Studio, create the required project, and copy the corresponding files into their respective locations.
