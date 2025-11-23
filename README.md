<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Access blocked</title>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --bg: #0f1220;
      --card: #161a2f;
      --text: #e6e8f0;
      --muted: #9aa3b2;
      --accent: #6aa9ff;
      --danger: #ff6473;
      --success: #79c888;
      --border: #262b44;
      --focus: #b8d4ff;
    }
    @media (prefers-color-scheme: light){
      :root{
        --bg: #f7f9fc;
        --card: #ffffff;
        --text: #101322;
        --muted: #596074;
        --accent: #2b6eff;
        --danger: #e6455d;
        --success: #199f5e;
        --border: #e6e8ef;
        --focus: #89b6ff;
      }
    }
    html,body{height:100%}
    body{
      margin:0;
      background: radial-gradient(1200px 600px at 10% 10%, rgba(106,169,255,0.12), transparent 50%),
                  radial-gradient(900px 500px at 90% 90%, rgba(255,100,115,0.10), transparent 60%),
                  var(--bg);
      color: var(--text);
      font-family: Inter, system-ui, -apple-system, "Segoe UI", Roboto, Arial, sans-serif;
      display:flex; align-items:center; justify-content:center;
    }
    .wrap{max-width:800px; width:100%; padding:24px}
    .card{
      background: var(--card);
      border: 1px solid var(--border);
      border-radius: 16px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.25);
      overflow: hidden;
    }
    .header{
      display:flex; align-items:center; gap:12px; padding:20px 24px; border-bottom:1px solid var(--border);
      background: linear-gradient(180deg, rgba(106,169,255,0.10), transparent);
    }
    .logo{
      width:36px; height:36px; border-radius:8px; background: linear-gradient(135deg, var(--accent), var(--danger));
      box-shadow: 0 8px 20px rgba(106,169,255,0.3), 0 6px 18px rgba(255,100,115,0.25);
    }
    .brand{
      font-weight:700; letter-spacing:0.2px;
    }
    .body{padding:24px}
    .status{
      display:flex; align-items:center; gap:10px; margin-bottom:14px;
      color: var(--danger); font-weight:600;
    }
    .status .dot{
      width:10px; height:10px; border-radius:50%; background: var(--danger);
      box-shadow: 0 0 12px var(--danger);
    }
    .domain{
      font-size:1.25rem; font-weight:700; margin:6px 0 12px; word-break: break-word;
    }
    .reason, .profile{
      color: var(--muted); margin:6px 0;
    }
    .details{
      margin-top:16px; padding:14px; border:1px dashed var(--border); border-radius:12px; color: var(--muted);
    }
    .actions{
      margin-top:20px; display:flex; flex-wrap:wrap; gap:12px;
    }
    .btn{
      appearance:none; border:1px solid var(--border); background: transparent; color: var(--text);
      padding:10px 14px; border-radius:10px; font-weight:600; cursor:pointer;
      transition: border-color .15s, box-shadow .15s, transform .06s;
    }
    .btn:hover{ border-color: var(--focus); box-shadow: 0 0 0 4px rgba(136, 176, 255, 0.18) }
    .btn:active{ transform: translateY(1px) }
    .btn.primary{ background: var(--accent); color:white; border-color: transparent; }
    .footer{
      padding:16px 24px; border-top:1px solid var(--border); display:flex; justify-content:space-between; align-items:center; color: var(--muted);
      font-size:0.95rem;
    }
    .badge{
      display:inline-flex; align-items:center; gap:8px; padding:8px 12px; border-radius:10px; border:1px solid var(--border); color: var(--muted);
    }
    .badge .pill{
      width:9px; height:9px; border-radius:50%; background: var(--success); box-shadow: 0 0 10px var(--success);
    }
    .tip{font-size:0.95rem; color: var(--muted); margin-top:10px}
    code{background: rgba(255,255,255,0.06); border: 1px solid var(--border); padding:2px 6px; border-radius:6px}
  </style>
</head>
<body>
  <div class="wrap">
    <div class="card">
      <div class="header">
        <div class="logo" aria-hidden="true"></div>
        <div class="brand">Your Network</div>
      </div>
      <div class="body">
        <div class="status">
          <span class="dot" aria-hidden="true"></span>
          <span>Access blocked</span>
        </div>

        <div class="domain" id="domain">Requested domain: —</div>
        <div class="reason" id="reason"></div>
        <div class="profile" id="profile"></div>

        <div class="details">
          This request was blocked according to your DNS filtering policy. If you think this is an error,
          you can request a review or temporarily allow it based on your access level.
        </div>

        <div class="actions">
          <button class="btn primary" id="retry">Retry</button>
          <button class="btn" id="request">Request review</button>
          <button class="btn" id="allow">Temporarily allow (5 min)</button>
        </div>

        <p class="tip">
          Tip: If an app uses its own encrypted DNS, network policies may still apply. Use your approved resolver or VPN profile.
        </p>
      </div>
      <div class="footer">
        <div class="badge">
          <span class="pill" aria-hidden="true"></span>
          Filtering active
        </div>
        <div>© <span id="year"></span> Your Organization</div>
      </div>
    </div>
  </div>

  <script>
    (function(){
      const params = new URLSearchParams(location.search);
      const host = (params.get('host') || '').trim();
      const reason = (params.get('reason') || '').trim();
      const profile = (params.get('profile') || '').trim();

      const domainEl = document.getElementById('domain');
      const reasonEl = document.getElementById('reason');
      const profileEl = document.getElementById('profile');

      if (host) domainEl.textContent = `Requested domain: ${host}`;
      if (reason) reasonEl.textContent = `Reason: ${reason}`;
      if (profile) profileEl.textContent = `Profile: ${profile}`;

      document.getElementById('year').textContent = new Date().getFullYear();

      // Actions: wire these to your own endpoints
      document.getElementById('retry').onclick = () => {
        if (host) location.href = `https://${host}`;
        else history.back();
      };
      document.getElementById('request').onclick = () => {
        const mailto = `mailto:admin@yourdomain.com?subject=Review%20request%20for%20${encodeURIComponent(host || 'unknown')}&body=Please%20review%20block%20for%20${encodeURIComponent(host || 'unknown')}%0AReason:%20${encodeURIComponent(reason || 'n/a')}`;
        location.href = mailto;
      };
      document.getElementById('allow').onclick = async () => {
        alert('Requesting a temporary allow... If approved, retry will work within ~30 seconds.');
        // POST to your allowlist API here with host and a TTL=300
        // fetch('/api/allow-temp', { method:'POST', headers:{'Content-Type':'application/json'}, body: JSON.stringify({ host, ttl:300, reason }) });
      };
    })();
  </script>
</body>
</html>
