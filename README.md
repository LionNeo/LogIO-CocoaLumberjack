# LogIO-CocoaLumberjack

[![Version](http://cocoapod-badges.herokuapp.com/v/LogIO-CocoaLumberjack/badge.png)](http://cocoadocs.org/docsets/LogIO-CocoaLumberjack)
[![Platform](http://cocoapod-badges.herokuapp.com/p/LogIO-CocoaLumberjack/badge.png)](http://cocoadocs.org/docsets/LogIO-CocoaLumberjack)

A [log.io](http://logio.org/) logger for [CocoaLumberjack](https://github.com/CocoaLumberjack/CocoaLumberjack).


## Installation

### Using cocoapods

Add the following line to your Podfile:

    pod "LogIO-CocoaLumberjack"

### Manual installation

Simply clone this repository and add the files from the *Classes* directory to your project.

## Usage

Just add the logger to CocoaLumberjack:

``` objective-c
[DDLog addLogger:[LogIOLogger sharedInstance]];
```

Then, configure your node and stream:

``` objective-c 
NSString *deviceName = [[UIDevice currentDevice] name];
NSString *appName = [[[NSBundle mainBundle] infoDictionary] objectForKey:@"CFBundleDisplayName"];
[LogIOLogger configureNode:deviceName stream:appName];
```
