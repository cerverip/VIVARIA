
### Folder description

- `Profiles/` contains the `profiles.json` file with the saved profiles.
- `TaskStatistics/` contains one folder for each profile.
- Each profile folder contains the saved data related to the tasks completed by that profile.

SETUP

1. UNITY

  a. Version 6000.3.10f1

2. ULTRALEAP SETUP GUIDE

  a. Install Ultraleap Tracking Software
  
     * Go to Ultraleap official website: https://www.ultraleap.com/downloads/3di/
     * Select the operating system you are using (Windows, macOS, or Linux).
     * Download Ultraleap Hyperion
     
  b. Install the software by following the on-screen instructions
  
  c. Connect the Ultraleap device to your computer using the provided USB cable
  
  d. Open the Ultraleap Hyperion software and ensure that your device is recognized
  
  e. Calibrate the device using the calibration tool in the Ultraleap software to ensure accurate tracking
  
  f. Test the device by moving your hands in front of it and observing the tracking data in the software

3. BUILD
   
  a. Download the latest release
  
  b. Open the exe file

4. GITHUB PROJECT SETUP GUIDE
   
  a. Clone the repo
  
  b. Add the "rat\_anatomy\_fbx" folder to the local path: "Assets\\3DModels\\RatModels\\"
  
  c. Add the "Video" folder to "Assets\\"
  
  d. Remove the [SerializeField] tag in the "Capsule Hands" script to remove the error in the editor
  
  e. Ignore the check that Ultraleap does for PhysicalHandsSettings to remove the error in the editor
  
  f. Run in the editor from the ProfileScene and test that everything works fine


## SAVED FILES

The application saves its local data in the following directory:

`C:\Users\"USER_NAME_IN_YOUR_PC"\AppData\LocalLow\POLIMI\VIVARIA`

Inside the `VIVARIA` folder, the saved data is organized like this:

```text
VIVARIA/
├── Profiles/
│   └── profiles.json
└── TaskStatistics/
    ├── profile_id_1/
    │   ├── first_task_name_1
    │   ├── first_task_name_2
    │   ├── second_task_name_1
    │   └── third_task_name_1
    ├── profile_id_2/
    │   └── ...
    └── ...
```
# Example of the content of a task file

```json
{
    "taskName": "Jaw blood collection",
    "profileId": "78c9cad7-f6b5-44e1-b1e2-9d6f75ed2694",
    "totalTime": 28.437463760375978,
    "totalCriticalErrors": 0,
    "totalManualRewinds": 0,
    "successfulGrabCount": 10,
    "failedGrabAttemptCount": 5,
    "totalGrabAttemptCount": 15,
    "grabbedObjectsWithHandInOrder": [
        {
            "objectName": "cage",
            "hand": "left"
        },
        {
            "objectName": "mouse",
            "hand": "left"
        },
        {
            "objectName": "mouse",
            "hand": "left"
        },
        {
            "objectName": "mouse",
            "hand": "left"
        },
        {
            "objectName": "needle",
            "hand": "right"
        },
        {
            "objectName": "capillarytube",
            "hand": "right"
        },
        {
            "objectName": "mouse",
            "hand": "right"
        },
        {
            "objectName": "mouse",
            "hand": "right"
        },
        {
            "objectName": "needle",
            "hand": "right"
        },
        {
            "objectName": "needle",
            "hand": "right"
        }
    ],
    "completionDateString": "2026-03-11T16:57:32.0413202+01:00",
    "stepStats": [
        {
            "stepName": "Workbench Placement Step",
            "criticalErrors": 0,
            "manualRewinds": 0,
            "stepTotalTimeSeconds": 9.303930282592774,
            "events": [
                {
                    "eventType": "completed",
                    "deltaSeconds": 9.303930282592774
                }
            ]
        },
        {
            "stepName": "Jaw Blood Sample",
            "criticalErrors": 0,
            "manualRewinds": 0,
            "stepTotalTimeSeconds": 10.240579605102539,
            "events": [
                {
                    "eventType": "completed",
                    "deltaSeconds": 10.240579605102539
                }
            ]
        },
        {
            "stepName": "Cage Placement Step",
            "criticalErrors": 0,
            "manualRewinds": 0,
            "stepTotalTimeSeconds": 5.42393684387207,
            "events": [
                {
                    "eventType": "completed",
                    "deltaSeconds": 5.42393684387207
                }
            ]
        },
        {
            "stepName": "Dispose sharp objects",
            "criticalErrors": 0,
            "manualRewinds": 0,
            "stepTotalTimeSeconds": 3.4690170288085939,
            "events": [
                {
                    "eventType": "completed",
                    "deltaSeconds": 3.4690170288085939
                }
            ]
        }
    ]
}
```
