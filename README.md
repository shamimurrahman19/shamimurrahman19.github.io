<!DOCTYPE html>
<html>
  <head>
    <title>Mohammad Shamimur Rahman</title>
    <style>
      /* Define the size and position of the cube */
      .cube {
        width: 200px;
        height: 200px;
        position: absolute;
        top: 50%;
        left: 50%;
        margin-top: -100px;
        margin-left: -100px;
        perspective: 800px;
      }
      
      /* Define the appearance of the cube */
      .cube figure {
        position: absolute;
        width: 100%;
        height: 100%;
        padding: 10px;
        box-sizing: border-box;
        background: #ccc;
        border: 1px solid #999;
      }
      
      /* Define the appearance of the cube's faces */
      .cube figure div {
        position: absolute;
        width: 100%;
        height: 100%;
        background: #ccc;
        border: 1px solid #999;
      }
      
      /* Define the position of the front face */
      .cube .front {
        transform: translateZ(100px);
      }
      
      /* Define the position of the back face */
      .cube .back {
        transform: rotateY(180deg) translateZ(100px);
      }
      
      /* Define the position of the right face */
      .cube .right {
        transform: rotateY(90deg) translateZ(100px);
      }
      
      /* Define the position of the left face */
      .cube .left {
        transform: rotateY(-90deg) translateZ(100px);
      }
      
      /* Define the position of the top face */
      .cube .top {
        transform: rotateX(90deg) translateZ(100px);
      }
      
      /* Define the position of the bottom face */
      .cube .bottom {
        transform: rotateX(-90deg) translateZ(100px);
      }
    </style>
  </head>
  <body>
    <div class="cube">
      <figure>
        <div class="front"></div>
        <div class="back"></div>
        <div class="right"></div>
        <div class="left"></div>
        <div class="top"></div>
        <div class="bottom"></div>
      </figure>
    </div>
    
    <script>
      // Get a reference to the cube element
      var cube = document.querySelector(".cube");
      
      // Animate the cube's rotation
      function animate() {
        cube.style.transform = "rotateX(-20deg) rotateY(-45deg)";
        setTimeout(function() {
          cube.style.transform = "none";
        }, 2000);
      }
      
      animate();
      setInterval(animate, 3000);
    </script>
  </body>
</html>
