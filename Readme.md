# Reproduction
- Install app
- Remove the app from recents
- Run  adb shell am start -a android.intent.action.VIEW -d "myapptest://test"
- App starts MainActivity, navigates to SecondActivity and then to ThirdActivity
- Navigate back to SecondActivity
- Run adb shell am start -a android.intent.action.VIEW -d "myapptest://test" again
- Third activity is not opened
- There's a message "Warning: Activity not started, intent has been delivered to currently running top-most instance." in terminal even though MainActivity which handles deeplinks has nohistory flag and is not running