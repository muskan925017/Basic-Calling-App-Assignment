A.Project Objective
The objective of this project is to build a functional calling app UI and basic call flow using Kotlin to demonstrate proficiency in Android fundamentals, UI handling, and state management.

B.Tech Stack
Language: Kotlin 
UI Framework: Jetpack Compose)
Navigation: Jetpack Navigation Component 
Architecture: Basic MVVM-oriented structure 

C.Features Implemented
i) Dial Pad Screen
1. Full numeric keypad (0-9, *, #) for number entry.
2. Dynamic display for the input number.
3. Backspace functionality to edit the entered number.
4. Call button to trigger the outgoing call flow.

i)Dial Pad Screen (Core Input)
Numeric Keypad: A custom-built grid (0-9, *, and #) allowing users to input phone numbers.
Input Validation: Limits input to 10 characters and restricts characters to digits and call symbols only.
Backspace Functionality: A "Close" icon button that allows users to delete the last digit entered one by one.
Special Character Support: Uses URLEncoder and URLDecoder to safely pass numbers containing * and # between screens via Navigation arguments.
Dynamic UI: The "Call" button is positioned at the bottom center using Box alignment for a professional look.

ii).Outgoing Call Screen
Displays the dialed number and a "Calling..." status.
Automatic transition to the Incoming Call screen after a 2-second delay to simulate network ringing.
"End Call" button to cancel the call and return to the dial pad.

iii).Incoming Call Screen
Displays the caller's number.
Accept Button: Transitions the user to the Active Call screen.
Reject Button: Ends the simulation and returns the user to the Dial Pad.

iv).Active Call Screen
Call Timer: A real-time timer starting from 00:00 once the call is accepted.
UI Toggles: Interactive buttons for Mute and Speaker modes (UI state only).
End Call: Terminates the active session and returns to the main screen.

D.Approach & State Management
The application manages the call lifecycle through a clear state machine:Idle → Calling → Incoming → Active → Ended.
Navigation: Used a NavHost to handle transitions. Numbers are passed between screens using string arguments and URLencoding to handle special characters like * and #.
Concurrency: Used LaunchedEffect and coroutines to handle the timer logic and automated screen transitions without blocking the UI thread.
UI/UX: Focused on high responsiveness and ensuring the "End Call" functionality is available at every stage of the process.

E.How to Run
Clone this repository.
Open the project in Android Studio.
Build and run the app on an emulator or physical device.
Alternatively, download and install the APK provided in the submission link.# Basic-Calling-App-Assignment
