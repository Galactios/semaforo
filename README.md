# semaforo
<html>
<head>
  <style>
    #traffic-light {
      width: 199px;
      height: 300px;
      margin: 100px auto;
      position: relative;
      border: 2px solid black;
    }
    
    .bulb {
      width: 100px;
      height: 100px;
      border-radius: 50%;
      position: absolute;
      bottom: 0;
    }
    
    #red {
      background-color: red;
      left: 50px;
    }
    
    #yellow {
      background-color: yellow;
      left: 50px;
      bottom: 100px;
    }
    
    #green {
      background-color: green;
      left: 50px;
      bottom: 200px;
    }
  </style>
</head>
<body>
  <div id="traffic-light">
    <div id="red" class="bulb"></div>
    <div id="yellow" class="bulb"></div>
    <div id="green" class="bulb"></div>
  </div>
  
  <script>
    const trafficLight = document.querySelector("#traffic-light");
    const red = document.querySelector("#red");
    const yellow = document.querySelector("#yellow");
    const green = document.querySelector("#green");
    
    let currentLight = "green";
    
    setInterval(() => {
      if (currentLight === "green") {
        green.style.backgroundColor = "gray";
        yellow.style.backgroundColor = "yellow";
        currentLight = "yellow";
      } else if (currentLight === "yellow") {
        yellow.style.backgroundColor = "gray";
        red.style.backgroundColor = "red";
        currentLight = "red";
      } else if (currentLight === "red") {
        red.style.backgroundColor = "gray";
        green.style.backgroundColor = "green";
        currentLight = "green";
      }
    }, 1000);
  </script>
</body>
</html>
