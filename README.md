# Regula Document Reader (Android version)

The DocumentReader is a SDK for identification documents reading and validation which is working fully **offline**. It contains two parts: **API** for frameworks users. And **Core** that performs all main logic. [Just take me to the notes!](https://github.com/regulaforensics/DocumentReader-Android/wiki)

If you have any questions, feel free to [contact us](mailto:support@regulaforensics.com).

<img src="DocumentReaderDemo_default.png" width="250"> <img src="DocumentReaderDemo_process.png" width="250"> <img src="DocumentReaderDemo_result.png" width="250">

#

* [How to build demo application](#how_to_build_demo_application)
* [How to add DocumentReader library to your project](#how_to_add_documentreader_library_to_your_project)
* [Troubleshooting license issues](#troubleshooting_license_issues)
* [Documentation](#docs)
* [Additional information](#additional_information)

## <a name="how_to_build_demo_application"></a> How to build demo application
1. Get trial license for demo application at [licensing.regulaforensics.com](https://licensing.regulaforensics.com) (`regula.license` file).
1. Clone current repository using command `git clone https://github.com/regulaforensics/DocumentReader-Android.git`.
1. Download and install latest [JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html).
1. Download and install latest [Android Studio](https://developer.android.com/studio/index.html).
1. Copy file `regula.license` to `DocumentReader-sample/app/src/main/res/raw` folder. 
1. Launch Android Studio and select _Open an existing Android Studio project_ then select _DocumentReader-sample_ project in file browser.
1. Download additional files proposed by Android Studio to build project (build tools, for example).
3. Change application ID to specified during registration of your license key at [licensing.regulaforensics.com](https://licensing.regulaforensics.com) (`com.regula.documentreader` by default).
1. Select appropriate build variant and run application.

## <a name="how_to_add_documentreader_library_to_your_project"></a> How to add DocumentReader library to your project

DocumentReader libraries are available in our [Maven repository](http://maven.regulaforensics.com/RegulaDocumentReader/com/regula/documentreader/). To install
them, simply add the following lines to your build.gradle

* Loading full library edition:
```java
implementation 'com.regula.documentreader.fullrfid:core:+@aar'	
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install Core library edition:
```java
implementation 'com.regula.documentreader.core:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install Bounds library edition:
```java
implementation 'com.regula.documentreader.bounds:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install Barcode library edition:
```java
implementation 'com.regula.documentreader.barcode:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install MRZ library edition:
```java
implementation 'com.regula.documentreader.mrz:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install MRZ-Barcode library edition:
```java
implementation 'com.regula.documentreader.barcodemrz:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install OCR library edition:
```java
implementation 'com.regula.documentreader.ocrandmrz:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```
* Install Bank Card library edition:
```java
implementation 'com.regula.documentreader.creditcard:core:+@aar'
implementation ('com.regula.documentreader:api:+aar'){
	transitive = true
}
```

## <a name="troubleshooting_license_issues"></a> Troubleshooting license issues
If you have issues with license verification when running the application, please verify that next is true:
1. OS you are using is the same as in the license you received (Android).
1. Application ID is the same that you specified for license.
1. Date and time on the device you are trying to run the application is correct and inside the license validity term.
1. You are using the latest release of the SDK.
1. You placed the license into the correct folder as described here [How to build demo application](#how_to_build_demo_application) (`DocumentReader-sample/app/src/main/res/raw`).

## <a name="docs"></a> Documentation
You can find documentation on API [here](https://regulaforensics.github.io/DocumentReader-Android/).

## <a name="additional_information"></a> Additional information
If you have any questions, feel free to contact us at support@regulaforensics.com
