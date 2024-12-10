<!DOCTYPE html>
<html>
<head>
  <style>
    body, html {
      height: 100%;
      margin: 0;
      font-family: 'Cursive', Arial, sans-serif;
    }

    .birthdayimg {
      background-image: url('https://cdn.pixabay.com/photo/2018/02/23/21/29/roses-frame-3176667_960_720.jpg');
      height: 100%;
      background-position: center;
      background-size: cover;
      position: relative;
      text-align: center;
      color: black;
    }

    .topleft {
      position: absolute;
      top: 10px;
      left: 20px;
      font-size: 26px;
      color: black;
    }

    .middle {
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      width: 80%; /* Increased width for wider alignment */
    }

    #waitMessage {
      font-size: 70px; /* Larger font for wait message */
      color: red;
      margin-bottom: 20px;
    }

    #amx {
      font-size: 60px; /* Larger font for countdown */
      margin-top: 20px;
    }

    #message {
      font-size: 50px; /* 2x larger font */
      width: 100%; /* Full-width alignment */
      margin: 20px auto;
      text-align: center; /* Center-align text */
      line-height: 1.3; /* Increased line height for better readability */
      color: black;
    }

    .bottomleft {
      position: absolute;
      bottom: 10px;
      left: 20px;
      font-size: 26px;
      color: black;
    }
  </style>
</head>
<body>
  <div class="birthdayimg">
    <div class="topleft">CODING4FUN</div>
    <div class="middle">
      <p id="waitMessage">Wait for the Surprise</p>
      <h1 id="amx">Countdown Loading...</h1>
      <p id="message"></p>
    </div>
    <div class="bottomleft">Created by AmX</div>
  </div>

  <script>
    // Set countdown date
    var countDownDate = new Date("Dec 11, 2024 00:00:00").getTime();

    // Update the countdown every second
    var countdownfunction = setInterval(function () {
      // Current time
      var now = new Date().getTime();

      // Distance between now and countdown date
      var distance = countDownDate - now;

      // Calculate time
      var days = Math.floor(distance / (1000 * 60 * 60 * 24));
      var hours = Math.floor((distance % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
      var minutes = Math.floor((distance % (1000 * 60 * 60)) / (1000 * 60));
      var seconds = Math.floor((distance % (1000 * 60)) / 1000);

      // Display countdown
      document.getElementById("amx").innerHTML =
        days + "D " + hours + "H " + minutes + "M " + seconds + "S ";

      // If countdown is over
      if (distance < 0) {
        clearInterval(countdownfunction);
        document.getElementById("waitMessage").style.display = "none"; // Hide the "Wait for the Surprise" text
        document.getElementById("amx").innerHTML = "HAPPY BIRTHDAY, ELUU! ";
        document.getElementById("message").innerHTML =
          `<b>Happy Birthday to my favorite human, Eluu (My Senorita)!</b><br><br>
          I hope your day is filled with cake, laughter, and all the happiness in the world.
          Today, I promise to annoy you a little less (but just for today).<br>
          Remember, you are stuck with me forever-deal with it!<br>
          <i>Love you more than infinity and beyond!</i>`;
      }
    }, 1000);
  </script>
</body>
</html>
