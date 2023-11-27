# Random-Quote-Generator-pro
This is a Random Quote Generator pro 2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Random Quote Generator</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 50px;
        }

        #quote-container {
            max-width: 600px;
            margin: 0 auto;
            padding: 20px;
            border: 1px solid #ccc;
            border-radius: 8px;
        }

        #quote {
            font-size: 18px;
            margin-bottom: 20px;
        }

        #author {
            font-style: italic;
            color: #555;
        }

        #new-quote-btn {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #007BFF;
            color: #fff;
            border: none;
            border-radius: 4px;
        }
    </style>
</head>
<body>

<div id="quote-container">
    <p id="quote">Click the button below to get a random quote.</p>
    <p id="author"></p>
    <button id="new-quote-btn" onclick="getRandomQuote()">New Quote</button>
</div>

<script>
    // Array of quotes and authors
    const quotes = [
        { quote: "The only way to do great work is to love what you do.", author: "Steve Jobs" },
        { quote: "In the end, we will remember not the words of our enemies, but the silence of our friends.", author: "Martin Luther King Jr." },
        { quote: "Success is not final, failure is not fatal: It is the courage to continue that counts.", author: "Winston Churchill" },
        { quote: "The only limit to our realization of tomorrow will be our doubts of today.", author: "Franklin D. Roosevelt" },
        { quote: "Your time is limited, don't waste it living someone else's life.", author: "Steve Jobs" }
    ];

    function getRandomQuote() {
        const randomIndex = Math.floor(Math.random() * quotes.length);
        const randomQuote = quotes[randomIndex];

        document.getElementById("quote").innerHTML = randomQuote.quote;
        document.getElementById("author").innerHTML = `- ${randomQuote.author}`;
    }
</script>

</body>
</html>
