# Exe01_StarterCordovaMobileFirst

Adding the MobileFirst Foundation SDK to Cordova Applications.

## Overview

In this tutorial, you learn how to add the MobileFirst SDK to a new or existing Cordova application that has been created with Apache Cordova, Ionic, or another thirdy-party tool. You also learn how to configure the MobileFirst Server to recognize the application, and to find information about the MobileFirst configuration files that are changed in the project.

The MobileFirst Cordova SDK is provided as a set of Cordova plug-ins, and is registered at NPM.

Available plug-ins are:

* **cordova-plugin-mfp** - The core SDK plug-in
* **cordova-plugin-mfp-push** - Provides push notifications support
* **cordova-plugin-mfp-jsonstore** - Provides JSONStore support
* **cordova-plugin-mfp-fips** - Android only. Provides FIPS support
* **cordova-plugin-mfp-encrypt-utils** - iOS only. Provides support for encryption and decryption

### Support levels
The Cordova platform versions supported by the MobileFirst plug-ins, are:

* cordova-ios: **>= 4.1.1 and < 5.0**
* cordova-android: **>= 6.1.2 and <= 7.0**
* cordova-windows: **>= 4.3.2 and < 6.0**

## Getting Started 

Before creating new application or using existing one, we need to install related software.

* [**Node.js**](https://nodejs.org/en/) - Download and install.
* **NPM(3.10.10)** - ``npm install -g npm@3.10.10`` - Run the command in terminal.
* **Codova** - ``npm install -g cordova`` - Run the command in terminal.
* [**JDK 7 or 8**](http://www.oracle.com/technetwork/java/javase/downloads/index.html)- - Download and install.
* **MobileFirst CLI** - ``npm install -g mfpdev-cli`` - Run the command in terminal.
* [**MobileFirst Server**](http://mobilefirstplatform.ibmcloud.com/downloads/#developer-kit) - Download and install.
* [**Gradle**](https://services.gradle.org/distributions/gradle-4.8-bin.zip) - Extract and add path in System variable
* [**Android Studio & SDK**](https://developer.android.com/studio/) - - Download and install.

## New Application

### Step 1: Create a Cordova project

Consider creating the project by using the MobileFirst Cordova application template. The template adds the necessary MobileFirst- specific plug-in entries to the Cordova project’s config.xml file, and provides a MobileFirst-specific, ready-to-use, index.js file that is adjusted for MobileFirst application development.


``cordova create Exe01_StarterCordovaMobileFirst com.androidabcd.helloworld HelloWorld --template cordova-template-mfp``

Where,
* “Exe01_StarterCordovaMobileFirst” is the folder name of the application.
* “com.androidabcd.helloworld” is the ID of the application.
* “HelloWorld” is the Name of the application.
* –template modifies the application with MobileFirst-specific additions.

### Step 2: Change directory to the root of the Cordova project: 
``cd Exe01_StarterCordovaMobileFirst``

### Step 3: Add supported platform (ios|android|windows)
``cordova platform add android``

### Step 4: Prepare the application resources
`` cordova prepare``

## Existing Application

### Step 5: Navigate to the root of your existing Cordova project and add the MobileFirst core Cordova plug-in:
``cordova plugin add cordova-plugin-mfp``

### Step 6: Strat MobileFirst Server:
* From a **Command-line** window, navigate to the extracted folder and execute the run.sh|cmd script to start the MobileFirst Server.

* Load the MobileFirst Operations Console (username/password: admin/admin): [``http://localhost:9080/mfpconsole``](http://localhost:9080/mfpconsole)

### Step 7: Registering the application
``mfpdev app register``

### Step 8: Build the app 
``cordova buld android``

### Step 9: Run the app
``cordova run android``

