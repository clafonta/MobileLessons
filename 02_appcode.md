# App Code

OK, this section isn't about _how_ the app is coded but rather the minimum set of tools and concepts for UI and QA engineers to be able to do their job efficiently and build solid App Code.

## App Architecture

This is a very broad topic and requires lots of discussions and difficult decisions. Saving this topic for another day.

## Environment Picker and Console

The non-production build should have a secret control panel to allow the engineer to pick an environment, e.g. 'local', qa1, qa2, uat, perf', etc. In addition, the console should provide meta data (app version, build, date), and debug information. 

## Mock Services

It's really important for the engineer to run everything on a laptop, not connected to the internet. This requires a mock server to replicate back-end services and provides the following benefits: 

* **Avoid downtime:** There are too many times when a QA/dev environment is broken, unavailable, slow, etc. 
* **Experience chaos:** With a mock environment, the engineer should be able to vet out the app when bad things happen. For example:
 * _No connection release:_ does your app properly handle connection timeouts? Try making a network call that the server never releases. 
 * _Garbage responses:_ does your app properly handle invalid data? 
 * _Slow responses:_ does your app properly handle slow responses and thread management?
* **Future services:** engineers should be able to create screens without the need to wait for back end services to be created. App and Service/API engineers can agree on a contract e.g. http://json-schema.org, the app engineer can stub out the future service, and start coding the app and screen immediately. 
* **Edge cases:** with control of mock services, an engineer can test bizarre cases, like names with special characters, descriptions that are very long in length (does this cause UI reflow?), etc.

## Testing

There are many great testing tools and I leave it up to the engineers to decide what works best for them. At minimum, the app must have a blend of unit, functional, automated, and manual tests. 

* **Unit and functional testing:** Good primer reads for [Android](https://developer.android.com/training/testing/unit-testing/) and [iOS](https://developer.apple.com/documentation/xctest).
* **Automated:** It's unstable to point automated testing to real non-prod/test environments. There are too many false positives. Automated testing should leverage the mock services as mentioned above. Data is known, repeatable, always available, and stable. 
* **Manual testing:** All engineers and testers will need access to real devices. There are too many physical actions that can't be replicated with virtual devices. We need a large set of physical interaction like swiping, scrolling, changing from portrait to landscape, etc. to ensure the app performs as expected.  
* **Device library:** The more device permutations you have on hand, the better, especially with Android. It's good to have a few brand new, entry level, cheap hardware devices on hand. Test with a mix of OS versions, screen sizes, tablets, landscape vs. portrait.

---

__Android is weird:__ We had two Samsung devices, same device, same OS, but could only reproduce a bug on 1 of them. We made sure we had the exact same OS version, same settings, same app version, etc. That is just one story of _many, many_ odd Android dev and testing experiences. What works on a Pixel 2 running Android P, doesn't mean it will work on a Samsung Note running Android P. 

---

[Previous](01_appstart.md) | [Next](03_uidesign.md)