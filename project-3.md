# Project 3

This application will test your basic knowledge of React as our main frontend stack. The application must run in client-side only, no server-side application required to run the app.

Instructions:

## Release 1

Create a register page that contains a form for users to register which includes following fields: each field present is worth 5 points
- Company to Apply - Dropdown with 4 options populated from React-Redux: "Brewed Delight", "Noah's Coffee", "Royal Coffee", or "Cup of Magic".

- Position to Apply - Five checkboxes for our Software Engineer position, consisted of "Backend Developer", "Frontend Developer", "Quality Assurance", "Devops", and "Check All".

- Full Name - One input field

- Phone Number with +62 prefix - One input field, but the prefix must be OUTSIDE the input field.

- Password and Confirm password field with toggle button to show/hide the input - Two input fields, with toggle button at the end of the field.


## Release 2

Validate the register form upon **user input** NOT **form submission**, the validation must be displayed on each field with following restrictions: Each validator is worth 10 points:

- Company to Apply - Must be selected to proceed, your code will be checked to determine whether or not the data uses React-Redux to populate.

- Position to Apply - Must be checked to proceed, you can check multiple items, but the Check All checkbox must override all checkboxes.

- Full Name - Must be a text with a minimum of 3 characters and a maximum of 2 words representing First Name and Last Name inside one field, allows numbers but cannot contain symbols

- Phone Number - Must be a mobile number with minimum of 11 digits (excluding +62), but should include the prefix upon submitting.

- Password and Confirm Password - A string with no restrictions, but must be a match to proceed. Cannot be empty!
    
## Plus Points

- Write your own cascading stylesheet to design the page: 10 points

- Create a user list page that display registered user with React-Redux: 10 points

- Write a thorough documentation: 5 points