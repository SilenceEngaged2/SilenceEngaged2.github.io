
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Silence — Links</title>
  <meta name="color-scheme" content="dark">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@500&display=swap" rel="stylesheet">
  <style>
    :root { --bg:#0b0d10; --text:#e6e9ef; --radius:14px; }
    body { margin:0; font-family:Inter,sans-serif; background:var(--bg); color:var(--text); }
    .container { max-width:720px; margin:auto; padding:32px 16px; text-align:center; }
    header { margin-bottom:32px; }
    .avatar {
      width:80px; height:80px;
      border-radius:50%;
      object-fit:cover;
      border:2px solid #242b37;
      transition: box-shadow 0.3s ease, border-color 0.3s ease;
    }
    .avatar:hover {
      border-color:#ff0000;
      box-shadow:0 0 12px #ff0000;
    }
    h1 { margin:12px 0 4px; font-size:1.8rem; }
    p { margin:0; color:#a9b0bc; }
    .links {
      display:grid;
      grid-template-columns: repeat(auto-fit, minmax(140px, 1fr));
      gap:16px;
      margin-top:24px;
    }
    .link {
      display:flex; flex-direction:column; align-items:center; justify-content:center;
      padding:20px; border-radius:var(--radius);
      background:#12161d; border:1px solid #242b37;
      text-decoration:none; color:var(--text);
      transition: box-shadow 0.3s ease, border-color 0.3s ease, transform 0.2s ease;
    }
    .link:hover {
      border-color:#ff0000;
      box-shadow:0 0 12px #ff0000;
      transform:translateY(-2px);
    }
    .label { font-weight:500; margin-top:10px; }
    img.icon { width:32px; height:32px; }
    .footer { margin-top:32px; font-size:0.9rem; color:#a9b0bc; }
    button.copy {
      padding:10px 16px; border-radius:var(--radius);
      border:1px solid #242b37; background:#12161d;
      color:var(--text); cursor:pointer;
    }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <img class="avatar" src="https://i.ibb.co/Ndt1xtSB/Batman.png" alt="Profile avatar">
      <h1 id="site-title">SilenceEngaged</h1>
      <p>Catholic • Patriot • Batman Fan • Information Security consultant • Patriots, Red Sox, Bruins and Celtics Fan.</p>
    </header>

    <section class="links">
      <a class="link" href="https://github.com/SilenceEngaged2" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/github/ffffff" alt="">
        <div class="label">GitHub</div>
      </a>
      <a class="link" href="https://www.snapchat.com/add/SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/snapchat/ffffff" alt="">
        <div class="label">Snapchat</div>
      </a>
      <a class="link" href="https://x.com/SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/x/ffffff" alt="">
        <div class="label">X</div>
      </a>
      <a class="link" href="https://instagram.com/silence.engaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/instagram/ffffff" alt="">
        <div class="label">Instagram</div>
      </a>
      <a class="link" href="https://rumble.com/user/SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/rumble/ffffff" alt="">
        <div class="label">Rumble</div>
      </a>
      <a class="link" href="https://www.threads.net/@silence.engaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/threads/ffffff" alt="">
        <div class="label">Threads</div>
      </a>
      <a class="link" href="https://kick.com/SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/kick/ffffff" alt="">
        <div class="label">Kick</div>
      </a>
      <a class="link" href="https://twitch.tv/SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/twitch/ffffff" alt="">
        <div class="label">Twitch</div>
      </a>
      <a class="link" href="https://tiktok.com/@SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/tiktok/ffffff" alt="">
        <div class="label">TikTok</div>
      </a>
      <a class="link" href="https://youtube.com/@SilenceEngaged" target="_blank" rel="noopener">
        <img class="icon" src="https://cdn.simpleicons.org/youtube/ffffff" alt="">
        <div class="label">YouTube</div>
      </a>
    </section>

    <section class="footer">
      <button class="copy" id="copy-url">Copy page URL</button>
      <span id="toast"></span>
    </section>
  </div>

  <script>
    const toast = msg => { const el=document.getElementById('toast'); el.textContent=msg; setTimeout(()=>el.textContent='',1500); };
    document.getElementById('copy-url').addEventListener('click', async () => {
      try { await navigator.clipboard.writeText(location.href); toast('Link copied'); }
      catch { toast('Copy failed'); }
    });
  </script>
</body>
