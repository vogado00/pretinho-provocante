# pretinho-provocante
<!DOCTYPE html>

<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>quer sair comigo?</title>
</head>

<body>
    <div id="conteudo">
        <h2>Aceita sair comigo?</h2>
        <div style="margin: auto;width: 170px;">
            <button style="position: fixed;display: block;" class="btn" onclick="sim()">SIM</button>
            <button class="btn" onclick="desvia(this)" onmouseover="desvia(this)" style="position: absolute;">NÃO</button>
        </div>
    </div>
</body>
<style>
    #conteudo {
        background: #ff7a7a;
        width: 100%;
        height: 100%;
        position: fixed;
        top: 0;
        left: 0;
        padding: 10px;
        text-align: center;
        font-family: sans-serif;
    }

    .btn {
        background: black;
        color: white;
        border: none;
        padding: 10px;
        width: 80px;
        border-radius: 5px;
    }
</style>

<script>
    function sim() {
        alert("Você aceitou sair comigo! :)");
        // redireciona para um URL após clicar no SIM
        location.href = "https://open.spotify.com/track/43TfOO2Dspo5zj2PpH6M84?si=hGgPHYBaThyWqVQUGrfntg";
    }

    function desvia(btn) {
        // btn declarado na função
        btn.style.position = 'absolute';
        btn.style.bottom = geraPosicao(10, 90);
        btn.style.left = geraPosicao(10, 90);
        console.log('opa, desviei...');
    }

    function geraPosicao(min, max) {
        return (Math.random() * (max - min) + min) + "%";
    }

</script>

</html>
