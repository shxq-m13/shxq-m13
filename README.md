<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>User Input Form</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 20px;
    }
    form {
      max-width: 400px;
      margin: auto;
      padding: 20px;
      border: 1px solid #ccc;
      border-radius: 10px;
      background-color: #f9f9f9;
    }
    label {
      font-weight: bold;
    }
    input, textarea, button {
      width: 100%;
      padding: 10px;
      margin: 10px 0;
      border: 1px solid #ccc;
      border-radius: 5px;
    }
    button {
      background-color: #007bff;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }
    button:hover {
      background-color: #0056b3;
    }
  </style>
</head>
<body>
  <h1>User Input Form</h1>
  <form id="userInputForm">
    <label for="name">Full Name:</label>
    <input type="text" id="name" name="name" placeholder="Enter your full name" required>
    
    <label for="email">Email Address:</label>
    <input type="email" id="email" name="email" placeholder="Enter your email address" required>
    
    <label for="message">Message:</label>
    <textarea id="message" name="message" placeholder="Type your message here..." rows="5" required></textarea>
    
    <button type="submit">Submit</button>
  </form>
  <script>
    document.getElementById('userInputForm').addEventListener('submit', function (event) {
      event.preventDefault(); // Prevent page refresh

      const name = document.getElementById('name').value;
      const email = document.getElementById('email').value;
      const message = document.getElementById('message').value;

      console.log('Name:', name);
      console.log('Email:', email);
      console.log('Message:', message);

      alert('Form submitted successfully!');
    });
  </script>
</body>
</html>
