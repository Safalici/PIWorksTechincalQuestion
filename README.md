# PIWorksTechincalQuestion
This srepository created to solve the 5th question of Technical Question for  Product Design Intern (Telecom Software)

# User Management Screen UI Specification

## Overview
This document provides the detailed specifications for the User Management Screen, detailing the components, behaviors, and requirements.

## UI Components

### Main Table
- **Columns:**
  - `ID`: Displays the unique identifier for each user.
  - `User Name`: Displays the username of the user.
  - `Email`: Displays the email address associated with the user.
  - `Enabled`: Displays a boolean (true/false) value indicating if the user account is active.
- **Features:**
  - Sortable columns: Clicking on the column headers will sort the table based on that column's data.
  - Hover effect: Hovering over a row should provide a visual indication, aiding in readability.

### Buttons
- `+ New User`: Clicking this button will open the "New User" form on the right, allowing the addition of a new user.
- `Hide Disabled User`: Toggles the display of users who are disabled (where `Enabled` is `false`).
- `Save User`: Saves the details entered in the "New User" form.

### New User Form
- **Fields:**
  - `Username`: Text input for the user's login name. It's mandatory.
  - `Display Name`: Text input for the full name or alias of the user. It's mandatory.
  - `Phone`: Text input for the user's contact number.
  - `Email`: Text input for the user's email address. It's mandatory.
  - `User Roles`: A dropdown selection allowing for multiple roles (like Admin, Guest, SuperAdmin) to be assigned to the user.
  - `Enabled`: A checkbox that determines if the user is active or not. By default, it should be checked (true).
- **Behavior:**
  - If any mandatory fields are left empty when the `Save User` button is clicked, display an error prompt.
  - Upon successful save, add the new user details to the main table and clear the form.

## Initial Behavior
- On initial load, the main table should display all users, including both enabled and disabled ones.
- The "New User" form should be cleared/reset.

## Guidelines for Developers
- Ensure that all components are responsive and adapt to different screen sizes.
- Implement appropriate error handling for server-side operations and provide user feedback.
- Ensure proper validation of email and phone number fields.
- Before saving, confirm that the username and email aren't already used.
