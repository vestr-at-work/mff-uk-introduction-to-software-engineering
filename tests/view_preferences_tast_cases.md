# View Preferences - Testing

We are testing the [Use Case 10](https://gitlab.mff.cuni.cz/berkal/nswi041-sch/-/blob/37ac2959e6f4a70dd23a790f7687d37566dd2e50/USE_CASES.md#use-case-10-view-preferences).

## Test Conditions

- T_CONDITION_01: Role of the user (should be logged as a teacher)
- T_CONDITION_02: Empty preferences (impossible to view preferences)
- T_CONDITION_03: State of the preferences after viewing stays the same
- T_CONDITION_04: Visibility of the button "Teacher preferences" when logged in as a student (should not be visible)
- T_CONDITION_05: Visibility of the button "Teacher preferences" when logged in as a teacher (should be visible)
- T_CONDITION_06: Editing preferences while viewing them should fetch new data
- T_CONDITION_07: Clicking the "Teacher preferences" button shows correct preferences

## Test Case 1

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Viewing Preferences - Normal flow</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role, User preferences specified, User is in the main menu</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Users preferences have not changed</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Teacher</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Teacher preferences</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2"> T_CONDITION_03, T_CONDITION_05, T_CONDITION_07</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Teacher is in the main menu.</td>
        <td>Button "Teacher preferences" button can be seen.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Teacher clicks on "Teacher preferences" button in the menu</td>
        <td>The window with list of teachers preferences appears</td>
    </tr>
</table>

## Test Case 2

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Viewing Empty Preferences</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role, User has no specified preferences</td>
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
        <td colspan="2">Empty preferences</td>
    </trBBBB>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_02</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Teacher is in the main menu</td>
        <td>Button "Teacher preferences" can be seen.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Teacher clicks on the "Teacher prefereces" button</td>
        <td>Dialog window informing the user that no preferences are speficied is shown</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Teacher clicks on the "OK" button in the dialog window</td>
        <td>Window is closed and the view is back to main menu</td>
    </tr>
</table>

## Test Case 3

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_03</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Viewing preferences as a student</td>
    </tr>
    <tr>
        <th>Priority</BBth>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has student role</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2"></td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Student</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2"></td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_01, T_CONDITION_04</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Student is in the main menu</td>
        <td>Button "Teacher preferences" can not be seen or clicked.</td>
    </tr>
</table>