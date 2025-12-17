<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1"/>
  <title>Made in Heaven — Enquiry System</title>

  <style>
    :root{
      --bg:#070712;
      --card:#0d0d1c;
      --text:#e9e9ff;
      --muted:#a8a8c7;
      --line:#1f1f3d;
      --glow: 0 0 18px rgba(255, 92, 231, .35), 0 0 32px rgba(92, 173, 255, .20);
      --grad: linear-gradient(135deg, #ff5ce7, #5cadff, #7bffb5);
      --btn: linear-gradient(135deg, #ff5ce7, #5cadff);
      --btnHover: linear-gradient(135deg, #ff7aef, #7bc0ff);
      --shadow: 0 16px 40px rgba(0,0,0,.55);
      --radius: 18px;
      --mono: ui-monospace, SFMono-Regular, Menlo, Monaco, Consolas, monospace;
      --sans: ui-sans-serif, system-ui, -apple-system, Segoe UI, Roboto, Helvetica, Arial;
    }

    *{ box-sizing:border-box; }
    body{
      margin:0;
      font-family: var(--sans);
      background:
        radial-gradient(800px 400px at 20% 10%, rgba(255,92,231,.18), transparent 55%),
        radial-gradient(900px 500px at 80% 30%, rgba(92,173,255,.18), transparent 60%),
        radial-gradient(700px 500px at 50% 90%, rgba(123,255,181,.10), transparent 60%),
        var(--bg);
      color: var(--text);
      min-height:100vh;
      display:flex;
      align-items:center;
      justify-content:center;
      padding:24px;
    }

    .card{
      width: min(860px, 100%);
      border:1px solid rgba(255,255,255,.08);
      background: rgba(13,13,28,.75);
      border-radius: var(--radius);
      box-shadow: var(--shadow);
      padding:24px;
    }

    .header{
      display:flex;
      gap:14px;
      align-items:center;
      margin-bottom:14px;
    }

    .badge{
      width:56px;
      height:56px;
      border-radius:16px;
      display:grid;
      place-items:center;
      font-weight:900;
      font-size:18px;
      background: var(--btn);
      box-shadow: var(--glow);
      color:#090915;
    }

    h1{
      margin:0;
      font-size:22px;
    }

    .sub{
      color: var(--muted);
      font-size:14px;
      margin-top:4px;
    }

    .desc{
      margin: 14px 0 18px;
      font-size:14px;
      line-height:1.6;
      color: rgba(233,233,255,.9);
    }

    .grid{
      display:grid;
      grid-template-columns: repeat(3, 1fr);
      gap:14px;
    }

    @media (max-width: 820px){
      .grid{ grid-template-columns: 1fr; }
    }

    .linkCard{
      border:1px solid rgba(255,255,255,.08);
      background: rgba(0,0,0,.25);
      border-radius:16px;
      padding:16px;
      transition:.15s ease;
      text-decoration:none;
      color: var(--text);
      display:block;
    }

    .linkCard:hover{
      transform: translateY(-2px);
      box-shadow: var(--glow);
      border-color: rgba(255,92,231,.35);
    }

    .linkTitle{
      font-weight:900;
      margin-bottom:6px;
    }

    .linkDesc{
      font-size:13px;
      color: var(--muted);
      line-height:1.5;
    }

    .footer{
      margin-top:18px;
      padding-top:12px;
      border-top:1px solid rgba(255,255,255,.08);
      font-size:12px;
      color: var(--muted);
      display:flex;
      justify-content:space-between;
      flex-wrap:wrap;
      gap:8px;
    }

    .mono{ font-family: var(--mono); }
  </style>
</head>
<body>

  <div class="card">
    <div class="header">
      <div class="badge">MIH</div>
      <div>
        <h1>Made in Heaven — Customer Enquiry System</h1>
        <div class="sub">Cloud-based enquiry inbox (Option A — Customer Enquiry Inbox)</div>
      </div>
    </div>

    <p class="desc">
      This system demonstrates a cloud-based business application built using GitHub Pages and
      Firebase Firestore. It allows customers to submit enquiries, staff to manage them in real time,
      and management to view operational insights.
    </p>

    <div class="grid">
      <a class="linkCard" href="public.html">
        <div class="linkTitle">Public Enquiry Page</div>
        <div class="linkDesc">
          Customer-facing form used to submit enquiries into the live Firestore database.
        </div>
      </a>

      <a class="linkCard" href="staff.html">
        <div class="linkTitle">Staff Dashboard</div>
        <div class="linkDesc">
          Internal real-time inbox where staff triage enquiries and update their status.
          <br/><span class="mono">Login: admin / staff123</span>
        </div>
      </a>

      <a class="linkCard" href="insights.html">
        <div class="linkTitle">Operational Insights</div>
        <div class="linkDesc">
          Management view showing enquiry volume, status distribution, and resolution rate.
        </div>
      </a>
    </div>

    <div class="footer">
      <div>Built with GitHub Pages + Firebase Firestore</div>
      <div class="mono">Real-time updates enabled</div>
    </div>
  </div>

</body>
</html>
