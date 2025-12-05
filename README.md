<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Silence — Links</title>
  <meta name="color-scheme" content="dark">
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600;700&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b0d10;
      --panel: #111418;
      --text: #e6e9ef;
      --muted: #a9b0bc;
      --accent: #6aa8ff;
      --accent-2: #9f6aff;
      --ring: rgba(106, 168, 255, 0.35);
      --radius: 14px;
      --shadow: 0 20px 60px rgba(0,0,0,0.35), inset 0 1px 0 rgba(255,255,255,0.03);
    }
    * { box-sizing: border-box; }
    html, body { height: 100%; }
    body {
      margin: 0;
      font-family: Inter, system-ui, -apple-system, Segoe UI, Roboto, "Helvetica Neue", Arial, sans-serif;
      background: radial-gradient(1200px 600px at 10% 10%, #0f1217 0%, var(--bg) 50%) fixed;
      color: var(--text);
      line-height: 1.6;
    }
    .container { max-width: 680px; margin: 0 auto; padding: 32px 16px 64px; }
    header { display: grid; grid-template-columns: auto 1fr auto; gap: 16px; align-items: center; margin-bottom: 20px; }
    .avatar { width: 72px; height: 72px; border-radius: 50%; background: linear-gradient(135deg, #1b1f26, #12151a); border: 1px solid #232834; box-shadow: var(--shadow); }
    .title { display: flex; flex-direction: column; gap: 4px; }
    .title h1 { margin: 0; font-size: 1.5rem; }
    .title p { margin: 0; color: var(--muted); font-size: 0.95rem; }
    .gear { width: 40px; height: 40px; border-radius: 10px; background: #161a21; border: 1px solid #262c38; color: var(--text); cursor: pointer; }
    .links { display: grid; gap: 14px; }
    .link { display: grid; grid-template-columns: 1fr auto; align-items: center; padding: 14px 16px; border-radius: var(--radius); background: #10141a; border: 1px solid #242b37; text-decoration: none; color: var(--text); }
    .link:hover { border-color: #2e3646; }
    .link .label { font-weight: 600; }
    .link .meta { color: var(--muted); font-size: 0.92rem; }
    .chip { display: inline-flex; gap: 8px; align-items: center; padding: 8px 10px; border-radius: 10px; background: #121720; border: 1px solid #242b37; font-size: 0.85rem; }
    .chip .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent); box-shadow: 0 0 8px var(--accent); }
    .footer { margin-top: 26px; display: flex; gap: 10px; flex-wrap: wrap; align-items: center; color: var(--muted); font-size: 0.9rem; }
    .copy { padding: 10px 12px; border-radius: 10px; background: #121720; border: 1px solid #242b37; cursor: pointer; }
    dialog.settings { width: 560px; max-width: 95vw; border: 1px solid #2a3141; border-radius: 16px; background: #11161d; color: var(--text); padding: 18px; }
    dialog::backdrop { backdrop-filter: blur(6px); background: rgba(3,6,9,0.5); }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="avatar"></div>
      <div class="title">
        <h1 id="site-title">Silence</h1>
        <p>Tech • Design • Links that actually work</p>
      </div>
      <button class="gear" id="open-settings">⚙</button>
    </header>

    <main>
      <section class="links">
        <!-- Core links -->
        <a class="link" href="https://github.com/" target="_blank" rel="noopener noreferrer" data-label="GitHub">
          <div><div class="label">GitHub</div><div class="meta">Code, projects</div></div>
          <span class="chip"><span class="dot"></span> Follow</span>
        </a>
        <!-- Social buttons -->
        <a class="link" href="https://www.snapchat.com/add/yourhandle" target="_blank" rel="noopener noreferrer" data-label="Snapchat">
          <div><div class="label">Snapchat</div><div class="meta">@yourhandle</div></div>
          <span class="chip"><span class="dot"></span> Snap</span>
        </a>
        <a class="link" href="https://x.com/yourhandle" target="_blank" rel="noopener noreferrer" data-label="X">
          <div><div class="label">X</div><div class="meta">@yourhandle</div></div>
          <span class="chip"><span class="dot"></span> Posts</span>
        </a>
        <a class="link" href="https://instagram.com/yourhandle" target="_blank" rel="noopener noreferrer" data-label="Instagram">
          <div><div class="label">Instagram</div><div class="meta">@yourhandle</div></div>
          <span class="chip"><span class="dot"></span> Photos</span>
        </a>
        <a class="link" href="https://rumble.com/c/yourchannel" target="_blank" rel="noopener noreferrer" data-label="Rumble">
          <div><div class="label">Rumble</div><div class="meta">Video channel</div></div>
          <span class="chip"><span class="dot"></span> Watch</span>
        </a>
        <a class="link" href="https://www.threads.net/@yourhandle" target="_blank" rel="noopener noreferrer" data-label="Threads">
          <div><div class="label">Threads</div><div class="meta">@yourhandle</div></div>
          <span class="chip"><span class="dot"></span> Chat</span>
        </a>
        <a class="link" href="https://kick.com/yourchannel" target="_blank" rel="noopener noreferrer" data-label="Kick">
          <div><div class="label">Kick</div><div class="meta">Live streaming</div></div>
          <span class="chip"><span class="dot"></span> Live</span>
        </a>
        <a class="link" href="https://twitch.tv/yourchannel" target="_blank" rel="noopener noreferrer" data-label="Twitch">
          <div><div class="label">Twitch</div><div class="meta">Streaming</div></div>
          <span class="chip"><span class="dot"></span> Stream</span>
        </a>
        <a class="link" href="https://tiktok.com/@yourhandle" target="_blank" rel="noopener noreferrer" data-label="TikTok">
          <div><div class="label">TikTok</div><div class="meta">@yourhandle</div></div>
          <span class="chip"><span class="dot"></span> Shorts</span>
        </a>
        <a class="link" href="https://youtube.com/@yourchannel" target="_blank" rel="noopener noreferrer" data-label="YouTube">
          <div><div class="label">YouTube</div><div class="meta">Videos</div></div>
          <span class="chip"><span class="dot"></span> Subscribe</span>
        </a>
      </section>

      <section class="footer">
        <button
Clean the code up
Here’s a cleaned‑up, streamlined version of your full “link in bio” site. I’ve removed redundant styles, tightened selectors, and kept everything in one neat file. It’s still dark‑themed, responsive, and includes all the social buttons you asked for.

html
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Silence — Links</title>
  <meta name="color-scheme" content="dark">
  <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;600&display=swap" rel="stylesheet">
  <style>
    :root {
      --bg: #0b0d10;
      --text: #e6e9ef;
      --muted: #a9b0bc;
      --accent: #6aa8ff;
      --radius: 12px;
    }
    * { box-sizing: border-box; }
    body {
      margin: 0; font-family: Inter, sans-serif;
      background: var(--bg); color: var(--text);
      line-height: 1.6;
    }
    .container { max-width: 640px; margin: auto; padding: 32px 16px; }
    header { display: flex; align-items: center; gap: 16px; margin-bottom: 24px; }
    .avatar { width: 64px; height: 64px; border-radius: 50%; background: #1b1f26; }
    h1 { margin: 0; font-size: 1.5rem; }
    p { margin: 0; color: var(--muted); }
    .links { display: grid; gap: 12px; }
    .link {
      display: flex; justify-content: space-between; align-items: center;
      padding: 12px 16px; border-radius: var(--radius);
      background: #12161d; border: 1px solid #242b37;
      text-decoration: none; color: var(--text);
    }
    .link:hover { border-color: var(--accent); }
    .label { font-weight: 600; }
    .meta { font-size: 0.9rem; color: var(--muted); }
    .chip { display: flex; align-items: center; gap: 6px; font-size: 0.85rem; }
    .dot { width: 8px; height: 8px; border-radius: 50%; background: var(--accent); }
    .footer { margin-top: 24px; font-size: 0.9rem; color: var(--muted); }
    button.copy { padding: 8px 12px; border-radius: var(--radius); border: 1px solid #242b37; background: #12161d; color: var(--text); cursor: pointer; }
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="avatar"></div>
      <div>
        <h1 id="site-title">Silence</h1>
        <p>Tech • Design • Links that actually work</p>
      </div>
    </header>

    <section class="links">
      <a class="link" href="https://github.com/" target="_blank" rel="noopener">
        <div><div class="label">GitHub</div><div class="meta">Code, projects</div></div>
        <span class="chip"><span class="dot"></span> Follow</span>
      </a>
      <a class="link" href="https://www.snapchat.com/add/yourhandle" target="_blank" rel="noopener">
        <div><div class="label">Snapchat</div><div class="meta">@yourhandle</div></div>
        <span class="chip"><span class="dot"></span> Snap</span>
      </a>
      <a class="link" href="https://x.com/yourhandle" target="_blank" rel="noopener">
        <div><div class="label">X</div><div class="meta">@yourhandle</div></div>
        <span class="chip"><span class="dot"></span> Posts</span>
      </a>
      <a class="link" href="https://instagram.com/yourhandle" target="_blank" rel="noopener">
        <div><div class="label">Instagram</div><div class="meta">@yourhandle</div></div>
        <span class="chip"><span class="dot"></span> Photos</span>
      </a>
      <a class="link" href="https://rumble.com/c/yourchannel" target="_blank" rel="noopener">
        <div><div class="label">Rumble</div><div class="meta">Video channel</div></div>
        <span class="chip"><span class="dot"></span> Watch</span>
      </a>
      <a class="link" href="https://www.threads.net/@yourhandle" target="_blank" rel="noopener">
        <div><div class="label">Threads</div><div class="meta">@yourhandle</div></div>
        <span class="chip"><span class="dot"></span> Chat</span>
      </a>
      <a class="link" href="https://kick.com/yourchannel" target="_blank" rel="noopener">
        <div><div class="label">Kick</div><div class="meta">Live streaming</div></div>
        <span class="chip"><span class="dot"></span> Live</span>
      </a>
      <a class="link" href="https://twitch.tv/yourchannel" target="_blank" rel="noopener">
        <div><div class="label">Twitch</div><div class="meta">Streaming</div></div>
        <span class="chip"><span class="dot"></span> Stream</span>
      </a>
      <a class="link" href="https://tiktok.com/@yourhandle" target="_blank" rel="noopener">
        <div><div class="label">TikTok</div><div class="meta">@yourhandle</div></div>
        <span class="chip"><span class="dot"></span> Shorts</span>
      </a>
      <a class="link" href="https://youtube.com/@yourchannel" target="_blank" rel="noopener">
        <div><div class="label">YouTube</div><div class="meta">Videos</div></div>
        <span class="chip"><span class="dot"></span> Subscribe</span>
      </a>
    </section>

    <section class="footer">
      <button class="copy" id="copy-url">Copy page URL</button>
      <span id="toast"></span>
    </section>
  </div>

  <script>
    const toast = msg => {
      const el = document.getElementById('toast');
      el.textContent = msg;
      setTimeout(() => el.textContent = '', 1500);
    };
    document.getElementById('copy-url').addEventListener('click', async () => {
      try {
        await navigator.clipboard.writeText(location.href);
        toast('Link copied');
      } catch {
        toast('Copy failed');
      }
    });
  </script>
</body>
</html>
