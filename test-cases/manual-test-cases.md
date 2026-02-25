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

## 2. Registration

This section covers testing related to user registration.

## 3. Login

This section covers testing related to user login.

## 4. Search

This section covers testing of recipe search functionality

## 5. Logged-In Features

This section covers functionality available only to authenticated users, which includes adding, viewing, editing and deleting recipes.
