# Dynamic Form Inputs with React

## Overview

This is a simple React application that allows users to add and display their hobbies dynamically. The app provides a form where users can input a hobby, submit it, and then see the list of hobbies displayed below the form. Each hobby in the list has a delete button, allowing the user to remove any hobby from the list.

## Features

- Add hobbies through a form input field.
- Display a list of submitted hobbies.
- Remove individual hobbies from the list using the delete button.

## Technologies Used

- **React**: A JavaScript library for building user interfaces.
- **JavaScript (ES6)**: Modern JavaScript syntax for building the application logic.
- **HTML/CSS**: Used to structure and style the app.
- **Babel**: A JavaScript compiler used to transpile JSX into browser-friendly JavaScript.

## How It Works

1. **Input Form**: Users can enter a hobby in a text field.
2. **Submit Button**: Once a hobby is typed in, clicking the "Submit" button will add the hobby to a list of hobbies. The text input field is then cleared for further entries.
3. **Display List**: The list of hobbies is displayed below the form, showing each hobby as a list item.
4. **Delete Functionality**: Each hobby has a "Delete" button beside it. Clicking this button will remove that specific hobby from the list.

## Components

### `FormInput`

- Responsible for rendering the input field and the submit button.
- Takes the following props:
  - `inputHobby`: A function that updates the current input field value.
  - `submitHobby`: A function that adds the input to the hobbies list.
  - `hobby`: The current value of the hobby input field (controlled input).

### `DisplayHobbies`

- Displays the list of hobbies with a delete button next to each hobby.
- Takes the following props:
  - `hobbies`: An array of the current hobbies.
  - `deleteHobby`: A function that removes a hobby based on its index.

### `App`

- The main component that manages the state of the hobbies and the current input value.
- Implements the logic for adding and deleting hobbies from the list.
- Renders the `FormInput` and `DisplayHobbies` components.

## Code Breakdown

1. **State Management**:
   - `hobbies`: An array to hold the list of hobbies.
   - `hobby`: A string to keep track of the current input value.
2. **Event Handlers**:
   - `inputHobby`: Updates the `hobby` state as the user types in the input field.
   - `submitHobby`: Adds the current value of `hobby` to the `hobbies` array and clears the input field.
   - `deleteHobby`: Removes a hobby from the `hobbies` array based on its index.

## Installation and Usage

1. Clone the repository or copy the code into an HTML file.
2. Open the file in a browser, and the app will render.
3. Start adding hobbies and use the delete functionality as needed.

## Example

### Adding a Hobby:

- Type a hobby in the input field, e.g., "Reading".
- Press "Submit", and "Reading" will appear in the hobby list.

### Deleting a Hobby:

- Click the "Delete" button next to a hobby, and it will be removed from the list.
