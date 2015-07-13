# Building watchOS apps

## MobileOptimized 2015

### Boris Bügling - @NeoNacho

![20%, original, inline](images/contentful.png)

![](images/button.gif)

<!--- use Poster theme, black -->

---

## CocoaPods

![](images/cocoapods.jpg)

---

## Contentful

![](images/contentful-bg.png)

---

![](images/who.gif)

---

# 💰💰💰💰

![](images/money.gif)

---

# ᴡᴀᴛᴄʜ

![](images/rorschach-2.gif)

---

# watchOS 1.x

- Notifications
- Glances
- WatchKit apps

![](images/background.jpg)

---

# Notifications

![inline](images/apple-notifications.png)

![](images/background.jpg)

---

# Glances

![inline](images/apple-glances.png)

![](images/background.jpg)

---

# WatchKit

![inline](images/apple-watchkit.png)

![](images/background.jpg)

---

# watchOS 2.x

- Apps run natively on the watch
- Custom complications

![](images/background.jpg)

---

# !!!

![](images/blast.gif)

---

![](images/apple-native.jpg)

---

# Complications

![inline](images/apple-complications.png)

![](images/background.jpg)

---

# Architecture

![](images/ozymandias.gif)

---

![inline](images/app-comm.png)

![](images/background.jpg)

---

# watchOS 2

Extension

phone => watch

![](images/rorschach-comic.gif)

---

# Resources

- Interface.storyboard
- Asset catalogs

![](images/background.jpg)

---

# Extension Delegate

```swift
class ExtensionDelegate: NSObject, WKExtensionDelegate {

    func applicationDidFinishLaunching() {
    }

    func applicationDidBecomeActive() {
    }

    func applicationWillResignActive() {
    }

}
```

---

# Interface Controller

```swift
class InterfaceController: WKInterfaceController {

    override func awakeWithContext(context: AnyObject?) {
        super.awakeWithContext(context)
    }

    override func willActivate() {
        super.willActivate()
    }

    override func didDeactivate() {
        super.didDeactivate()
    }

}
```

---

# WKInterfaceController

- Navigation
- Presentation
- Handoff
- Handle notification actions
- Communicate with parent app

![](images/background.jpg)

---

# Design

![](images/manhattan-2.gif)

---

# Principles

- Lightweight interactions
- Holistic design
- Personal communication

![](images/background.jpg)

---

# Layout

- based on horizontal or vertical groups
- very similar to `UIStackView`
- two device sizes (38mm and 42mm)
- edge-to-edge, bezel provides margins

![](images/background.jpg)

---

![inline](images/interactivity.png)

![](images/background.jpg)

---

# Some examples

![](images/save-us-no.gif)

---

![inline](images/design-fundamentals-customization-hailo_2x.png)

![](images/background.jpg)

---

![inline](images/design-fundamentals-customization-lifesum_2x.png)

![](images/background.jpg)

---

![inline](images/design-fundamentals-customization-rules_2x.png)

![](images/background.jpg)

---

![inline](images/design-fundamentals-customization-spg_2x.png)

![](images/background.jpg)

---

![inline](images/design-fundamentals-customization-transit_2x.png)

![](images/background.jpg)

---

# Building a simple app

![](images/rorschach-1.gif)

---

![inline](images/keynote-watch-app.png)

![](images/background.jpg)

---

# WatchPresenter

- Remote controls Deckset instead
- Direct connection to the Mac
- Shows a preview of the slides
- Measures heartrate to display the "most exciting" slide
- Taps you if you're running out of time

![](images/background.jpg)

---

## Multipeer Connectivity!

![](images/somebody-knows.gif)

---

# Available Frameworks

![](images/rorschach-3.gif)

---

CFNetwork.framework
ClockKit.framework
Contacts.framework
CoreData.framework
CoreFoundation.framework
CoreGraphics.framework
CoreLocation.framework
CoreMotion.framework
EventKit.framework
Foundation.framework

![](images/nite-owl.gif)

---

HealthKit.framework
HomeKit.framework
ImageIO.framework
MapKit.framework
MobileCoreServices.framework
PassKit.framework
Security.framework
UIKit.framework
WatchConnectivity.framework
WatchKit.framework

![](images/comedian.gif)

---

# BT APIs are private :(

![](images/cry.gif)

---

# Other options

- `NSURLSession` via Wi-Fi
- WatchConnectivity.framework to talk via the phone

![](images/background.jpg)

---

# HealthKit.framework

- not usable in the Watch simulator

![](images/skeleton.gif)

---

# Taptic Engine

```objectivec
typedef NS_ENUM(NSInteger, WKHapticType) {
    WKHapticTypeNotification,
    WKHapticTypeDirectionUp,
    WKHapticTypeDirectionDown,
    WKHapticTypeSuccess,
    WKHapticTypeFailure,
    WKHapticTypeRetry,
    WKHapticTypeStart,
    WKHapticTypeStop,
    WKHapticTypeClick
} WK_AVAILABLE_WATCHOS_ONLY(2.0);
```

```swift
WKInterfaceDevice.currentDevice().playHaptic(.Start)
```

---

### but also not usable in the sim

![](images/what-happened-to-dream.gif)

---

# Demo

![](images/dream-came-true.gif)

---

# Tips

![](images/end-is-nigh.gif)

---

# `printf` debugging is great!


![](images/joke.gif)

---

# MMWormhole

- watchOS 1.0: `CFNotificationCenter`
- watchOS 2.0: WatchConnectivity.framework

![](images/minutemen.gif)

---

# Force quit apps

- Long press until "reboot" menu
- Long press again

![](images/background.jpg)

---

## If in doubt, reboot the watch :)

![](images/background.jpg)

---

# What have we learned?

- Code isn't very different from iOS apps
- But design very much is

![](images/background.jpg)

---

# Thank you!

![](images/explosion.gif)

---

- https://developer.apple.com/watch/human-interface-guidelines/
- https://developer.apple.com/library/prerelease/watchos/documentation/General/Conceptual/AppleWatch2TransitionGuide/
- https://github.com/shu223/watchOS-2-Sampler
- http://www.kristinathai.com/category/watchkit/

![](images/manhattan-1.gif)

---

@NeoNacho

boris@contentful.com

http://buegling.com/talks

![](images/manhattan-1.gif)
