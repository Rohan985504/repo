<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Test Submission Feedback</title>
    <style>
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap');
        
        body {
            font-family: 'Poppins', sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background-color: #f5f5f5;
            margin: 0;
        }
        .container {
            background: white;
            padding: 40px;
            border-radius: 12px;
            box-shadow: 0 4px 15px rgba(0, 0, 0, 0.1);
            max-width: 700px;
            width: 90%;
            text-align: center;
        }
        .emoji {
            font-size: 50px;
            margin-bottom: 10px;
        }
        h2 {
            color: #d9534f;
            margin-bottom: 10px;
            font-weight: bold;
            font-size: 22px;
        }
        p {
            color: #555;
            font-size: 14px;
        }
        .buttons {
            display: flex;
            justify-content: center;
            gap: 15px;
            margin-top: 15px;
        }
        .buttons button {
            padding: 12px 25px;
            border: 2px solid #d9534f;
            border-radius: 30px;
            cursor: pointer;
            background: #ffe6e6;
            color: #d9534f;
            font-weight: bold;
            font-size: 14px;
            transition: 0.3s ease;
        }
        .buttons button:hover, .buttons button.active {
            background: #d9534f;
            color: white;
        }
        textarea {
            width: calc(100% - 20px);
            padding: 12px;
            margin-top: 20px;
            border-radius: 8px;
            border: 1px solid #ccc;
            height: 100px;
            resize: none;
            font-size: 14px;
        }
        .submit-btn {
            background: #d9534f;
            color: white;
            padding: 12px 30px;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            margin-top: 20px;
            font-size: 16px;
            font-weight: bold;
            transition: 0.3s ease;
        }
        .submit-btn:hover {
            background: #b52b27;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="emoji">👏</div>
        <h2>Test submitted successfully :)</h2>
        <p>You took <span id="time-taken">7 min</span> to finish the test.</p>
        <p>Please take a moment to submit your feedback.</p>
        
        <h3>How was the interpretation of questions?</h3>
        <div class="buttons">
            <button onclick="selectRating(this)">EXCELLENT</button>
            <button onclick="selectRating(this)">GOOD</button>
            <button onclick="selectRating(this)">AVERAGE</button>
            <button onclick="selectRating(this)">POOR</button>
        </div>
        
        <h3>Any other suggestions or feedback?</h3>
        <textarea placeholder="Enter your feedback here..."></textarea>
        <br>
        <button class="submit-btn" onclick="submitFeedback()">Submit</button>
    </div>

    <script>
        function selectRating(button) {
            document.querySelectorAll('.buttons button').forEach(btn => btn.classList.remove('active'));
            button.classList.add('active');
        }

        function submitFeedback() {
            alert('Thank you for your feedback!');
        }
    </script>
</body>
</html>
