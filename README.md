# ProVibeStudio
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ProVibe Studio</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <div id="root"></div>
    <script src="app.js"></script>
</body>
</html>
body {
    font-family: Arial, sans-serif;
    margin: 0;
    padding: 0;
}

header {
    background-color: #333;
    color: #fff;
    padding: 1rem;
    text-align: center;
}

nav a {
    color: #fff;
    margin: 0 15px;
    text-decoration: none;
}

main {
    padding: 1rem;
}

form {
    display: flex;
    flex-direction: column;
}

input⬤
document.getElementById('profileForm').addEventListener('submit', function(event) {
    event.preventDefault();
    const name = document.getElementById('name').value;
    const industry = document.getElementById('industry').value;

    fetch('https://your-backend-url.glitch.me/profile', {
        method: 'POST',
        headers: { 'Content-Type': 'application/json' },
        body: JSON.stringify({ name, industry })
    })
    .then(response => response.json())
    .then(data => alert(data.message));
});