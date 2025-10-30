# DIGITAL-CLOCK
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Digital Clock</title>
<style>
  body {
    background: #282c34;
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
    margin: 0;
    font-family: 'Courier New', Courier, monospace;
  }
  .clock {
    background: #61dafb;
    padding: 30px 50px;
    border-radius: 15px;
    box-shadow: 0 4px 20px rgba(97, 218, 251, 0.5);
    font-size: 60px;
    color: #20232a;
    letter-spacing: 8px;
  }
</style>
</head>
<body>

<div class="clock" id="clock">00:00:00</div>

<script>
  function updateClock() {
    const now = new Date();
    let hours = now.getHours().toString().padStart(2, '0');
    let minutes = now.getMinutes().toString().padStart(2, '0');
    let seconds = now.getSeconds().toString().padStart(2, '0');
    const timeString = `${hours}:${minutes}:${seconds}`;
    document.getElementById('clock').textContent = timeString;
  }

  setInterval(updateClock, 1000);
  updateClock(); // initial call immediately
</script>

</body>
</html>
