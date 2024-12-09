### Assignment: Building a Multimedia Webpage and a Registration Form  

#### Objective: 
The goal of this assignment is to create a multimedia-rich webpage featuring audio and video elements and design a simple registration form with built-in HTML validation.  

---

### Part 1: Multimedia Webpage 
Create an HTML webpage that includes the following:  
1. **Audio Element**:  
   - Add an audio file using the `<audio>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Use at least one source format (e.g., `.mp3` or `.ogg`).  

2. **Video Element**:  
   - Add a video file using the `<video>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Include at least two source formats for compatibility (e.g., `.mp4` and `.webm`).  
   - Add a poster image that displays before the video plays.  

**Example Output:**  
A webpage where users can play an audio track and watch a video.  

---

### **Part 2: Registration Form **  
Design a user registration form with the following requirements:  

1. **Form Elements**:  
   - Full Name (Text input)  
   - Email Address (Input of type `email`)  
   - Password (Input of type `password`)  
   - Age (Input of type `number`, with a minimum value of 18)  
   - Gender (Radio buttons for Male, Female, Other)  
   - Terms and Conditions (Checkbox to agree before submitting)  

2. **Validation**:  
   - Use HTML5 validation attributes such as `required`, `min`, `maxlength`, etc.  
   - Ensure the email field has proper validation for email format.  
   - Make the password field require at least 8 characters.  

3. **Submit Button**:  
   - Include a "Register" button to submit the form.  

**Example Output:**  
A user-friendly registration form that prevents submission if required fields are not filled correctly.  

---



my answers 



<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multimedia Webpage with Registration Form</title>
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>Welcome to My Multimedia Webpage</h1>
    </header>

    <!-- Audio Section -->
    <section>
        <h2>Audio Player</h2>
        <p>Click the play button to listen to the audio track.</p>
        <audio controls>
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
            <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.ogg" type="audio/ogg">
            Your browser does not support the audio element.
        </audio>
    </section>

    <!-- Video Section -->
    <section>
        <h2>Video Player</h2>
        <p>Click the play button to watch the video.</p>
        <video controls poster="https://www.w3schools.com/html/movie.jpg">
            <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
            <source src="https://www.w3schools.com/html/mov_bbb.webm" type="video/webm">
            Your browser does not support the video element.
        </video>
    </section>

    <!-- Registration Form Section -->
    <section>
        <h2>Registration Form</h2>
        <form action="#" method="POST">
            <!-- Full Name -->
            <label for="fullname">Full Name:</label>
            <input type="text" id="fullname" name="fullname" required maxlength="50" placeholder="Enter your full name"><br><br>

            <!-- Email Address -->
            <label for="email">Email Address:</label>
            <input type="email" id="email" name="email" required placeholder="Enter your email"><br><br>

            <!-- Password -->
            <label for="password">Password:</label>
            <input type="password" id="password" name="password" required minlength="8" placeholder="Enter your password"><br><br>

            <!-- Age -->
            <label for="age">Age (18+):</label>
            <input type="number" id="age" name="age" required min="18" placeholder="Enter your age"><br><br>

            <!-- Gender -->
            <label>Gender:</label><br>
            <input type="radio" id="male" name="gender" value="male" required>
            <label for="male">Male</label><br>
            <input type="radio" id="female" name="gender" value="female">
            <label for="female">Female</label><br>
            <input type="radio" id="other" name="gender" value="other">
            <label for="other">Other</label><br><br>

            <!-- Terms and Conditions -->
            <label for="terms">
                <input type="checkbox" id="terms" name="terms" required> I agree to the terms and conditions.
            </label><br><br>

            <!-- Submit Button -->
            <input type="submit" value="Register">
        </form>
    </section>

</body>
</html>
