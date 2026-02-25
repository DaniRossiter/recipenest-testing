# RecipeNest Test Plan

## 1. Objective

The objective of this test plan is to verify that the main features of RecipeNest work as expected and provide a reliable user experience. 

This includes identifying bugs, checking behaviour, and reducing the risk of users encountering errors.

## 2. Scope

### In Scope
- User registration
- User login
- Searching recipes
- Viewing recipe list and recipe details
- Adding recipes (logged-in users)
- Viewing recipes (logged-in users)
- Editing recipes (logged-in users)
- Deleting recipes (logged-in users)

### Out of Scope (for now)
- Performance testing
- Security testing
- Accessibility testing
- Cross-browser testing on multiple devices
- Automated testing

## 3. Test Approach

Testing will begin by using the site as a normal user without being logged in. The functionality of searching and viewing recipes will be tested to confirm that they work as expected.

After that, negative testing will be performed by trying to break features using invalid inputs, empty fields, and unexpected behaviour.

User registration and login will also be tested using both valid and invalid details.

The same approach will be repeated while logged in, which will include testing recipe creation, viewing the logged-in user's recipes, editing, and deletion.

Both positive (expected behaviour) and negative (invalid or unexpected behaviour) scenarios will be tested.

## 4. Risks

- Users might not be able to register or log in if validation or backend logic fails.
- The same user could potentially register multiple times if duplicate checks are not handled properly.
- Users might be able to edit or delete recipes that are not theirs if authorization is not enforced correctly.
- Invalid input could break the UI or cause display issues.
- Data could be saved incorrectly or stored in the wrong format in the database.
- There could be potential security risks, such as SQL injection, if input is not validated properly.

## 5. Entry and Exit Criteria

### Entry Criteria
- The site is deployed and accessible.
- The features listed in scope are available to test.

### Exit Criteria
- All planned tests have been run.
- All bugs found have been logged.
- A final review of the test results has been completed.
