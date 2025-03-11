# Hello everyone! 👋

My name is **Najam**.

- 🔭 **I’m currently working on:** Data Analysis
- 🌱 **I’m currently learning:** Generative AI
- 💬 **Ask me about:** Python and C++
- 📫 **How to reach me:** [mirpince120@gmail.com](mailto:mirpince120@gmail.com)
- ⚡ **Fun fact:** My email is *childish* 😄

<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Exiting Terminal</title>
  <style>
    body {
      margin: 0;
      padding: 0;
      background: black;
      color: #00ff00;
      font-family: "Courier New", Courier, monospace;
      overflow: hidden;
    }

    #terminal {
      white-space: pre-wrap;
      font-size: 16px;
      padding: 20px;
    }
  </style>
</head>
<body>
  <div id="terminal"></div>

  <script>
    const terminal = document.getElementById("terminal");

    const exitCommands = [
      "Closing session...",
      "Finalizing saved work...",
      "Disconnecting from terminal...",
      "Clearing session cache...",
      "Terminal exited successfully. Goodbye!"
    ];

    function typeCommand(command, speed) {
      return new Promise((resolve) => {
        let index = 0;
        const interval = setInterval(() => {
          terminal.textContent += command[index];
          index++;
          if (index === command.length) {
            clearInterval(interval);
            terminal.textContent += "\n";
            resolve();
          }
        }, speed);
      });
    }

    async function runExitCommands() {
      for (let command of exitCommands) {
        await typeCommand("> " + command, 50);
      }
    }

    // Run the exit sequence
    runExitCommands();
  </script>
</body>
</html>
