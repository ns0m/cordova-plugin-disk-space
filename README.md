### Publication-only version of the [sqli/sqli-cordova-disk-space-plugin](https://github.com/sqli/sqli-cordova-disk-space-plugin) package with some fixes. [![Latest Published Version](https://img.shields.io/npm/v/cordova-plugin-ns0m-disk-space)](https://www.npmjs.com/package/cordova-plugin-ns0m-disk-space)
```
cordova plugin add cordova-plugin-ns0m-disk-space
```

---

# Disk Space Plugin
This plugin allows getting information about disk space in Android / iOS / Windows 10 platforms.

## Installation
To use this plugin in a project, you have to do:

	cordova plugin add sqli-cordova-disk-space-plugin

Add your targeted platforms:

	cordova platform add android
	cordova platform add ios
	cordova platform add windows

## Usage

1- You can get disk information by executing the `info` function:

	DiskSpacePlugin.info(options, successCallback, errorCallback);

Where _options_ is a javascript object:

	location: 1 // To get information about external storage (For android only)
	location: 2 // To get information about internal storage (For android only)

The result object is like that:

	{
		"app": 29887, // Space occupied by the current application
		"total": 98717873000, // Total space of the device
		"free": 76556280  // Free space of the device
	}
