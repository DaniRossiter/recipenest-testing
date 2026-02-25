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

## 2. Registration

This section covers testing related to user registration.

## 3. Login

This section covers testing related to user login.

## 4. Search

This section covers testing of recipe search functionality

## 5. Logged-In Features

This section covers functionality available only to authenticated users, which includes adding, viewing, editing and deleting recipes.
