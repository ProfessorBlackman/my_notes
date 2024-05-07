Implementing each of the alternative triggering methods requires a combination of Flutter code and platform-specific code using platform channels. Here's a brief overview of how you might approach implementing each method:

1. **Volume Button Press:**
   Implement a platform channel to listen for volume button presses. This will involve using native code to capture the button events and then communicating them to Flutter using platform channels.

2. **Shake Gesture:**
   Use the device accelerometer to detect shakes. You can use the `sensors` package in Flutter to access accelerometer data and implement shake detection logic.

3. **Screen Gesture:**
   Use the `GestureDetector` widget to capture specific gestures on the screen. You'll need to define the gesture pattern and trigger the SMS function when the gesture is recognized.

4. **Voice Command:**
   Integrate a speech recognition library, such as the `speech_to_text` package, to convert spoken words into text. Define specific phrases as triggers and initiate the SMS function when the trigger phrase is detected.

5. **Hardware Button (Fingerprint, Dedicated Button):**
   This might be more complex and device-specific. You'll need to research how to access the hardware button's events or actions. Platform channels would be involved to communicate between Flutter and the native code.

6. **In-App Button:**
   Simply design a button within your app's UI that, when tapped, initiates the SMS sending function. This can be done using standard Flutter widget interactions.

7. **Timer:**
   Implement a timer that starts when the emergency trigger is activated. If the timer expires without being canceled by the user, the emergency SMS is sent.

8. **Location-Based Triggers:**
   Use location services and geofencing to detect when the user enters or exits specific locations. When a trigger location is detected, initiate the SMS sending function.

Remember, for each method, you'll need to integrate platform-specific code (Java/Kotlin for Android, Objective-C/Swift for iOS) using platform channels. The specifics of implementing these methods can vary widely based on the platform and the libraries you choose to use.

Additionally, I recommend checking the Flutter community for any available plugins or packages that might simplify the implementation of these features. The Flutter ecosystem is quite active, and there might be existing solutions or libraries that could save you development time.