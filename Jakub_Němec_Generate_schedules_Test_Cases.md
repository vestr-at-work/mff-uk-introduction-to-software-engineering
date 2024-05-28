# View Preferences - Testing

We are testing the [Use Case 2](https://gitlab.mff.cuni.cz/berkal/nswi041-sch/-/blob/master/USE_CASES.md?ref_type=heads).

## Test Conditions

- T_CONDITION_01: Verify that the user has valid administrator privileges.
- T_CONDITION_02: Verify that the schedule committee has been created and confirmed by its members.
- T_CONDITION_03: Verify that the deadline for adding preferences and constraints has passed.
- T_CONDITION_04: Verify that all teacher preferences and constraints are filled in.
- T_CONDITION_05: Verify that the administrator can navigate to the schedule generation subpage.
- T_CONDITION_06: Verify that the administrator can generate potential schedules by clicking on the "Generate" button.
- T_CONDITION_07: Verify that the scheduling process handles inconsistencies in preferences and constraints correctly.
- T_CONDITION_08: Verify that the generated schedules can be submitted for approval.

## Test Case 1: Successful Schedule Generation

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_01</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Successful Schedule Generation</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has administrator privileges.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Schedule committee created and confirmed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Deadline for adding preferences and constraints has passed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">All teacher preferences and constraints are filled in.</td>
    </tr>    
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Potential schedules are generated and displayed for approval.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Administrator</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2"></td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2"> T_CONDITION_01, T_CONDITION_02, T_CONDITION_03, T_CONDITION_04</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Action: User logs in as an administrator.</td>
        <td>Expected Result: Log in is successful.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Action: User navigates to the schedule generation subpage.</td>
        <td>Expected Result: Access is granted, and the subpage is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Action: User clicks the "Generate" button.</td>
        <td>Expected Result: Scheduling process completes successfully.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Action: Verify that potential schedules are displayed.</td>
        <td>Expected Result: Schedules are displayed for approval.</td>
    </tr>
</table>

## Test Case 2: Inconsistent Preferences and Constraints

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_02</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Inconsistent Preferences and Constraints</td>
    </tr>
    <tr>
        <th>Priority</th>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has administrator privileges.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Schedule committee created and confirmed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Deadline for adding preferences and constraints has passed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Preferences and constraints have inconsistencies.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Preferences and constraints are adjusted, and scheduling process is retried.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Administrator</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Inconsistent preferences and constraints data.</td>
    </trBBBB>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_05, T_CONDITION_04, T_CONDITION_03</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Action: User logs in as an administrator.</td>
        <td>Expected Result: Log in is successful.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Action: User navigates to the schedule generation subpage.</td>
        <td>Expected Result: Access is granted, and the subpage is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Action: User clicks the "Generate" button.</td>
        <td>Expected Result: Scheduling process crashes due to inconsistencies.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Action: User adjusts the preferences and constraints to resolve inconsistencies.</td>
        <td>Expected Result: Preferences and constraints are updated.</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>Action: User retries the schedule generation process.</td>
        <td>Expected Result: Scheduling process completes successfully, and schedules are displayed for approval.</td>
    </tr>
</table>

## Test Case 3: Missing Administrator Privileges

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_03</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Missing Administrator Privileges</td>
    </tr>
    <tr>
        <th>Priority</BBth>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User does not have administrator privileges.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Access is denied.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Non-administrator</td>
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
        <td>Action: User logs in as a non-administrator.</td>
        <td>Expected Result: Log in is successful.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Action: User attempts to navigate to the schedule generation subpage.</td>
        <td>Expected Result: Access is denied, and an error message is displayed.</td>
    </tr>
</table>

## Test Case 4: Unauthorized Access to Teacher Preferences

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_04</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">User has not enough privileges</td>
    </tr>
    <tr>
        <th>Priority</BBth>
        <td colspan="2">Medium</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has teacher role but is not authorized to see other teachers' preferences.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Access is rejected.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Unauthorized Teacher</td>
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
        <td>Action: User logs in as a teacher.</td>
        <td>Expected Result: Log in is successful.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Action: User clicks on "Teacher preferences" in the menu.</td>
        <td>Expected Result: Access is granted, "Teacher preferences" window appears.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Action: The teacher fills in the name of another teacher.</td>
        <td>Expected Result: Access is rejected, teacher is redirected to "Not authorized" error page.</td>
    </tr>
</table>

## Test Case 5: Submission of Generated Schedules for Approval

<table>
    <tr>
        <th>ID</th>
        <td colspan="2">TC_05</td>
    </tr>
    <tr>
        <th>Title</th>
        <td colspan="2">Submission of Generated Schedules for Approval</td>
    </tr>
    <tr>
        <th>Priority</BBth>
        <td colspan="2">High</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">User has administrator privileges.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Schedule committee created and confirmed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Deadline for adding preferences and constraints has passed.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">All teacher preferences and constraints are filled in.</td>
    </tr>
    <tr>
        <th>Preconditions</th>
        <td colspan="2">Schedules are generated.</td>
    </tr>
    <tr>
        <th>Postconditions</th>
        <td colspan="2">Schedules are submitted for approval.</td>
    </tr>
    <tr>
        <th>Role</th>
        <td colspan="2">Administrator</td>
    </tr>
    <tr>
        <th>Test Data</th>
        <td colspan="2">Generated schedules data.</td>
    </tr>
    <tr>
        <th>Covered Test Conditions</th>
        <td colspan="2">T_CONDITION_01, T_CONDITION_02, T_CONDITION_03, T_CONDITION_04</td>
    </tr>
    <tr>
        <th>Test steps</th>
        <th>Action</th>
        <th>Expected result</th>
    </tr>
    <tr>
        <td>1.</td>
        <td>Action: User logs in as an administrator.</td>
        <td>Expected Result: Log in is successful.</td>
    </tr>
    <tr>
        <td>2.</td>
        <td>Student is in the main menu</td>
        <td>Expected Result: Access is granted, and the subpage is displayed.</td>
    </tr>
    <tr>
        <td>3.</td>
        <td>Action: User navigates to the schedule generation subpage.</td>
        <td>Expected Result: Scheduling process completes successfully.</td>
    </tr>
    <tr>
        <td>4.</td>
        <td>Action: Verify that potential schedules are displayed.</td>
        <td>Expected Result: Schedules are displayed for approval.</td>
    </tr>
    <tr>
        <td>5.</td>
        <td>Action: User submits the generated schedules for approval.</td>
        <td>Expected Result: Schedules are submitted, and a confirmation is received.</td>
    </tr>
</table>
