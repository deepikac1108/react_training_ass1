# react_training_ass1

HTML Signup Page

This repository contains the code for a responsive signup page designed using HTML5 and CSS3. The signup page includes various input fields and a checkbox, with a focus effect that gives the input fields a blue shadow when selected.

Project Structure

The project consists of two main files:

	•	index.html
	•	styles.css

index.html

This file contains the HTML structure for the signup page. It includes a form with fields for first name, last name, mobile number, email address, password, and confirm password, as well as a checkbox for agreeing to terms and conditions.

Key Sections:

	•	Form: Contains input fields for user data.
	•	Footer: Displays company contact information.

styles.css

This file contains the CSS styles used to design the signup page. It includes styles for layout, form elements, buttons, and focus effects.

Key Styles:

	•	Container: Centers the form on the page and adds styling such as background color, border radius, and box shadow.
	•	Form Elements: Styles the input fields, buttons, and labels, including a custom focus effect with a blue shadow.
	•	Buttons: Styles for the register and sign-in buttons, including color and hover effects.
	•	Footer: Styles for the footer content and links.

Features

	•	Responsive Design: The signup page is designed to be responsive and adjustable to all screen sizes.
	•	Custom Focus Effect: When an input field is focused, it displays a blue shadow around the field.
	•	Proper Nesting: HTML tags are nested properly, adhering to HTML5 standards.
	•	No Inline Styles: All styles are defined in the external styles.css file.

How to Use

	1.	Clone the repository to your local machine:
       git clone https://github.com/yourusername/html-signup-page.git
  2.	Navigate to the project directory:
       cd html-signup-page
  3.	Open the index.html file in your browser to view the signup page.

Code Snippets

index.html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Signup Page</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div class="container">
        <form class="signup-form">
            <h2>Sign Up</h2>
            <div class="form-group row">
                <input type="text" id="firstName" name="firstName" placeholder="First Name" required>
                <input type="text" id="lastName" name="lastName" placeholder="Last Name" required>
            </div>
            <div class="form-group">
                <input type="tel" id="mobile" name="mobile" placeholder="Mobile No." required>
            </div>
            <div class="form-group">
                <input type="email" id="email" name="email" placeholder="Email Address" required>
            </div>
            <div class="form-group row">
                <input type="password" id="password" name="password" placeholder="Password" required>
                <input type="password" id="confirmPassword" name="confirmPassword" placeholder="Confirm Password" required>
            </div>
            <div class="form-group">
                <label for="agree">
                    <input type="checkbox" id="agree" name="agree" required>
                    I Agree
                </label>
                <p>By clicking <strong>Register</strong>, you agree to the <a href="#">Terms and Conditions</a> set out by this site, including our <a href="#">Cookie Use</a>.</p>
            </div>
            <div class="form-buttons">
                <button type="submit" class="register-btn">Register</button>
                <button type="button" class="signin-btn">Sign In</button>
            </div>
        </form>
    </div>
    <footer>
        <p>Antra Inc: 21355 Ridgetop Circle Suite 300 Dulles VA 20166</p>
        <p>Phone: 703.994.4545 Fax: 703.373.2975 e-mail: <a href="mailto:hr@antra.net">hr@antra.net</a> website: <a href="http://www.antra.net">www.antra.net</a></p>
    </footer>
</body>
</html>

styles.css

body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    background-color: #f0f0f0;
}

.container {
    background-color: white;
    border-radius: 8px;
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.1);
    padding: 20px;
    max-width: 600px;
    width: 100%;
    margin: 20px;
}

.signup-form {
    display: flex;
    flex-direction: column;
}

.signup-form h2 {
    text-align: center;
    margin-bottom: 20px;
}

.form-group {
    display: flex;
    flex-direction: column;
    margin-bottom: 15px;
}

.form-group.row {
    flex-direction: row;
    gap: 10px;
}

.form-group input[type="text"],
.form-group input[type="tel"],
.form-group input[type="email"],
.form-group input[type="password"] {
    padding: 10px;
    margin: 5px 0;
    border: 1px solid #ccc;
    border-radius: 4px;
    width: 100%;
    transition: box-shadow 0.3s ease-in-out;
}

.form-group input[type="text"]:focus,
.form-group input[type="tel"]:focus,
.form-group input[type="email"]:focus,
.form-group input[type="password"]:focus {
    outline: none;
    box-shadow: 0 0 5px rgba(0, 123, 255, 0.5);
}

.form-group input[type="checkbox"] {
    margin-right: 10px;
}

label {
    font-weight: bolder;
}

strong {
    padding: 2px 3px;
    border: none;
    border-radius: 4px;
    background-color: #007bff;
    color: white;
}
.form-buttons {
    display: flex;
    justify-content: space-between;
}

button {
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
}

.register-btn {
    background-color: #007bff;
    color: white;
}

.signin-btn {
    background-color: #28a745;
    color: white;
}

footer {
    text-align: center;
    margin-top: 20px;
}

footer a {
    color: #007bff;
    text-decoration: none;
}

footer a:hover {
    text-decoration: underline;
}

