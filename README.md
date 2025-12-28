<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Loja PB - Mercado de Contas</title>
    <style>
        body { font-family: Arial, sans-serif; background-color: #121212; color: white; text-align: center; }
        .container { padding: 20px; }
        .card { background: #1e1e1e; border: 1px solid #333; border-radius: 10px; padding: 15px; margin: 10px; display: inline-block; width: 250px; }
        .price { color: #27ae60; font-size: 20px; font-weight: bold; }
        button { background: #00b894; color: white; border: none; padding: 10px 20px; border-radius: 5px; cursor: pointer; margin-top: 10px; }
        .pix-area { margin-top: 20px; background: #2d3436; padding: 20px; display: none; }
    </style>
</head>
<body>

<div class="container">
    <h1>🛒 Loja de Contas Point Blank</h1>
    <p>Escolha sua conta e pague via PIX</p>

    <div class="card">
        <h3>Conta Coronel - Full Cash</h3>
        <p>Itens: Aug G, Kriss, Personagens</p>
        <p class="price">R$ 50,00</p>
        <button onclick="mostrarPix('50,00')">Comprar Agora</button>
    </div>

    <div id="pix-container" class="pix-area">
        <h2>Pagamento via PIX</h2>
        <p>Sua chave PIX: <strong>SUA_CHAVE_AQUI</strong></p>
        <p>Valor: R$ <span id="valor-pix"></span></p>
        <p><em>Após pagar, envie o comprovante no WhatsApp para receber o login na hora!</em></p>
        <a href="https://wa.me/SEUNUMERO" target="_blank">
            <button style="background: #25d366;">Enviar Comprovante (WhatsApp)</button>
        </a>
    </div>
</div>

<script>
    function mostrarPix(valor) {
        document.getElementById('pix-container').style.display = 'block';
        document.getElementById('valor-pix').innerText = valor;
        window.scrollTo(0, document.body.scrollHeight);
    }
</script>

</body>
</html>
