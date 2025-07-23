# student-data-entry-from<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Student Data Entry</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="container">
        <h1>Student Data Entry Form</h1>
        <form id="studentForm">
            <label for="studentName">Student Name:</label>
            <input type="text" id="studentName" name="studentName" required>

            <label for="studentId">Student ID:</label>
            <input type="text" id="studentId" name="studentId" required>

            <label for="studentClass">Class:</label>
            <input type="text" id="studentClass" name="studentClass" required>

            <label for="dob">Date of Birth:</label>
            <input type="date" id="dob" name="dob" required>

            <label for="email">Email:</label>
            <input type="email" id="email" name="email" required>

            <button type="submit">Submit</button>
        </form>

        <div id="output"></div>
    </div>

    <script>
        const form = document.getElementById('studentForm');
        const output = document.getElementById('output');

        form.addEventListener('submit', function(event) {
            event.preventDefault();
            const name = document.getElementById('studentName').value;
            const id = document.getElementById('studentId').value;
            const studentClass = document.getElementById('studentClass').value;
            const dob = document.getElementById('dob').value;
            const email = document.getElementById('email').value;

            output.innerHTML = `
                <h2>Submitted Student Info:</h2>
                <p><strong>Name:</strong> ${name}</p>
                <p><strong>ID:</strong> ${id}</p>
                <p><strong>Class:</strong> ${studentClass}</p>
                <p><strong>Date of Birth:</strong> ${dob}</p>
                <p><strong>Email:</strong> ${email}</p>
            `;
        });
    </script>
</body>
</html>
