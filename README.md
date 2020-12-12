# index.html
<!DOCTYPE html>
<html lang= "en">
<head>
    <meta charset="Utf-8">
    <meta name="viewport" content="width= device-width, initial-scale=1.0">
    <title>Jarvis</title>
</head>
<body>

    <script src="https://cdnjs.cloudflare.com/ajax/libs/annyang/2.6.0/annyang.min.js"></script>
    <script>
        if (annyang) {
        alert("Annyang is working!");

        var messages = ["Greetings Master Adam", "Hello there Sir Smith", "Hi there Adam", "Hello."];

        var commands = {
            'Hello' : greetings,

            'What is your name' : introduction
        }

        // Display Greetings Message
        function greetings(){
            var randomIndex = Math.round(Math.random() * messages.length);
            alert(messages[randomIndex]);

        }

        //Display Introduction Message
        function introduction() {

        }

        //Add Command
        annyang.addCommands(commands);

        // Start Listening

        annyang.start();

        }
    </script>



</body>
