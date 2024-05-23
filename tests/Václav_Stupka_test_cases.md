# use case 8 (Find preferences of other teachers)

[Use Case 8 – source](https://gitlab.mff.cuni.cz/berkal/nswi041-sch/-/blob/37ac2959e6f4a70dd23a790f7687d37566dd2e50/USE_CASES.md#use-case-8-find-preferences-of-other-teachers)

### test conditions
- Test_Con_1 – User is logged as a teacher.
- Test_Con_2 – User is not logged as a teacher.
- Test_Con_3 – Teacher is authorize to see preferences of other teachers.
- Test_Con_4 – Teacher is not authorize to see preferences of other teachers.
- Test_Con_5 – Searched teacher is not found.
- Test_Con_6 – Selected teacher has not submitted their preferences.
- Test_Con_7 – Selected teacher has submitted their preferences.
- Test_Con_8 – Show preferences of the selected teacher.

### test case 1

| ID | TC_1 |
| -------------- | ----------- |
| Title          | Find preferences – successful |
| Priority       | High |
| Preconditions  | User has teacher role, is authorised to see other teachers preferences, other teacher has submitted their preferences |
| Postconditions | Preferences are shown |
| Role           | Authorised Teacher |
| Test data      | |
| Covered Test Conditions | Test_Con_1, Test_Con_3, Test_Con_7, Test_Con_8  |

| Steps | Action | Expected result |
| --- | --- | --- |
| 1) | User logs in as a teacher. | Log in is successful. |
| 2) | User clicks on "Teacher preferences" in the menu. | Access is granted, "Teacher preferences" window appears. |
| 3) | The teacher fills in the name of the other teacher. | A selection menu with matching teachers is shown. |
| 4) | The teacher selects the other teacher in a selection menu. | The list of selected teacher's preferences is shown. |

### test case 2

| ID | TC_2 |
| -------------- | ----------- |
| Title          | Teacher not found |
| Priority       | Medium |
| Preconditions  | User has teacher role, is authorised to see other teachers preferences, selected teacher does not exist |
| Postconditions | Warning is shown |
| Role           | Authorised Teacher |
| Test data      | |
| Covered Test Conditions | Test_Con_1, Test_Con_3, Test_Con_7, Test_Con_8  |

| Steps | Action | Expected result |
| --- | --- | --- |
| 1) | User logs in as a teacher. | Log in is successful. |
| 2) | User clicks on "Teacher preferences" in the menu. | Access is granted, "Teacher preferences" window appears. |
| 3) | The teacher fills in the name of the other teacher. | A selection menu with matching teachers is shown. |
| 4) | The teacher selects the other teacher in a selection menu. | Teacher is redirected to "Preferences not filled" error page. |

### test case 3

| ID | TC_3 |
| -------------- | ----------- |
| Title          | Preferences not submitted |
| Priority       | Medium |
| Preconditions  | User has teacher role, is authorised to see other teachers preferences, |
| Postconditions | Warning is shown |
| Role           | Authorised Teacher |
| Test data      | |
| Covered Test Conditions | Test_Con_1, Test_Con_6  |

| Steps | Action | Expected result |
| --- | --- | --- |
| 1) | User logs in as a teacher. | Log in is successful. |
| 2) | User clicks on "Teacher preferences" in the menu. | Access is granted, "Teacher preferences" window appears. |
| 3) | The teacher fills in the name of the other teacher. | Teacher is redirected to "Teacher not found" error page. |

### test case 4

| ID | TC_4 |
| -------------- | ----------- |
| Title          | User has not enough privilegia |
| Priority       | Medium |
| Preconditions  | User has teacher role, but is not authorised to see other teachers preferences |
| Postconditions | Access is rejected |
| Role           | Unauthorised Teacher |
| Test data      | |
| Covered Test Conditions | Test_Con_1, Test_Con_4  |

| Steps | Action | Expected result |
| --- | --- | --- |
| 1) | User logs in as a teacher. | Log in is successful. |
| 2) | User clicks on "Teacher preferences" in the menu. | Access is granted, "Teacher preferences" window appears. |
| 3) | The teacher fills in the name of the other teacher. | Access is rejected, teacher is redirected to "Not authorized" error page. |

### test case 5

| ID | TC_5 |
| -------------- | ----------- |
| Title          | User is not a teacher |
| Priority       | High |
| Preconditions  | User does not have teacher role preferences |
| Postconditions | Access is rejected |
| Role           | Basic user |
| Test data      |  |
| Covered Test Conditions | Test_Con_2  |

| Steps | Action | Expected result |
| --- | --- | --- |
| 1) | User logs in not as a teacher. | Log in is successful. |
| 2) | User clicks on "Teacher preferences" in the menu. | Access is rejected, user is redirected to "Not authorized" error page. |

