<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Movie Mate</title>
<style>
  :root { --bg:#0b0f14; --card:#121821; --text:#eef2f7; --muted:#a7b1c2; --accent:#e50914; }
  *{box-sizing:border-box}
  body{margin:0;font-family:Inter,system-ui,Arial;background:radial-gradient(1200px 600px at 80% -10%,#1b2330 0%,#0b0f14 60%);color:var(--text);display:grid;place-items:center;min-height:100vh}
  .card{background:rgba(18,24,33,.85);backdrop-filter:blur(10px);border:1px solid #1f2733;border-radius:18px;padding:28px;width:100%;max-width:380px}
  h1{margin:0 0 6px;font-size:26px}
  .muted{color:var(--muted);font-size:14px;margin-bottom:18px}
  input{width:100%;padding:12px 14px;border-radius:12px;border:1px solid #263142;background:#0f1520;color:var(--text);margin-top:10px}
  button{width:100%;padding:12px 14px;border-radius:12px;border:0;background:var(--accent);color:#fff;font-weight:800;margin-top:14px;cursor:pointer}
  .brand{display:flex;align-items:center;gap:10px;margin-bottom:10px;font-weight:900}
  .logo{width:28px;height:28px;border-radius:8px;background:var(--accent)}
</style>
</head>
<body>
  <form class="card" id="signupForm">
    <div class="brand"><div class="logo"></div> Movie Mate</div>
    <h1>Create your account</h1>
    <p class="muted">Free. No credit card. Start watching now.</p>
    <input id="name" type="text" placeholder="Full Name" required>
    <input id="email" type="email" placeholder="Email" required>
    <input id="pass" type="password" placeholder="Password" required minlength="6">
    <button type="submit">Sign Up & Continue</button>
  </form>

<script>
document.getElementById('signupForm').addEventListener('submit', e=>{
  e.preventDefault();
  const user = {
    name: document.getElementById('name').value,
    email: document.getElementById('email').value,
  };
  localStorage.setItem('moviemate_user', JSON.stringify(user));
  window.location.href = 'index.html';
});
</script>
</body>
</html>mU
