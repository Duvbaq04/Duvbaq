<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cut It Barbershop</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>

    <!-- Header Section -->
    <header>
        <h1>Welcome to Cut It Barbershop</h1>
        <p>We handle all kinds of haircuts!</p>
        <a href="#booking" class="button">Book an Appointment</a>
    </header>

    <!-- About Section -->
    <section id="about">
        <h2>About Us</h2>
        <p>Cut It Barbershop provides top-notch haircuts for everyone. Come as you are, and leave with a fresh look! Open daily from 11:00 AM to 08:00 PM.</p>
    </section>

    <!-- Services Section -->
    <section id="services">
        <h2>Our Services</h2>
        <p>Haircut - 250kr (1-hour session)</p>
    </section>

    <!-- Booking Section -->
    <section id="booking">
        <h2>Book an Appointment</h2>
        <form id="bookingForm">
            <label for="name">Name:</label>
            <input type="text" id="name" required>

            <label for="email">Email:</label>
            <input type="email" id="email" required>

            <label for="date">Date:</label>
            <input type="date" id="date" required>

            <label for="time">Time:</label>
            <input type="time" id="time" required>

            <label for="message">Desired Haircut:</label>
            <textarea id="message" rows="4" placeholder="Describe your desired haircut here..." required></textarea>

            <button type="submit">Send Booking Request</button>
        </form>
    </section>

    <!-- Footer Section -->
    <footer>
        <p>&copy; 2023 Cut It Barbershop</p>
    </footer>

    <script src="script.js"></script>
</body>
</html>* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    font-family: Arial, sans-serif;
}

body {
    background-color: #f4f4f9;
    color: #333;
}

header {
    background-color: #333;
    color: #fff;
    padding: 20px;
    text-align: center;
}

h1 {
    margin-bottom: 10px;
}

.button {
    display: inline-block;
    margin-top: 10px;
    padding: 10px 20px;
    color: #333;
    background-color: #fff;
    text-decoration: none;
}

section {
    margin: 20px;
    padding: 20px;
    background-color: #fff;
    border-radius: 8px;
}

form label {
    display: block;
    margin-top: 10px;
}

form input, form textarea, form button {
    width: 100%;
    padding: 10px;
    margin-top: 5px;
}

footer {
    text-align: center;
    padding: 10px;
    background-color: #333;
    color: #fff;
}document.getElementById("bookingForm").addEventListener("submit", function(event) {
    event.preventDefault();
    
    const name = document.getElementById("name").value;
    const email = document.getElementById("email").value;
    const date = document.getElementById("date").value;
    const time = document.getElementById("time").value;
    const message = document.getElementById("message").value;

    console.log("Booking Request:");
    console.log("Name:", name);
    console.log("Email:", email);
    console.log("Date:", date);
    console.log("Time:", time);
    console.log("Desired Haircut:", message);

    alert("Thank you for booking! We’ll confirm your appointment soon.");
    
    // Optional: integrate email API here for real emails
});
