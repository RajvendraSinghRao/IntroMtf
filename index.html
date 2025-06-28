<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Live NSE Stock Prices (Yahoo Finance)</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: #f4f4f4;
      text-align: center;
      padding: 40px;
    }
    table {
      margin: auto;
      border-collapse: collapse;
      width: 80%;
      background: white;
      box-shadow: 0 0 10px rgba(0,0,0,0.1);
    }
    th, td {
      padding: 12px;
      border: 1px solid #ddd;
    }
    th {
      background-color: #007bff;
      color: white;
    }
    .price {
      color: green;
      font-weight: bold;
    }
    .error {
      color: red;
    }
  </style>
</head>
<body>

<h1>Live NSE Stock Prices (Powered by Yahoo Finance)</h1>
<table>
  <thead>
    <tr>
      <th>Company</th>
      <th>Symbol</th>
      <th>Price (INR)</th>
    </tr>
  </thead>
  <tbody id="stock-table"></tbody>
</table>

<script>
  const rapidApiKey = "bbaeb02be6msh9a9da0403d69311p1ed7fejsn8df7214e4b7b"; // ✅ Your API Key

  const stocks = [
    { name: "Reliance", symbol: "RELIANCE.NS" },
    { name: "TCS", symbol: "TCS.NS" },
    { name: "Infosys", symbol: "INFY.NS" },
    { name: "HDFC Bank", symbol: "HDFCBANK.NS" },
    { name: "ICICI Bank", symbol: "ICICIBANK.NS" }
  ];

  const table = document.getElementById("stock-table");

  // Build table rows
  stocks.forEach(stock => {
    const row = document.createElement("tr");
    row.innerHTML = `
      <td>${stock.name}</td>
      <td>${stock.symbol}</td>
      <td id="${stock.symbol.replace('.', '')}">Loading...</td>
    `;
    table.appendChild(row);
  });

  async function fetchPrices() {
    const symbols = stocks.map(s => s.symbol).join(",");
    const url = `https://apidojo-yahoo-finance-v1.p.rapidapi.com/market/v2/get-quotes?region=IN&symbols=${symbols}`;

    try {
      const res = await fetch(url, {
        method: "GET",
        headers: {
          "X-RapidAPI-Key": rapidApiKey,
          "X-RapidAPI-Host": "apidojo-yahoo-finance-v1.p.rapidapi.com"
        }
      });

      const data = await res.json();
      const results = data.quoteResponse.result;

      results.forEach(stock => {
        const cell = document.getElementById(stock.symbol.replace('.', ''));
        if (stock.regularMarketPrice !== undefined) {
          cell.textContent = `₹${stock.regularMarketPrice.toFixed(2)}`;
          cell.classList.remove("error");
          cell.classList.add("price");
        } else {
          cell.textContent = "Unavailable";
          cell.classList.add("error");
        }
      });

    } catch (error) {
      console.error("API fetch error:", error);
      stocks.forEach(s => {
        const cell = document.getElementById(s.symbol.replace('.', ''));
        cell.textContent = "Error";
        cell.classList.add("error");
      });
    }
  }

  fetchPrices();
  setInterval(fetchPrices, 15000); // Update every 15 seconds
</script>

</body>
</html>
