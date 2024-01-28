<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Data Entry</title>
</head>
<body>
    <h1>Data Entry</h1>
    <form id="data-form">
        <label for="color">Color:</label>
        <input type="text" id="color" name="color" required><br><br>

        <label for="name">Name:</label>
        <input type="text" id="name" name="name" required><br><br>

        <label for="id">ID:</label>
        <input type="number" id="id" name="id" required><br><br>

        <input type="submit" value="Submit">
    </form>

    <script>
        document.getElementById('data-form').addEventListener('submit', function(event) {
            event.preventDefault();
            const color = document.getElementById('color').value;
            const name = document.getElementById('name').value;
            const id = document.getElementById('id').value;

            if (color === 'q' || name === 'q' || id === 'q') {
                alert('Data entry terminated.');
            } else {
                // You can process the data or send it to the server here
                console.log(`Color: ${color}, Name: ${name}, ID: ${id}`);

                // Clear the form for the next entry
                document.getElementById('color').value = '';
                document.getElementById('name').value = '';
                document.getElementById('id').value = '';
            }
        });
    </script>
</body>
</html>
