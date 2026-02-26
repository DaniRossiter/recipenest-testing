# RecipeNest Manual Test Cases

## Introduction

This document contains manual test cases to verify the core functionality of RecipeNest.

The test cases are based on the scope defined in the Test Plan and focus on the main user journeys within the web application.

## 1. Public Access (Not Logged In)

This section covers testing for users who are not logged in.

### TC-001 - Landing page buttons navigate correctly

**Preconditions:**
User is not logged in.

**Steps:**
1. Open the RecipeNest home page.
2. Click the "Browse Recipes" button.
3. Observe which page loads.
4. Return to the home page.
5. Click the "Login" button.
6. Observe which page loads.

**Expected Result:**
Clicking "Browse Recipes" should navigate to the recipes page.
Clicking "Login" should navigate to the login page.
No error messages should be displayed.

### TC-002 - Viewing a recipe displays correct details

**Preconditions:**  
User is not logged in.  
At least one recipe exists in the system.

**Steps:**  
1. Open the RecipeNest home page.  
2. Click the "Browse Recipes" button.  
3. Click on any recipe from the list.  
4. Observe the recipe details page.

**Expected Result:**  
The selected recipe's details page should load.  
The recipe title, serving size, description, ingredients, and instructions should be displayed correctly.  
No error messages should be shown.

### TC-003 - Back button returns user to recipe list

**Preconditions:**
User is not logged in.
User is currently viewing a recipe details page.

**Steps:**
1. Scroll to the bottom of the recipe details page.
2. Click the "Back" button.
3. Observe the page that loads.

**Expected Result:**
The user should be navigated back to the recipes list page.
The list of recipes should be visible.
No error messages should be displayed.

### TC-004 - Navbar links navigate correctly when logged out

**Preconditions:**  
User is not logged in.

**Steps:**  
1. Open the RecipeNest home page.  
2. Click "Recipes" in the navbar.  
3. Observe the page that loads.  
4. Click "Home" in the navbar.  
5. Observe the page that loads.

**Expected Result:**  
Clicking "Recipes" should navigate to the recipes list page.  
Clicking "Home" should navigate to the home page.  
No error messages should be displayed.

### TC-005 - Protected navbar links redirect to login when logged out

**Preconditions:**  
User is not logged in.

**Steps:**  
1. Open the RecipeNest home page.  
2. Click "My Recipes" in the navbar.  
3. Observe the page that loads.  
4. Navigate back to the home page.
5. Click "Add Recipe" in the navbar.
6. Observe the page that loads.

**Expected Result:** 
Clicking "My Recipes" should redirect to the login page.  
Clicking "Add Recipe" should redirect to the login page.  
No error messages should be displayed.

### TC-006 - Login navbar link opens login page when logged out

**Preconditions:**  
User is not logged in.

**Steps:**  
1. Open the RecipeNest home page.  
2. Click "Login" in the navbar.  
3. Observe the page that loads.

**Expected Result:**  
The login page should be displayed.  
No error messages should be shown.

## 2. Registration

This section covers testing related to user registration.

### TC-007 - Successful registration logs user in and redirects

**Preconditions:**
User is not logged in.
The username does not already exist.
The email does not already exist.
The password used meets complexity requirements.

**Steps:**
1. Navigate to Login page.
2. Click the “Register” link under "New here? Register".
3. Enter a unique username.
4. Enter a unique email.
5. Enter a valid password that meets the password requirements.
6. Enter the same password again in "Confirm Password".
7. Click the "Register" button.
8. Observe which page loads.
9. Click "My Recipes" in the navbar.
10. Observe which page loads.
11. Click "Add Recipe" in the navbar.
12. Observe which page loads.

**Expected Result:**
Registration should succeed with no error messages.
User should be redirected to the recipes page.
User should be logged in (navbar should show "Logout").
Clicking "My Recipes" should open the My Recipes page.
Clicking "Add Recipe" should open the Add Recipe page.

### TC-008 - Registration requires all fields

**Preconditions:**
User is not logged in.
User is on the Register Page.

**Steps:**
1. Open the Register page.
2. Leave all input fields blank.
3. Click the "Register" button.
4. Observe any messages shown.

**Expected Result:**
Registration should not submit.
The message "All fields are required." should be displayed.
User should remain on the register page.
User should not be logged in (navbar should still show "Login").

### TC-009 - Registration requires password complexity

**Preconditions:**
User is not logged in.
User is on the Register Page.
Username and email used are unique.

**Steps:**
1. Open the Register page.
2. Enter a unique username.
3. Enter a unique email.
4. Enter an invalid password (example: abc123).
5. Enter the same invalid password in Confirm Password.
6. Click "Register".
7. Observe the message shown under the input fields.

**Expected Result:**
Registration should not submit.
The message "Password must be at least 8 characters long and include uppercase, lowercase, a number, and a special character." should be displayed.
User remains on Register page.
User is not logged in (navbar still shows "Login").

### TC-010 - Registration requires matching passwords

**Preconditions:**
User is not logged in.
User is on the Register page.
Username and email used are unique.

**Steps:**
1. Open the Register page.
2. Enter a unique username.
3. Enter a unique email.
4. Enter a valid password that meets the password requirements.
5. Enter a different password in "Confirm Password".
6. Click the "Register" button.
7. Observe the message shown under the input fields.

**Expected Result:**
Registration should not submit.
The message "Passwords do not match." should be displayed.
User remains on Register page.
User is not logged in (navbar still shows "Login").

### TC-011 - Registration requires unique username

**Preconditions:**
User is not logged in.
User is on the Register page.
An account already exists with a known username.

**Steps:**
1. Open the Register page.
2. Enter a username that is already registered.
3. Enter a unique email address.
4. Enter a valid password that meets the password requirements.
5. Enter the same password again in "Confirm Password".
6. Click the "Register" button.
7. Observe the message shown under the input fields.

**Expected Result:**
Registration should not submit.
The message "Username already taken" should be displayed.
User remains on Register page.
User is not logged in (navbar still shows "Login").

### TC-012 - Registration requires unique email address

**Preconditions:**
User is not logged in.
User is on the Register page.
An account already exists with a known email address.

**Steps:**
1. Open the Register page.
2. Enter a unique username.
3. Enter an email address that is already registered.
4. Enter a valid password that meets the password requirements.
5. Enter the same password again in "Confirm Password".
6. Click the "Register" button.
7. Observe the message shown under the input fields.

**Expected Result:**
Registration should not submit.
The message "Email already registered" should be displayed.
User remains on Register page.
User is not logged in (navbar still shows "Login").

### TC-013 - Registration requires valid email format

**Preconditions:**
User is not logged in.
User is on the Register page.

**Steps:**
1. Open the Register page.
2. Enter an invalid email address (example: test).
3. Click the "Register" button.
4. Observe what happens.

**Expected Result:**
The form should not submit.
A browser validation message should appear indicating the email address is invalid.
User remains on Register page.
User is not logged in (navbar still shows "Login").

### TC-014 - Register page login link navigates correctly

**Preconditions:**
User is not logged in.
User is on the Register page.

**Steps:**
1. Open the Register page.
2. Click the word "Login" in the text "Already have an account? Login".
3. Observe which page loads.

**Expected Result:**
The Login page should be displayed.
No error messages should be shown.

### TC-015 - Password field does not display plain text

**Preconditions:**
User is not logged in.
User is on the Register page.

**Steps:**
1. Open the Register page.
2. Click inside the "Password" field.
3. Enter a sample password.
4. Observe how the characters are displayed.
5. Click inside the "Confirm Password" field.
6. Enter a sample password.
7. Observe how the characters are displayed.

**Expected Result:**
Characters entered into both the Password field and the Confirm Password field should not be visible as plain text.

## 3. Login

This section covers testing related to user login.

### TC-016 - Successful login redirects to My Recipes

**Preconditions:**
User is logged out.
A valid account exists.

**Steps:**
1. Open the Login page.
2. Enter a registered email address.
3. Enter the correct password.
4. Click the "Login" button.
5. Observe which page loads.
6. Observe the navbar.

**Expected Result:**
Login should succeed with no error messages.
User should be redirected to the My Recipes page.
User should be logged in (navbar should show "Logout").

### TC-017 - Login requires email and password

**Preconditions:**
User is logged out.
User is on the Login page.

**Steps:**
1. Open the Login page.
2. Leave the Email and Password fields blank.
3. Click the "Login" button.
4. Observe the message shown under the Login button.
5. Enter any email address and leave Password blank.
6. Click the "Login" button.
7. Observe the message shown.
8. Enter any password and leave Email blank.
9. Click the "Login" button.
10. Observe the message shown.

**Expected Result:**
Login should not submit.
The message "Email and password are required" should be displayed each time.
User should remain on the Login page.
User should not be logged in (navbar should still show "Login").

### TC-018 - Login fails with invalid credentials

**Preconditions:**
User is logged out.
User is on the Login page.
At least one valid account exists in the system.

**Steps:**
1. Open the Login page.
2. Enter a registered email address.
3. Enter an incorrect password.
4. Click the "Login" button.
5. Observe the message shown under the Login button.
6. Enter an unregistered email address.
7. Enter any password.
8. Click the "Login" button.
9. Observe the message shown.

**Expected Result:**
Login should not submit.
The message "Invalid email or password" should be displayed.
User should remain on the Login page.
User should not be logged in (navbar should still show "Login").

### TC-019 - Login requires valid email format

**Preconditions:**
User is logged out.
User is on the Login page.

**Steps:**
1. Open the Login page.
2. Enter an invalid email address (example: test).
3. Enter any password.
4. Click the "Login" button.
5. Observe what happens.

**Expected Result:**
The form should not submit.
A browser validation message should appear indicating the email address is invalid.
User should remain on the Login page.
User should not be logged in (navbar should still show "Login").

## 4. Search

This section covers testing related to searching recipes.

### TC-020 - Search redirects to Recipes page when typing from Home page

**Preconditions:**
User is on the Home page.

**Steps:**
1. Click inside the search input field in the navbar.
2. Type any text.
3. Observe which page is displayed.

**Expected Result:**
The user should be redirected to the Recipes page automatically when typing in the search field.
No error messages should be displayed.

### TC-021 - Search filters recipe titles as user types on Recipes page

**Preconditions:**
User is on the Recipes page.
At least two recipes exist with different titles.

**Steps:**
1. Click inside the search input field in the navbar.
2. Type text that matches part of an existing recipe title.
3. Observe the recipes shown.
4. Continue typing additional letters to narrow the results.
5. Change the case of the text entered (uppercase/lowercase).
6. Observe the recipes shown.

**Expected Result:**
The recipe list should filter automatically as the user types.
Only recipes with titles containing the entered text should be displayed.
Partial matches should be returned.
Search should not be case sensitive.
No error messages should be displayed.

## 5. Logged-In Features

This section covers functionality available only to authenticated users, which includes adding, viewing, editing and deleting recipes.
