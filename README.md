<!DOCTYPE html>
<html>
<head>
    <title>Enter Your Name</title>
    <script>
        function submitForm() {
            var name = document.getElementById("name").value;
            if(name) {
                // Show the image and a welcome message
                document.getElementById("welcome").innerHTML = "Thank you, " + name + "!";
                document.getElementById("image").style.display = "block";
                // Redirect after a delay
                setTimeout(function() {
                    window.location.href = "https://yourwebsite.com"; // Redirect to the actual page
                }, 3000); // 3 seconds delay
            } else {
                alert("Please enter your name!");
            }
        }
    </script>
    <style>
        #image {
            display: none; /* Hide the image initially */
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h2>Welcome! Please enter your name to continue</h2>
    <input type="text" id="name" placeholder="Enter your name" required>
    <button onclick="submitForm()">Submit</button>
    <div id="welcome"></div>
    <img id="image" src="your-image-url.jpg" alt="Welcome Image" width="300"> <!-- Adjust width as needed -->
</body>
</html>
