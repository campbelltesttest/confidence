<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>DeskConfidence</title>
<!-- Linking to Google Fonts for modern typography -->
<link href="https://fonts.googleapis.com/css2?family=Poppins:wght@400;700&display=swap" rel="stylesheet">
<style>
  body {
    font-family: 'Poppins', sans-serif;
    background-color: #f4f4f4;
    margin: 0;
    padding: 0;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
  }
  form {
    background-color: #f0ffff; /* Turquoise color */
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    max-width: 90%; /* Adjusted for better fit on mobile */
    width: 100%;
    text-align: center; /* Centering content */
  }
  h1 {
    margin-bottom: 20px; /* Added spacing below the title */
  }
  label {
    font-weight: bold;
    text-align: left; /* Aligning question labels to the left */
    display: block; /* Ensuring each label takes a full line */
  }
  input[type="text"] {
    width: 100%;
    padding: 8px;
    margin-top: 5px;
    margin-bottom: 10px;
    border: 1px solid #ccc;
    border-radius: 4px;
    box-sizing: border-box;
    font-size: 16px;
  }
  button {
    background-color: #00ced1; /* Turquoise color */
    color: white;
    padding: 10px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer;
    font-size: 16px;
    margin-top: 20px; /* Added margin to the top of the button */
  }
  button:hover {
    background-color: #20b2aa; /* Darker shade of turquoise on hover */
  }
  .message {
    color: green;
    font-size: 14px;
    margin-top: 5px;
  }
</style>
<script src="https://cdnjs.cloudflare.com/ajax/libs/jspdf/2.4.0/jspdf.umd.min.js"></script>
</head>
<body>

<form id="questionnaireForm">
  <h1>DeskConfidence</h1>
  
  <label for="question1">1. What are you most proud about yourself?</label><br>
  <input type="text" id="question1" name="question1"><br>
  <span class="message" id="message1"></span><br>

  <label for="question2">2. When did you feel the most proud of yourself?</label><br>
  <input type="text" id="question2" name="question2"><br>
  <span class="message" id="message2"></span><br>

  <label for="question3">3. What are 3 things you love doing?</label><br>
  <input type="text" id="question3" name="question3"><br>
  <span class="message" id="message3"></span><br>

  <label for="question4">4. Who do you admire most?</label><br>
  <input type="text" id="question4" name="question4"><br>
  <span class="message" id="message4"></span><br>

  <label for="question5">5. What do they do?</label><br>
  <input type="text" id="question5" name="question5"><br>
  <span class="message" id="message5"></span><br>

  <button type="button" onclick="generatePDF()">Generate PDF</button>
</form>

<script>
function generatePDF() {
  const doc = new jsPDF();
  const answers = [];
  
  // Get answers from form
  answers.push(document.getElementById('question1').value);
  answers.push(document.getElementById('question2').value);
  answers.push(document.getElementById('question3').value);
  answers.push(document.getElementById('question4').value);
  answers.push(document.getElementById('question5').value);
  
  // Generate PDF
  let yPos = 10;
  for (let i = 0; i < answers.length; i++) {
    doc.text(10, yPos, "Question " + (i + 1) + ": " + answers[i]);
    yPos += 10;
  }
  
  // Save PDF
  doc.save('answers.pdf');
}

// Function to display "Great Work" message when a question is filled
function displayMessage(questionNumber) {
  const messageElement = document.getElementById('message' + questionNumber);
  if (messageElement) {
    messageElement.textContent = "Great Work";
  }
}

// Event listeners to call displayMessage function when input field changes
document.getElementById('question1').addEventListener('input', function() {
  displayMessage(1);
});
document.getElementById('question2').addEventListener('input', function() {
  displayMessage(2);
});
document.getElementById('question3').addEventListener('input', function() {
  displayMessage(3);
});
document.getElementById('question4').addEventListener('input', function() {
  displayMessage(4);
});
document.getElementById('question5').addEventListener('input', function() {
  displayMessage(5);
});
</script>

</body>
</html>
