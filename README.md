<!DOCTYPE html>
<html lang="pt-BR">
    <head>
        <title>Exemplo de arco 1</title>
        <meta charset="UTF-8">
        <!-- Incício do Script do Canvas -->        
        <script>
            function draw(){
                var canvas = document.getElementById('meuCanvas');
                if (canvas.getContext){
                    var cntxt = canvas.getContext('2d');
                    /*Exemplo de desenho com arc*/
                    cntxt.beginPath();
                    cntxt.moveTo(120,50);
                    cntxt.lineTo(150,70);
                    cntxt.lineTo(140,90);
                    cntxt.lineTo(100,90);
                    cntxt.lineTo(90,70);
                    cntxt.closePath();
                    cntxt.fillstyle="rgb(100,200,100)";
                    cntxt.fill();
                }
            }
        </script>        
        <!-- Fim do Script do canvas-->        
    </head>
    <body onload="draw();">
        <h1>Exemplo de arco 1</h1>
        <div>
            <canvas id="meuCanvas" width="500" height="500" style="border:1px solid #000000; background-color: white;"></canvas>
        </div>
    </body>
</html>





<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <title>happyface all</title>
    <meta charset="UTF-8">
    <!-- Inicio do Script do Canvas -->
    <script>
        function draw() {
            var canvas = document.getElementById('meuCanvas');
            if (canvas.getContext) {
                var cntxt = canvas.getContext('2d');

                // Desenho do rosto feliz
                cntxt.beginPath();
                cntxt.fillStyle = "rgba(255, 255, 0)";
                cntxt.arc(75, 75, 50, 0, Math.PI * 2, true); // Círculo exterior
                cntxt.fill();
                cntxt.moveTo(40, 75);
                cntxt.arc(75, 75, 35, 0, Math.PI, false); // Boca (sentido horário)
                cntxt.moveTo(65, 65);
                cntxt.arc(60, 65, 5, 0, Math.PI * 2, true); // Olho esquerdo
                cntxt.moveTo(95, 65);
                cntxt.arc(90, 65, 5, 0, Math.PI * 2, true); // Olho direito
                cntxt.stroke();
                cntxt.closePath();

                // Desenho com bezierCurveTo
                cntxt.beginPath();
                cntxt.fillStyle = "rgb(255, 0, 0)";
                cntxt.moveTo(200, 100);
                cntxt.bezierCurveTo(120, 50, 120, 200, 200, 200);
                cntxt.moveTo(200, 100);
                cntxt.bezierCurveTo(280, 50, 280, 200, 200, 200);
                cntxt.fill();
                cntxt.stroke();
                cntxt.closePath();
                
                cntxt.beginPath();
                cntxt.fillStyle = "rgb(0, 255, 0)";
                cntxt.moveTo(200, 100);
                cntxt.bezierCurveTo(190, 50, 250, 30, 280, 30);
                cntxt.fill();
                cntxt.stroke();
                cntxt.closePath();

                // Desenho com quadraticCurveTo
                cntxt.beginPath();
                cntxt.fillStyle = "rgb(0, 255, 0)";
                cntxt.moveTo(350, 200);
                cntxt.quadraticCurveTo(300, 250, 350, 300);
                cntxt.fill();
                cntxt.stroke();
                cntxt.beginPath();
                cntxt.moveTo(350, 200);
                cntxt.quadraticCurveTo(400, 250, 350, 300);
                cntxt.fill();
                cntxt.stroke();
                cntxt.closePath();
            }
        }
    </script>
    <!-- Fim do Script do canvas-->
</head>
<body onload="draw();">
    <h1>Happy face (jorge)</h1>
    <div>
        <canvas id="meuCanvas" width="500" height="500" style="border:1px solid #000000; background-color: white;"></canvas>
    </div>
</body>
</html>
