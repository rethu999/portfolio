# portfolio
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rethasi's Portfolio</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }
        .container {
            max-width: 800px;
            margin: 2em auto;
            background-color: #fff;
            padding: 2em;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .section {
            display: none;
        }
        .section.active {
            display: block;
        }
        nav {
            display: flex;
            justify-content: space-between;
        }
        nav button {
            padding: 10px 15px;
            border: none;
            background-color: #333;
            color: #fff;
            cursor: pointer;
        }
        nav button.active {
            background-color: #555;
        }
    </style>
</head>
<body>
    <div class="container">
        <nav>
            <button onclick="showSection('skills')" class="active">Skills</button>
            <button onclick="showSection('projects')">Projects</button>
            <button onclick="showSection('contact')">Contact</button>
        </nav>

        <div id="skills" class="section active">
            <h2>Skills</h2>
            <ul>
                <li>HTML & CSS</li>
                <li>JavaScript</li>
                <li>React</li>
                <!-- Add more skills as needed -->
            </ul>
        </div>

        <div id="projects" class="section">
            <h2>Projects</h2>
            <ul>
                <li><a href="#">Project 1</a></li>
                <li><a href="#">Project 2</a></li>
                <!-- Add more projects as needed -->
            </ul>
        </div>

        <div id="contact" class="section">
            <h2>Contact</h2>
            <p>Email: example@example.com</p>
            <p>Phone: +1234567890</p>
        </div>
    </div>

    <script>
        function showSection(id) {
            // Hide all sections
            const sections = document.querySelectorAll('.section');
            sections.forEach(section => {
                section.classList.remove('active');
            });

            // Deactivate all buttons
            const buttons = document.querySelectorAll('nav button');
            buttons.forEach(button => {
                button.classList.remove('active');
            });

            // Show the selected section
            document.getElementById(id).classList.add('active');

            // Activate the clicked button
            const activeButton = Array.from(buttons).find(button => button.innerText.toLowerCase() === id);
            activeButton.classList.add('active');
        }
    </script>
</body>
</html>
