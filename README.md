<!DOCTYPE html>
<html>
<head>
  <meta http-equiv="Content-Type" content="text/html; charset=utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style type="text/css">
    body {
      background-color: #1a1a1a;
      color: #ffffff;
      font-family: Arial, sans-serif;
    }

    nav {
      margin-top: 10px
      margin: 10px;
      padding: 10px;
      border: 4px solid black;
      border-radius: 10px;
      background-color: #1a1a1a;
      color: #ffffff;
    }

    p {
      text-align: center;
    }

    button.floating-button {
      display: block;
      margin: 10px auto;
      border: none;
      border-radius: 5px;
      padding: 10px 20px;
      background-color: #0000CD;
      color: white;
      font-size: 16px;
      cursor: pointer;
    }

    h1 {
      font-size: 1.8em;
      text-align: center;
    }

    img {
      max-width: 100%;
      height: auto;
    }
  </style>
</head>
  <h1>Presale Coin</h1>
  <hr>

  <script src="https://unpkg.com/@tonconnect/ui@latest/dist/tonconnect-ui.min.js"></script>
<div id="ton-connect" style="position: absolute; top: 20%; right: 20%"></div>
<script>
    const tonConnectUI = new TON_CONNECT_UI.TonConnectUI({
        manifestUrl: 'https://raw.githubusercontent.com/purplemeth/presalebot/main/tonconnect-manifest.json',
        buttonRootId: 'ton-connect'
    });
</script>
<script>
    async function connectToWallet() {
        const connectedWallet = await tonConnectUI.connectWallet();
        // Do something with connectedWallet if needed
        console.log(connectedWallet);
    }

    // Call the function
    connectToWallet().catch(error => {
        console.error("Error connecting to wallet:", error);
    });
    await tonConnectUI.disconnect();
</script>

  
<body>
<nav>
<strong>No Active  <img src="https://i.postimg.cc/657qFJPZ/pngtree-circle-clipart-gray-circle-png-image-2381994.png" width="12" height="12"></strong><br>
  <center><img src="https://i.postimg.cc/QCZbCcwt/photo-2024-02-24-19-29-37.png" width="75" height="75" alt="Logo"></center>
  <strong><p>MATVEY JETTON</p></strong>
  <strong><p>1 MATVEY = 0.003 TON</p></strong>
  <strong><p>Soft cap 100 TON</p></strong>
  <nav>
    <strong><p>Liquidity Pool: 100%</p></strong>
    <strong><p>Offered: 10,000 MATVEY</p></strong>
  </nav>
  <strong><p>Progress (50%) 50/100 TON</p></strong>
  <center><progress max="100" value="50">Загружено на <span id="value">50%</span></progress></center>
    <center><button type="submit" class="floating-button"><strong>Buy Token</strong></button></center>
</nav>
</body>
</html>
