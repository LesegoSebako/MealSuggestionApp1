# MealSuggestionApp1
Introduction to Mobile Application Development - Assignment 1

MODULE CODE - IMAD 5112
STUDENT NAME - LESEGO SEBAKO
STUDENT NUMBER - ST 10493865


https://github.com/LesegoSebako/MealSuggestionApp1

Youtube link - https://youtu.be/n3JaVpIUujM

PDF Link - https://github.com/LesegoSebako/MealSuggestionApp1/blob/main/Lesego%20Sebako%20-%20IMAD5112%20-%20ASSIGNEMENT%201.pdf

Technical Report: Meal Suggestion App

**1. Introduction**
This report explains the Meal Suggestion App, an Android application built usingKotlin in Android Studio. The app helps users decide what to eat based on the time
of day.
Key Features Learned
Basic Android UI design (TextViews, Buttons, EditText)Coroutines for background tasks
Toast messages for error handlingColor schemes for better UI
Click listeners for user interaction

2. App Features
User Interface (UI) Components,Component & Purpose

EditText (etTimeOfDay) - User types in time of day (e.g., "Morning")
Button (btnGetSuggestion) - Triggers meal suggestion
Button (btnReset) - Erases input and suggestionTextView (tvSuggestion) Displays the meal suggestion

Color Scheme
ElementColor CodePurpose
Background - #F5F5F5 (Light Gray) - Clean, neutral look
Get Suggestion Button - #4CAF50 (Green) - Positive actionReset Button - #F44336 (Red) - Warning/clear action
Text Color - #333333 (Dark Gray) - Readable text

**3. Key Methods & Classes Used**
MainActivity.kt
This is the main class controlling the app.
Methods Used:
onCreate() Runs when the app starts.Sets up the layout (activity_main.xml).
Calls initializeViews(), setupUI(), and setupClickListeners().
initializeViews()Connects UI elements (EditText, Button, TextView) to Kotlin code.
setupUI()Sets background color (#F5F5F5).Styles buttons (green for "Get Suggestion," red for "Reset").
Hides the suggestion TextView initially.

**setupClickListeners() btnGetSuggestion → Calls getMealSuggestion().
btnReset → Calls resetFields().
getMealSuggestion()Uses coroutines (lifecycleScope.launch) to run in the background.Checks user input and shows a Toast error if empty.
Uses when to match time of day with meal suggestions.
resetFields()Clears the EditText and TextView.

**4. Error Handling in the App**
Empty Input Check
When the user clicks "Get Meal Suggestion" without typing anything:
Invalid If the user types something unexpected (like "Nighttime"): Input Handling
Displays a friendly suggestion about valid inputs
Manual Testing
Empty input - Click button - Shows Toast error
"Morning" → Click button - Suggests oatmeal
"dinner" (lowercase) - Click button - Suggests salmon
"Midday" (invalid) - Click button - Shows valid options
Reset button - Clears all fields

**5. GitHub Actions Automated Testing**
Added basic workflow to catch build errors:
Automatically runs when code is pushedChecks if the project compiles successfully
Verifies no syntax errors in Kotlin/XML files

**6. GitHub Actions/Workflow.**

Below are steps I undertook to create a Github repository, locally and online, as
well creating and running workflow.

**7. Set Up Git Desktop & Repository**

    Online GitHub Setup
    Created a GitHub Actions Workflow
    Pushing/Pulling Changes
    Running & Monitoring Workflow**

Key Concepts Learned

Actions & Purpose
Workflow - Automates process that builds/test the app
YAML File- format for configuring workflows
Push - Uploads local changes to GitHub
Pull - Downloads team members' changes
