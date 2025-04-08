# Introduction to JavaScript and DOM Manipulation

## Objectives

Write basic JavaScript functions.
Manipulate the DOM dynamically.
Respond to user interactions.

## Instructions

- Create a script.js file and link it to a HTML.
- Structure the document using DOCTYPE, html, head, and body.

>[!NOTE]
>  - Write JavaScript that:
>  - Changes text content dynamically.
>  - Modifies CSS styles via JavaScript.
>  - Adds or removes an element when a button is clicked.


# Tasks
- Create a well-structured HTML5 document.
- Use at least 5 different HTML elements.
- Ensure semantic correctness.

Happy Coding! 💻✨

<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>DOM Manipulation Example</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 0;
            background-color: #f4f4f4;
        }

        header {
            background-color: #333;
            color: white;
            padding: 10px 0;
            text-align: center;
        }

        main {
            padding: 20px;
        }

        button {
            margin-top: 10px;
            padding: 10px;
            font-size: 16px;
            cursor: pointer;
        }

        footer {
            text-align: center;
            padding: 10px 0;
            background-color: #333;
            color: white;
        }
    </style>
</head>
<body>
    <header>
        <h1>DOM Manipulation Example</h1>
    </header>

    <main>
        <section>
            <p id="text">This is some initial text.</p>
            <button id="changeTextBtn">Change Text</button>
        </section>
        
        <section>
            <button id="toggleStyleBtn">Toggle Style</button>
        </section>
        
        <section>
            <button id="addElementBtn">Add New Element</button>
        </section>
    </main>

    <footer>
        <p>© 2025 Your Company</p>
    </footer>

    <script>

        document.getElementById("changeTextBtn").addEventListener("click", function() {
            document.getElementById("text").textContent = "The text has been changed!";
        });

        document.getElementById("toggleStyleBtn").addEventListener("click", function() {
            const textElement = document.getElementById("text");
            if (textElement.style.color === "blue") {
                textElement.style.color = "black";
                textElement.style.fontSize = "16px";
            } else {
                textElement.style.color = "blue";
                textElement.style.fontSize = "20px";
            }
        });
        document.getElementById("addElementBtn").addEventListener("click", function() {
            const newElement = document.createElement("p");
            newElement.textContent = "This is a newly added paragraph!";
            document.querySelector("main").appendChild(newElement);
        });
    </script>
</body>
</html>

