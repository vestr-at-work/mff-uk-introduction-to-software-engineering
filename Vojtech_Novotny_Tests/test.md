# Use Case 7 (Add preferences)

### 1. Initial Assumption

- The user has teacher role
- The preferences are open to changes - it's before the scheduling is in progress


### 2. Normal
1. The teacher clicks on "Teacher preferences" in the menu
2. The teacher selects their day and time preferences as they like
3. The teacher submits their preferences and saves them
4. The teacher receives a pop-up messages indicating that their preferences were saved.


### 3. What Can Go Wrong
- The preferences are in invalid times/days - eg. at night or weekends.
- The scheduling has already started


### 4. System State on Completion
- Teacher preferences are saved.
- Teacher can now see their preferences

# Test conditions
 - **Test_Con1** - User has teacher role
 - **Test_Con2** - User doesn't have teacher role
 - **Test_Con3** - Scheduling is not in progress
 - **Test_Con4** - Scheduling is already in progress
 - **Test_Con5** - Scheduling started being in progress mid adding
 - **Test_Con6** - Selecting invalid day
 - **Test_Con7** - Selecting invalid time
 - **Test_Con8** - Preference saving
 - **Test_Con9** - Not saving upon selecting preferences
 - **Test_Con10** - Pop-up message
 - **Test_Con11** - Teacher doesn't select any times/dates
 - **Test_Con12** - Selecting valid times
 - **Test_Con13** - Submitting invalid datetime


# Test Cases
| **ID**                      |TEST_CASE_1|
| --------------------------- | ---------- |
| **Title**                   |The healthy path|
| **Priority**                |High|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is not yet in progress |
| **Post conditions**         |Inputed preferences are saved and pop-up is displayed.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con1, Test_Con3, Test_Con8, Test_Con10, Test_Con12|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu | Teacher preferences tab loades and teacher can see the interactive calendar | 
| **2.**                      |Teacher selects a valid date and time| Selected times are highlighted| 
| **3.**                      |Teacher submits his preferences|A pop-up appears, informing user of the save. Teacher can now see their inputed preferences|
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_2|
| --------------------------- | ---------- |
| **Title**                   |Invalid dateTime|
| **Priority**                |High|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is not yet in progress. |
| **Post conditions**         |Preferences are not saved, error pop-up is displayed.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con6, Test_Con7, Test_Con13|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu | Teacher preferences tab loades and teacher can see the interactive calendar| 
| **2.**                      |Teacher selects an invalid date and time combination|Selected times are highlighted red| 
| **3.**                      |Teacher tries to submit his preferences| A pop-up appears, informing user that he selected invalid time or date and save was unsuccesful. |
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_3|
| --------------------------- | ---------- |
| **Title**                   |Scheduling already started|
| **Priority**                |High|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is in progress. |
| **Post conditions**         |Preferences are not saved, error pop-up is displayed.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con4|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu |Teacher preferences tab loades and teacher can see the interactive calendar| 
| **2.**                      |Teacher tries to select a date and time combination | A pop-up appears, informing user that preferences are already locked | 
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_4|
| --------------------------- | ---------- |
| **Title**                   |Scheduling started after opening "Teacher preferences"|
| **Priority**                |Low|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is not yet in progress. |
| **Post conditions**         |Preferences are not saved, error pop-up is displayed.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con5|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu |Teacher preferences tab loades and teacher can see the interactive calendar| 
| **2.**                      |Teacher selects a valid date and time combination |Selected times are highlighted| 
| **3.**                      |Scheduling starts.|A pop-up appears, informing user that cannot add his preferences anymore.| 
| **4.**                      |Teacher tries to submit their preferences.|  A pop-up appears, informing user that preferences are already locked.| 
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_5|
| --------------------------- | ---------- |
| **Title**                   |Leaving without saving the preferences|
| **Priority**                |Medium|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is not yet in progress. |
| **Post conditions**         |Preferences are not saved.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con9|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu |Teacher preferences tab loades and teacher can see the interactive calendar| 
| **2.**                      |Teacher selects a valid date and time combination |Selected times are highlighted| 
| **3.**                      |Teacher tries to leave the page|A pop-up appears, informing user that his preferences will not be saved| 
| **4.**                      |Teacher leaves the page|System does not save preferences| 
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_6|
| --------------------------- | ---------- |
| **Title**                   |Non-teacher tries to access teacher schedule|
| **Priority**                |High|
| **Preconditions**           |Scheduling is not yet in progress. |
| **Post conditions**         |User is redirected to an error page.|
| **Role**                    |Not Teacher (=User)|
| **Test data**               |            |
| **Covered test conditions** |Test_Con2|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |User tries to access "Teacher preferences"|Access is denied, user is redirected to an error page, informing him that he will burn in hell.| 
<br />
---
<br />
<br />

| **ID**                      |TEST_CASE_7|
| --------------------------- | ---------- |
| **Title**                   |No dateTime selected|
| **Priority**                |High|
| **Preconditions**           |Teacher is signed into his account. He does not have any preferences saved. Scheduling is not yet in progress. |
| **Post conditions**         |Preferences are not saved, error pop-up is displayed.|
| **Role**                    |Teacher|
| **Test data**               |            |
| **Covered test conditions** |Test_Con11|
<br />

| **Test steps**              | **Action** | **Expected result** |
|---|---|---|
| **1.**                      |Teacher clicks on "Teacher preferences" in the menu |Teacher preferences tab loades and teacher can see the interactive calendar| 
| **2.**                      |Teacher tries to submit their preferences.|A pop-up appears, informing user that he must select a time and date| 
<br />


