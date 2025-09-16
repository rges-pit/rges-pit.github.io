---
permalink: /submit/
title: "Submit"
description: "Submit website content, report issues, or send feedback to RGES-PIT."
---

Please use the following form to:

* Submit content for the website (**RGES PIT Membership Required**)
* Report an issue or bug
&nbsp;  
&nbsp;  

<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
</head>
<body>
    <form action="https://formspree.io/f/mgvvroeg" method="POST">
        <!-- Email Field -->
        <label for="subject">Email (optional):</label><br>
        <input type="text" id="email" name="email"><br><br>
        <!-- Subject Field -->
        <label for="subject">Subject (required):</label><br>
        <input type="text" id="subject" name="subject" required><br><br>
        
        <!-- Body Field -->
        <label for="body">Comment (required):</label><br>
        <textarea id="body" name="body" rows="10" cols="50" required></textarea><br><br>
        
        <!-- Attachment Field -->
        <label for="attachment">Attachment (optional):</label><br>
        <input type="file" id="attachment" name="attachment"><br><br>
        
        <!-- Submit Button -->
        <button type="submit">Submit</button>
    </form>
</body>

