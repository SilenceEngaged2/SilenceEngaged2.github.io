# SilenceEngaged2.github.io
<!doctype html>
<html>
<head>
  <meta charset="utf-8">
  <title>Page Blocked</title>
  <style>
    body { font-family: sans-serif; background:#f5f5f5; text-align:center; padding:50px; }
    .card { background:white; padding:30px; border-radius:10px; box-shadow:0 2px 10px rgba(0,0,0,0.1); display:inline-block; }
    h1 { color:#d9534f; }
  </style>
</head>
<body>
  <div class="card">
    <h1>🚫 Page Blocked</h1>
    <p>This site has been blocked by your network policy.</p>
    <p id="domain"></p>
  </div>
  <script>
    const params = new URLSearchParams(location.search);
    const host = params.get("host");
    if (host) document.getElementById("domain").textContent = "Domain: " + host;
  </script>
</body>
</html>
