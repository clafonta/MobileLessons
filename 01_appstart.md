# App Startup	

The customer has freshly downloaded the app from Google Play or the App Store and is about to start the app. In this case, we're running a financial app, which requires a different set of needs and care as compared to a utility, game, or social app. Key customer concerns are security, accuracy, and availability. Upon the app startup, we need to look out for the following things in this order: 

## 1. Customer's Device

We need to verify a few things: 
* **Is this a device we support?** Maybe the customer side loaded the app. Maybe we didn't properly configure our account with Google Play or the AppStore. Maybe the customer hasn't used the app in several years (think Windows Phone).
* **Is this an OS version we support?** We need to take a stand and not support early OS versions, e.g., Android 2.2. 
* **Is this device connected to the internet?** Think airplane mode. We don't want our application heavily dependent on an initialization file upon startup. 
* **Does this device have a strong wifi/cell connection?** If we have a weak connection, do we want to notify the customer? Not all customers are technically savvy. 
* **Is this customer's device rooted?** There are several products which we can use to help detect rooted devices and there are many reasons why we should be aware of this. *Important*: Don't block a customer with a rooted device. Falsly flagging a rooted device and blocking a customer from using the app leads to negative customer feedback. Instead, take account of this data point on the backend and review it with your data science team.  

## 2. Backend System Availability

After the customer passes all device and connectivity checks, we then need to ensure our backend services are in a good state. 

* **Are we in maintenance mode?** We should have a system notification letting the customer know "hey, we're in read only mode for the next few hours"
* **Disaster messaging**  Disasters happen: hurricanes, fires, data center meltdowns, DDoS attacks, system breaches, etc. We should take this opportunity to message the customer of our awareness and how we're addressing it. 

## 3. First Time Usage

At this point, we've ensured the customer's device is supported and our systems are healthy and running. For first time users, we need to balance out cross sell ads, welcome messages, out-of-box experiences, "what's new", and more. 


[Previous](00_intro.md) | [Next](02_appcode.md)




