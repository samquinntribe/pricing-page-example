<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>Tribe Pricing – Desktop Mockup</title>
<style>
  :root{
    --bg:#f7fbf9;
    --card:#ffffff;
    --text:#27434a;
    --muted:#6d8589;
    --line:#d9e9e1;
    --brand:#95C4BF;
    --brand-soft:#eaf4f1;
    --brand-dark:#325963;
    --accent:#dfeee9;
    --shadow:0 12px 30px rgba(50,89,99,.08);
  }
  *{box-sizing:border-box}
  body{
    margin:0;
    font-family:-apple-system,BlinkMacSystemFont,"Segoe UI",Roboto,Helvetica,Arial,sans-serif;
    color:var(--text);
    background:linear-gradient(180deg,#fbfefd 0%, #f3faf7 100%);
  }
  .wrap{max-width:1380px;margin:0 auto;padding:28px 24px 80px;}
  .hero{
    display:grid;grid-template-columns:1.25fr .75fr;gap:18px;margin-bottom:22px;
  }
  .hero-main,.hero-side,.access-bar,.filters,.section-card,.pack-card,.hours-card{
    background:#fff;border:1px solid var(--line);border-radius:28px;box-shadow:var(--shadow);
  }
  .hero-main{
    padding:34px;background:linear-gradient(135deg,#f0f8f5 0%, #fbfefd 100%);
  }
  .hero-side{padding:24px}
  .eyebrow{
    display:inline-flex;align-items:center;padding:8px 12px;border-radius:999px;
    background:rgba(50,89,99,.08);color:var(--brand-dark);font-size:12px;
    font-weight:800;letter-spacing:.08em;text-transform:uppercase;margin-bottom:16px;
  }
  h1{
    margin:0 0 12px;font-size:54px;line-height:1.02;letter-spacing:-.045em;max-width:900px;
  }
  .sub{font-size:18px;line-height:1.6;color:var(--muted);max-width:820px;}
  .side-stat{
    padding:18px;border:1px solid var(--line);border-radius:20px;background:#fbfdfc;
  }
  .side-stat + .side-stat{margin-top:12px}
  .side-stat .label{
    font-size:12px;text-transform:uppercase;letter-spacing:.08em;font-weight:800;color:var(--muted);
  }
  .side-stat .value{
    margin-top:8px;font-size:30px;font-weight:900;letter-spacing:-.04em;color:var(--brand-dark);
  }
  .side-stat .text{margin-top:8px;color:var(--muted);line-height:1.5}
  .access-bar{
    display:grid;grid-template-columns:1fr 1fr;gap:0;margin-bottom:20px;overflow:hidden;
  }
  .access-pane{
    padding:24px 26px;position:relative;
  }
  .access-pane + .access-pane{border-left:1px solid var(--line)}
  .pill{
    display:inline-flex;align-items:center;padding:8px 12px;border-radius:999px;
    background:var(--brand-soft);color:var(--brand-dark);font-size:12px;
    font-weight:800;letter-spacing:.06em;text-transform:uppercase;margin-bottom:12px;
  }
  .access-pane h2{margin:0 0 12px;font-size:32px;letter-spacing:-.03em}
  .hours-chip{
    display:inline-block;padding:12px 14px;border-radius:16px;border:1px solid var(--line);
    background:#fbfdfc;margin-right:8px;margin-bottom:8px;font-size:15px;line-height:1.4;
  }
  .hours-chip strong{color:var(--brand-dark)}
  .access-pane p{margin:10px 0 0;color:var(--muted);line-height:1.5}
  .layout{
    display:grid;grid-template-columns:290px 1fr;gap:20px;align-items:start;
  }
  .filters{
    padding:18px;position:sticky;top:18px;
  }
  .filters h3{margin:0 0 12px;font-size:22px;letter-spacing:-.03em}
  .filter-stack{display:grid;gap:10px}
  .filter-btn{
    border:1px solid var(--line);background:#fff;color:var(--brand-dark);padding:14px 14px;
    border-radius:18px;text-align:left;font-weight:800;cursor:pointer;
  }
  .filter-btn.active{background:var(--brand-dark);border-color:var(--brand-dark);color:#fff}
  .filter-btn .small{
    display:block;margin-top:4px;font-weight:600;font-size:13px;opacity:.78;
  }
  .summary-box{
    margin-top:16px;padding:16px;border-radius:18px;background:#f8fcfa;border:1px dashed #c7dcd6;
    color:var(--muted);line-height:1.55;font-size:14px;
  }
  .content{display:grid;gap:18px}
  .section-card{padding:22px}
  .section-head{
    display:flex;justify-content:space-between;gap:18px;align-items:end;margin-bottom:16px;
  }
  .section-head h2{margin:0;font-size:34px;letter-spacing:-.04em}
  .section-head p{margin:0;color:var(--muted);line-height:1.5;max-width:760px}
  .membership-grid,.pack-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
  .group-card{
    border:1px solid var(--line);border-radius:24px;padding:20px;background:#fbfdfc;
  }
  .group-head{
    display:flex;justify-content:space-between;gap:14px;align-items:flex-start;margin-bottom:14px;
  }
  .group-head h3{margin:0 0 6px;font-size:28px;letter-spacing:-.03em}
  .group-head p{margin:0;color:var(--muted);line-height:1.5}
  .subtag{
    padding:8px 11px;border-radius:999px;background:var(--brand-soft);color:var(--brand-dark);
    font-size:12px;font-weight:800;text-transform:uppercase;letter-spacing:.06em;
  }
  .plan{
    border:1px solid var(--line);border-radius:22px;padding:18px;background:#fff;
  }
  .plan + .plan{margin-top:12px}
  .plan-top{display:flex;justify-content:space-between;gap:14px;align-items:flex-start;margin-bottom:12px}
  .plan h4{margin:0 0 6px;font-size:24px;letter-spacing:-.03em}
  .micro{color:var(--muted);font-size:14px;font-weight:600}
  .price{text-align:right}
  .price .main{font-size:30px;font-weight:900;letter-spacing:-.04em;line-height:1}
  .price .sub{margin-top:5px;font-size:12px;color:var(--muted)}
  .features{list-style:none;margin:0;padding:0;display:grid;gap:9px}
  .features li{position:relative;padding-left:26px;line-height:1.5}
  .features li:before{
    content:"✓";position:absolute;left:0;top:0;color:var(--brand-dark);font-weight:900;
  }
  .cta-row{display:flex;gap:10px;flex-wrap:wrap;margin-top:14px}
  .btn{
    display:inline-block;text-decoration:none;padding:11px 14px;border-radius:14px;font-weight:800;
    font-size:14px;background:var(--brand-dark);color:#fff;
  }
  .btn.secondary{background:#fff;color:var(--brand-dark);border:1px solid var(--line)}
  .pack-card{padding:20px}
  .pack-card h3{margin:0 0 6px;font-size:28px;letter-spacing:-.03em}
  .pack-card p{margin:0 0 14px;color:var(--muted);line-height:1.5}
  .pack-option{
    display:flex;justify-content:space-between;gap:14px;align-items:center;padding:16px;border:1px solid var(--line);
    border-radius:18px;background:#fbfdfc;
  }
  .pack-option + .pack-option{margin-top:12px}
  .pack-option strong{display:block;margin-bottom:4px}
  .pack-option span{color:var(--muted);font-size:14px;line-height:1.45}
  .pack-price{text-align:right}
  .pack-price .main{font-size:26px;font-weight:900;letter-spacing:-.03em}
  .pack-price .sub{font-size:12px;color:var(--muted);margin-top:4px}
  .hours-grid{display:grid;grid-template-columns:1fr 1fr;gap:18px}
  .hours-card{padding:18px}
  .hours-card h4{margin:0 0 10px;font-size:22px;letter-spacing:-.03em}
  .hours-line{
    padding:12px 14px;border-radius:16px;border:1px solid var(--line);background:#fbfdfc;line-height:1.45;
  }
  .hours-line + .hours-line{margin-top:8px}
  .hours-line strong{color:var(--brand-dark)}
  .hidden{display:none !important}
</style>
</head>
<body>
<div class="wrap">
  <section class="hero">
    <div class="hero-main">
      <div class="eyebrow">Desktop mockup</div>
      <h1>Desktop should help people compare, not just scroll.</h1>
      <div class="sub">
        This version uses a left filter rail, wider comparison blocks, and clearer side-by-side scanning.
        It is built to make your subscription ladder obvious while still keeping packs visible and easy to reach.
      </div>
    </div>
    <div class="hero-side">
      <div class="side-stat">
        <div class="label">Memberships from</div>
        <div class="value">$15/week</div>
        <div class="text">Best for regular use. Marketed weekly, billed monthly.</div>
      </div>
      <div class="side-stat">
        <div class="label">Packs from</div>
        <div class="value">$190</div>
        <div class="text">Best for flexibility with no ongoing subscription.</div>
      </div>
    </div>
  </section>

  <section class="access-bar">
    <div class="access-pane">
      <div class="pill">Access Type</div>
      <h2>Off Peak Access</h2>
      <div class="hours-chip"><strong>Weekdays</strong> 9am–5pm</div>
      <div class="hours-chip"><strong>Weekends</strong> 5am–9am</div>
      <p>From $15/week on memberships, or from $190 on packs.</p>
    </div>
    <div class="access-pane">
      <div class="pill">Access Type</div>
      <h2>Anytime Access</h2>
      <div class="hours-chip"><strong>7 days a week</strong> 5am–9pm</div>
      <p>From $20/week on memberships, or from $240 on packs.</p>
    </div>
  </section>

  <div class="layout">
    <aside class="filters">
      <h3>Filter pricing</h3>
      <div class="filter-stack">
        <button class="filter-btn active" data-filter="all">Show all<span class="small">See every option together</span></button>
        <button class="filter-btn" data-filter="memberships">Memberships<span class="small">Weekly + Unlimited</span></button>
        <button class="filter-btn" data-filter="packs">Packs<span class="small">10 Visit + 20 Visit</span></button>
        <button class="filter-btn" data-filter="offpeak">Off Peak<span class="small">Lower entry price</span></button>
        <button class="filter-btn" data-filter="anytime">Anytime<span class="small">Full access</span></button>
      </div>
      <div class="summary-box">
        <strong>How I’d use this on desktop:</strong> keep this rail visible while the main content scrolls, so customers can quickly narrow the page without losing context.
      </div>
    </aside>

    <main class="content">
      <section class="section-card" id="memberships" data-kind="memberships">
        <div class="section-head">
          <div>
            <h2>Memberships</h2>
            <p>Lead the page with memberships. Weekly plans sell the stacking benefit. Unlimited plans sell daily access and routine.</p>
          </div>
        </div>

        <div class="membership-grid">
          <div class="group-card">
            <div class="group-head">
              <div>
                <h3>Weekly</h3>
                <p>For lighter, flexible routine use with visits that stack through the month.</p>
              </div>
              <div class="subtag">1 visit added each week</div>
            </div>

            <div class="plan" data-access="offpeak">
              <div class="plan-top">
                <div>
                  <h4>Off Peak Weekly</h4>
                  <div class="micro">Off Peak access</div>
                </div>
                <div class="price">
                  <div class="main">$15/week</div>
                  <div class="sub">billed monthly</div>
                </div>
              </div>
              <ul class="features">
                <li>1 Off Peak visit added each week</li>
                <li>If you don’t use a visit one week, it carries over and stacks onto the next</li>
                <li>Build up to 4–5 visits across the month, depending on the calendar</li>
              </ul>
              <div class="cta-row">
                <a href="#" class="btn">Choose Off Peak Weekly</a>
                <a href="#hours" class="btn secondary">See access hours</a>
              </div>
            </div>

            <div class="plan" data-access="anytime">
              <div class="plan-top">
                <div>
                  <h4>Anytime Weekly</h4>
                  <div class="micro">Anytime access</div>
                </div>
                <div class="price">
                  <div class="main">$20/week</div>
                  <div class="sub">billed monthly</div>
                </div>
              </div>
              <ul class="features">
                <li>1 visit added each week to use at any available session</li>
                <li>If you don’t use a visit one week, it carries over and stacks onto the next</li>
                <li>Build up to 4–5 visits across the month, depending on the calendar</li>
              </ul>
              <div class="cta-row">
                <a href="#" class="btn">Choose Anytime Weekly</a>
                <a href="#hours" class="btn secondary">See access hours</a>
              </div>
            </div>
          </div>

          <div class="group-card">
            <div class="group-head">
              <div>
                <h3>Unlimited</h3>
                <p>For regular users who want simple daily access and full routine value.</p>
              </div>
              <div class="subtag">Daily access</div>
            </div>

            <div class="plan" data-access="offpeak">
              <div class="plan-top">
                <div>
                  <h4>Off Peak Unlimited</h4>
                  <div class="micro">Off Peak access</div>
                </div>
                <div class="price">
                  <div class="main">$30/week</div>
                  <div class="sub">billed monthly</div>
                </div>
              </div>
              <ul class="features">
                <li>Enjoy daily Off Peak access</li>
                <li>Perfect for building a regular wellness routine</li>
                <li>Book into Off Peak sessions throughout the month</li>
              </ul>
              <div class="cta-row">
                <a href="#" class="btn">Choose Off Peak Unlimited</a>
                <a href="#hours" class="btn secondary">See access hours</a>
              </div>
            </div>

            <div class="plan" data-access="anytime">
              <div class="plan-top">
                <div>
                  <h4>Anytime Unlimited</h4>
                  <div class="micro">Anytime access</div>
                </div>
                <div class="price">
                  <div class="main">$40/week</div>
                  <div class="sub">billed monthly</div>
                </div>
              </div>
              <ul class="features">
                <li>Enjoy daily access to any available session</li>
                <li>Our most flexible option for regular use</li>
                <li>Book into sessions across the month with full flexibility</li>
              </ul>
              <div class="cta-row">
                <a href="#" class="btn">Choose Anytime Unlimited</a>
                <a href="#hours" class="btn secondary">See access hours</a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="section-card" id="packs" data-kind="packs">
        <div class="section-head">
          <div>
            <h2>Packs</h2>
            <p>Still visible and still easy to compare, but positioned underneath memberships so the main focus stays on subscriptions.</p>
          </div>
        </div>

        <div class="pack-grid">
          <div class="pack-card">
            <h3>10 Visit Packs</h3>
            <p>A flexible prepaid option for customers who do not want an ongoing membership.</p>
            <div class="pack-option" data-access="offpeak">
              <div>
                <strong>Off Peak 10 Visit Pack</strong>
                <span>10 Off Peak visits. Expires 6 months from purchase.</span>
              </div>
              <div class="pack-price">
                <div class="main">$190</div>
                <div class="sub">one-off payment</div>
              </div>
            </div>
            <div class="pack-option" data-access="anytime">
              <div>
                <strong>Anytime 10 Visit Pack</strong>
                <span>10 visits at any available session. Expires 6 months from purchase.</span>
              </div>
              <div class="pack-price">
                <div class="main">$240</div>
                <div class="sub">one-off payment</div>
              </div>
            </div>
          </div>

          <div class="pack-card">
            <h3>20 Visit Packs</h3>
            <p>Better value for customers who want more visits without moving to a membership.</p>
            <div class="pack-option" data-access="offpeak">
              <div>
                <strong>Off Peak 20 Visit Pack</strong>
                <span>20 Off Peak visits. Expires 6 months from purchase.</span>
              </div>
              <div class="pack-price">
                <div class="main">$280</div>
                <div class="sub">one-off payment</div>
              </div>
            </div>
            <div class="pack-option" data-access="anytime">
              <div>
                <strong>Anytime 20 Visit Pack</strong>
                <span>20 visits at any available session. Expires 6 months from purchase.</span>
              </div>
              <div class="pack-price">
                <div class="main">$380</div>
                <div class="sub">one-off payment</div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section class="section-card" id="hours">
        <div class="section-head">
          <div>
            <h2>Access hours</h2>
            <p>Shown once here for clarity, rather than repeated inside every card.</p>
          </div>
        </div>
        <div class="hours-grid">
          <div class="hours-card">
            <h4>Off Peak Access</h4>
            <div class="hours-line"><strong>Weekdays</strong> 9am–5pm</div>
            <div class="hours-line"><strong>Weekends</strong> 5am–9am</div>
          </div>
          <div class="hours-card">
            <h4>Anytime Access</h4>
            <div class="hours-line"><strong>7 days a week</strong> 5am–9pm</div>
          </div>
        </div>
      </section>
    </main>
  </div>
</div>

<script>
  const buttons = document.querySelectorAll('.filter-btn');
  const membershipSection = document.getElementById('memberships');
  const packSection = document.getElementById('packs');
  const accessItems = document.querySelectorAll('[data-access]');

  function setActive(filter){
    buttons.forEach(btn => btn.classList.toggle('active', btn.dataset.filter === filter));
  }

  function applyFilter(filter){
    setActive(filter);

    if(filter === 'all'){
      membershipSection.classList.remove('hidden');
      packSection.classList.remove('hidden');
      accessItems.forEach(el => el.classList.remove('hidden'));
      return;
    }
    if(filter === 'memberships'){
      membershipSection.classList.remove('hidden');
      packSection.classList.add('hidden');
      accessItems.forEach(el => el.classList.remove('hidden'));
      return;
    }
    if(filter === 'packs'){
      membershipSection.classList.add('hidden');
      packSection.classList.remove('hidden');
      accessItems.forEach(el => el.classList.remove('hidden'));
      return;
    }
    membershipSection.classList.remove('hidden');
    packSection.classList.remove('hidden');
    accessItems.forEach(el => el.classList.toggle('hidden', el.dataset.access !== filter));
  }

  buttons.forEach(btn => btn.addEventListener('click', () => applyFilter(btn.dataset.filter)));
  applyFilter('all');
</script>
</body>
</html>
