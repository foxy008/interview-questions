# Project 3

This application will test your basic knowledge of React as our main frontend stack. The application must run in client-side only, no server-side application required to run the app.

Instructions:

## Release 1
1. Create a register page that contains a form for users to register which includes following fields: each field present is worth 5 points
    1. Company to Apply - Dropdown with 4 options populated from React-Redux: "Brewed Delight", "Noah's Coffee", "Royal Coffee", or "Cup of Magic".
    2. Position to Apply - Five checkboxes for our Software Engineer position, consisted of "Backend Developer", "Frontend Developer", "Quality Assurance", "Devops", and "Check All".
    3. Full Name - One input field
    4. Phone Number with +62 prefix - One input field, but the prefix must be OUTSIDE the input field.
    5. Password and Confirm password field with toggle button to show/hide the input - Two input fields, with toggle button at the end of the field.
    
2. Validate the register form upon **user input** NOT **form submission**, the validation must be displayed on each field with following restrictions: Each validator is worth 10 points
    1. Company to Apply - Must be selected to proceed, your code will be checked to determine whether or not the data uses React-Redux to populate.
    2. Position to Apply - Must be checked to proceed, you can check multiple items, but the Check All checkbox must override all checkboxes.
    3. Full Name - Must be a text with a minimum of 3 characters and a maximum of 2 words representing First Name and Last Name inside one field, allows numbers but cannot contain symbols
    4. Phone Number - Must be a mobile number with minimum of 11 digits (excluding +62), but should include the prefix upon submitting.
    5. Password and Confirm Password - A string with no restrictions, but must be a match to proceed. Cannot be empty!
    
3. Plus Points
    1. Write your own cascading stylesheet to design the page: 10 points
    2. Create a user list page that display registered user with React-Redux: 10 points
    3. Write a thorough documentation: 5 points