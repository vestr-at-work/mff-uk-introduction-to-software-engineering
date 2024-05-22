### Test Conditions

- T_CONDITION_01: All - Teacher logins and has given access rights
- T_CONDITION_02: Preferences - Add preferences
- T_CONDITION_03: Preferences - Edit preferences
- T_CONDITION_04: Preferences - Delete preferences
- T_CONDITION_05: Preferences - Save preferences
- T_CONDITION_06: Preferences - View preferences
- T_CONDITION_07: Preferences - After deadline actions

[Use Case 9 - source](https://gitlab.mff.cuni.cz/berkal/nswi041-sch/-/blob/37ac2959e6f4a70dd23a790f7687d37566dd2e50/USE_CASES.md#use-case-9-edit-preferences)

### Test Case 1 (Use Case 9)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Editing Preferences - Normal flow</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role, User has already specified preferences, It is before deadline</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Users specified preferences changed</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Teacher</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Specified preferences, Deadline date set</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_03, T_CONDITION_05, T_CONDITION_06</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Teacher clicks on "Teacher preferences" in the menu</td>
        <td>The window with list of teachers preferences appears</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Teacher selects the first specified preference</td>
        <td>The first specified preference is marked as selected and modification buttons appear</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Teacher clicks on the "Edit" button on the selected preference</td>
        <td>Editing form with inserted data appears</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Teacher changes beginning of the preference by one hour in the future</td>
        <td>The time of specified preference is rewritten</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>Teacher clicks on "Save" button</td>
        <td>The successful pop-up message appears</td>
    </tr>
    <tr>
        <td>6.</td>
        <td>Teacher verify that the time of edited preference is updated</td>
        <td>The window with updated specified preference is visible</td>
    </tr>
</table>

### Test Case 2 (Use Case 9)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Editing Preferences - Edit not saved</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role, User has specified preferences, It is before the deadline</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Preferences remain unchanged</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Teacher</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Specified preferences, Deadline date set</td>
    </trBBBB>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_06</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Teacher clicks on "Teacher preferences" in the menu</td>
        <td>The window with list of teachers preferences appears</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Teacher selects a specified preference</td>
        <td>The specified preference is marked as selected and modification buttons appear</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Teacher clicks on the "Edit" button on the selected preference</td>
        <td>Editing form with inserted data appears</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Teacher changes beginning of the preference by one hour in the future</td>
        <td>The time of specified preference is rewritten</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>Exit by clicking out of form border</td>
        <td>The form window will close</td>
    </tr>
    <tr>
        <td>6.</td>
        <td>Teacher verifies that the changes were not saved</td>
        <td>The window with unchanged specified preference is visible</td>
    </tr>
</table>

### Test Case 3 (Use Case 9)

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_03</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Editing Preferences - Set preference after deadline</td>
    </tr>
    <tr>
        <th>Priority</BBth>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role, User has not specified preferences, It is after the deadline</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Preferences are not modified</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Teacher</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Deadline date set</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_06, T_CONDITION_07</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Teacher clicks on "Teacher preferencBBBBes" in the menu</td>
        <td>The window with list of teachers preferences appears</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Teacher selects a specified preference</td>
        <td>The specified preference is marked as selected but modification buttons are disabled</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Teacher clicks on "Edit" button</td>
        <td>The pop-up with text: "CANNOT BE EDITED. Is already after deadline, contact ..." appears</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Teacher verifies that the pop-up with text: "CANNOT BE EDITED. Is already after deadline, contact ..." appears</td>
        <td>Verification is valid</td>
    </tr>
</table>
