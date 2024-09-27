# Conversion-Tool
![image](https://github.com/user-attachments/assets/bdb40168-9b41-4994-83c8-5f01855e623b)


### Conversion Tool Documentation

This HTML document contains a simple conversion tool that can convert values from Fahrenheit to Celsius and from Meters to Kilometers. The design follows a neumorphism style, giving it a soft, 3D-like appearance with subtle shadow effects.

#### HTML Structure:

- The `<!DOCTYPE html>` declares the document type.
- The `<html>` element is the root element of the document.
- The `<head>` section contains meta information about the document, including:
  - The `<meta charset="UTF-8">` tag specifies the character encoding.
  - The `<meta name="viewport" content="width=device-width, initial-scale=1.0">` tag ensures proper scaling on mobile devices.
  - The `<title>` element defines the title displayed on the browser tab.
  - The `<style>` element contains CSS to define the visual styling of the tool.

#### Body Layout:

The `<body>` tag holds the main content of the page:
- A container `<div class="container">` encloses all elements and provides styling such as padding, background color, and shadow effects to create a neumorphism design.
- Inside the container:
  - `<h1>` for the title "Conversion Tool".
  - `<div class="dropdown">` holds the conversion type selection:
    - `<label for="conversion-type">` provides a label for the dropdown.
    - `<select id="conversion-type">` provides a dropdown menu where the user can select between two conversion options:
      1. Fahrenheit to Celsius (`value="ftoc"`)
      2. Meters to Kilometers (`value="mtokm"`)
  - `<div class="input-section">` holds the input field and conversion button:
    - `<input type="number" id="input-value" placeholder="Enter value">` is used to take user input for the conversion value.
    - `<button id="convert-btn">Convert</button>` is a button to trigger the conversion.
  - `<div class="result">` contains the result display:
    - `<p id="result-output"></p>` shows the converted value or any error message.

#### CSS (Style):

The CSS in the `<style>` block defines the neumorphism design:
- **Body**:
  - The body uses `flex` to center the conversion tool both horizontally and vertically.
  - Background color is a light grey (`#e0e0e0`), and the page uses the Arial font.
- **Container**:
  - A soft shadow effect is applied using `box-shadow` to give the container a raised effect (neumorphism).
  - The container has a light background, rounded corners (`border-radius: 16px`), and padding for space inside.
- **Inputs and Buttons**:
  - The `input` and `select` elements have inset shadows to create a "pressed" appearance, while the button has an outer shadow for a raised look.
  - Buttons change their shadow properties on hover and when clicked (active state) to provide visual feedback to the user.
  
#### JavaScript (Script):

The JavaScript code within the `<script>` tag adds interactivity by performing the actual conversions when the user clicks the "Convert" button.

- **Event Listener**:
  - The code listens for the "click" event on the `Convert` button using `addEventListener`. Once clicked, it retrieves the selected conversion type and input value.
  
- **Conversions**:
  - The selected conversion type is obtained from the dropdown using `document.getElementById('conversion-type').value`.
  - The input value is retrieved from the `input` field and converted to a float with `parseFloat`.
  - The conversion logic:
    - If the selected type is Fahrenheit to Celsius (`ftoc`):
      ```javascript
      result = ((inputValue - 32) * 5 / 9).toFixed(2) + " °C";
      ```
    - If the selected type is Meters to Kilometers (`mtokm`):
      ```javascript
      result = (inputValue / 1000).toFixed(2) + " km";
      ```
  - The result is displayed in the `<p id="result-output"></p>` element.

- **Error Handling**:
  - If the input is not a valid number, the tool displays a message `"Please enter a valid number"`.

### Summary:
This code provides a user-friendly conversion tool with a neumorphism design that allows users to convert values between Fahrenheit and Celsius or Meters and Kilometers. The layout is simple, and JavaScript ensures the correct functionality of the conversions.
