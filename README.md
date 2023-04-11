<!DOCTYPE html>
<html>
  <head>
    <meta charset="UTF-8">
    <title>Círculo se movendo para baixo</title>
  </head>
  <body>
    <canvas id="myCanvas" width="200" height="200"></canvas>

    <script>
      // Seleciona o elemento canvas
      var canvas = document.getElementById("myCanvas");

      // Define o contexto do canvas para 2D
      var ctx = canvas.getContext("2d");

      // Define as propriedades do círculo
      var x = canvas.width/2;
      var y = 10;
      var raio = 10;
      var dy = 2;

      // Desenha o círculo
      function desenhaCirculo() {
        ctx.beginPath();
        ctx.arc(x, y, raio, 0, Math.PI*2);
        ctx.fillStyle = "#0095DD";
        ctx.fill();
        ctx.closePath();
      }

      // Função de animação para mover o círculo para baixo
      function moveCirculo() {
        // Limpa o canvas
        ctx.clearRect(0, 0, canvas.width, canvas.height);

        // Desenha o círculo na nova posição
        desenhaCirculo();
        
        // Move o círculo para baixo
        y += dy;
      }

      // Define o intervalo de animação
      setInterval(moveCirculo, 10);
    </script>
  </body>
</html>
