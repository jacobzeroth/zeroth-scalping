<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>Zeroth Scalping</title>
  <style>
    body {
      margin: 0;
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      background-color: #0e0e0e;
      color: #f1f1f1;
    }
    header {
      text-align: center;
      padding: 2rem 1rem;
      background-color: #1a1a1a;
      box-shadow: 0 4px 12px rgba(255, 255, 255, 0.05);
    }
    header h1 {
      margin: 0;
      font-size: 2.5rem;
      color: #00ffcc;
    }
    header p {
      margin-top: 0.5rem;
      font-size: 1.2rem;
      color: #aaa;
    }
    .chart-container, .signals {
      padding: 2rem 1rem;
      max-width: 900px;
      margin: 0 auto;
    }
    .chart-container h2, .signals h2 {
      color: #00ffcc;
      margin-bottom: 1rem;
    }
    iframe {
      width: 100%;
      border: none;
      border-radius: 10px;
      height: 300px;
    }
    #signal-output {
      background-color: #1a1a1a;
      padding: 1.5rem;
      font-size: 1.4rem;
      text-align: center;
      border: 1px solid #333;
      border-radius: 12px;
      margin-top: 1rem;
    }
    footer {
      text-align: center;
      padding: 1.5rem;
      background-color: #111;
      color: #555;
      font-size: 0.9rem;
      border-top: 1px solid #222;
    }
  </style>
</head>
<body>
  <header>
    <h1>Zeroth Scalping</h1>
    <p>Free 1-Minute Scalping Strategy Dashboard</p>
  </header>
  <main>
    <section class="chart-container">
      <h2>Live BTC/USDT Chart</h2>
      <iframe 
        src="https://s.tradingview.com/embed-widget/mini-symbol-overview/?symbol=BINANCE:BTCUSDT"
        allowtransparency="true" scrolling="no" allowfullscreen>
      </iframe>
    </section>
    <section class="signals">
      <h2>Auto Trade Signals</h2>
      <div id="signal-output">Waiting for signals...</div>
    </section>
  </main>
  <footer>
    <p>Made with 💹 by Zeroth — Free & Open Source</p>
  </footer>
  <script>
    const output = document.getElementById("signal-output");
    function generateSignal() {
      const signals = ["🔼 BUY", "🔽 SELL", "⏸️ HOLD"];
      const random = Math.floor(Math.random() * signals.length);
      const now = new Date().toLocaleTimeString();
      output.textContent = `${signals[random]} @ ${now}`;
    }
    setInterval(generateSignal, 5000); // every 5 seconds
  </script>
</body>
</html>
