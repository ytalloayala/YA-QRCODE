 <!DOCTYPE html>
<html lang="pt-BR">
<head>
  <meta charset="UTF-8">
  <title>YA-QRCODE Generator</title>
  <style>
    body { font-family: Arial, sans-serif; text-align: center; margin-top: 50px; }
    input { padding: 10px; width: 300px; margin: 10px; }
    button { margin: 10px; padding: 10px 20px; font-size: 16px; cursor: pointer; }
    #qrcode { margin-top: 20px; }
  </style>
</head>
<body>
  <h1>Gerador de QR Code</h1>
  
  <input type="text" id="texto" placeholder="Digite o texto ou link">
  <br>
  <button onclick="gerarQRCode()">Gerar QR Code</button>
  <button onclick="baixarQRCode()">Baixar QR Code</button>
  
  <div id="qrcode"></div>
  
  <!-- Biblioteca QRCode.js -->
  <script src="https://cdnjs.cloudflare.com/ajax/libs/qrcodejs/1.0.0/qrcode.min.js"></script>
  <script>
    let qrcode;
    
    function gerarQRCode() {
      const texto = document.getElementById("texto").value;
      document.getElementById("qrcode").innerHTML = "";
      qrcode = new QRCode(document.getElementById("qrcode"), {
        text: texto,
        width: 200,
        height: 200
      });
    }
    
    function baixarQRCode() {
      if (!qrcode) {
        alert("Primeiro gere um QR Code!");
        return;
      }
      const canvas = document.querySelector("#qrcode canvas");
      const link = document.createElement("a");
      link.download = "qrcode.png";
      link.href = canvas.toDataURL("image/png");
      link.click();
    }
  </script>
</body>
</html>


# YA-QRCODE
O repositório YA-QRCODE é a base inicial do projeto YA System, uma iniciativa voltada para integrar tecnologia, inovação e acessibilidade em um formato simples e direto. A proposta central é criar uma plataforma que utilize QR Codes como ponte entre conteúdos digitais e experiências interativas, permitindo que qualquer pessoa acesse.

 # YA CCORE
