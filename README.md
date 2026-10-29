<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Nana Gamming | Play Beyond</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Orbitron:wght@400;500;600;700;800&family=Rajdhani:wght@400;500;600;700&display=swap');
:root{--cyan:#00f5ff;--pink:#ff31d2;--purple:#8a42ff;--ink:#050611;--glass:rgba(14,18,48,.48);--line:rgba(113,223,255,.32)}
*{box-sizing:border-box}html{scroll-behavior:smooth}body{margin:0;min-height:100vh;color:#f5f7ff;font-family:'Rajdhani',sans-serif;font-size:18px;background:#050611;overflow-x:hidden}
body:before{content:"";position:fixed;inset:0;z-index:-3;background:linear-gradient(120deg,rgba(3,5,20,.82),rgba(18,5,46,.55),rgba(2,15,36,.82)),url('https://images.unsplash.com/photo-1542751371-adc38448a05e?auto=format&fit=crop&w=2200&q=85') center/cover}
body:after{content:"";position:fixed;inset:0;z-index:-2;pointer-events:none;background:radial-gradient(ellipse at 15% 20%,rgba(0,245,255,.16),transparent 35%),radial-gradient(ellipse at 85% 25%,rgba(255,49,210,.17),transparent 32%),radial-gradient(ellipse at 55% 95%,rgba(138,66,255,.18),transparent 40%)}
button,input,select,textarea{font:inherit}button{cursor:pointer;color:white}.hidden{display:none!important}
.glass{background:linear-gradient(135deg,rgba(255,255,255,.13),rgba(255,255,255,.025) 45%,rgba(0,245,255,.055));border:1px solid rgba(255,255,255,.2);box-shadow:inset 0 1px 0 rgba(255,255,255,.18),0 18px 55px rgba(0,0,0,.35),0 0 25px rgba(0,245,255,.09);backdrop-filter:blur(24px) saturate(160%);-webkit-backdrop-filter:blur(24px) saturate(160%);border-radius:22px}
.neon{color:var(--cyan);text-shadow:0 0 8px rgba(0,245,255,.9),0 0 25px rgba(0,245,255,.4)}
.logo{font-family:Orbitron,sans-serif;font-weight:800;letter-spacing:1px;line-height:1.05;color:white;text-shadow:0 0 8px var(--cyan),0 0 18px var(--purple),2px 2px 0 var(--pink)}
.logo span{display:block;color:var(--pink);font-size:.55em;letter-spacing:5px;margin-top:5px}
.console-btn{border:1px solid rgba(0,245,255,.75);border-radius:14px;padding:12px 19px;background:linear-gradient(145deg,rgba(0,245,255,.26),rgba(79,20,151,.6) 55%,rgba(255,49,210,.2));box-shadow:0 5px 0 #20204d,0 8px 20px rgba(0,0,0,.4),inset 0 1px 1px rgba(255,255,255,.5),0 0 18px rgba(0,245,255,.22);font-family:Orbitron,sans-serif;font-size:12px;letter-spacing:.5px;transition:.18s;position:relative;top:0}
.console-btn:hover{transform:translateY(-3px);box-shadow:0 8px 0 #20204d,0 13px 24px rgba(0,0,0,.4),0 0 25px rgba(0,245,255,.55)}.console-btn:active{top:4px;transform:translateY(1px);box-shadow:0 1px 0 #20204d,0 3px 8px #000}
.secondary{border-color:rgba(255,49,210,.65);background:linear-gradient(145deg,rgba(255,49,210,.22),rgba(54,19,100,.7))}
input,select,textarea{width:100%;color:#fff;background:rgba(0,0,0,.68);border:1px solid rgba(0,245,255,.35);border-radius:12px;padding:12px 14px;outline:none;box-shadow:inset 0 2px 10px #0008}
input:focus,select:focus,textarea:focus{border-color:var(--cyan);box-shadow:0 0 0 2px #00f5ff25,0 0 18px #00f5ff22}
label{display:block;font-size:15px;color:#cbd7ff;margin:12px 0 6px}
#loginScreen{min-height:100vh;display:grid;place-items:center;padding:28px 16px}
.login-layout{width:min(1050px,100%);display:grid;grid-template-columns:1.1fr .9fr;gap:26px;align-items:center}
.hero{padding:30px 20px;text-align:center}.hero .logo{font-size:clamp(42px,7vw,82px)}.hero p{font-size:22px;color:#d9e7ff}.hero-art{font-size:clamp(80px,15vw,170px);filter:drop-shadow(0 0 24px #00eaff);margin:12px 0}
.login-card{padding:30px;max-width:470px;width:100%;justify-self:center}.login-card h2{text-align:center;font-family:Orbitron,sans-serif;font-size:22px}.gender-row{display:grid;grid-template-columns:1fr 1fr;gap:10px}.gender-choice{display:flex;align-items:center;justify-content:center;gap:8px;border:1px solid #8b80ff77;border-radius:12px;padding:10px;background:#080b20;cursor:pointer}.gender-choice input{width:auto;accent-color:var(--pink)}.full{width:100%;margin-top:18px}.hint{font-size:14px;color:#aebcde;line-height:1.4}.error{color:#ff8bdc;min-height:22px;font-size:15px}
#app{min-height:100vh}.topbar{position:sticky;top:0;z-index:10;display:flex;align-items:center;justify-content:space-between;gap:18px;padding:14px clamp(14px,4vw,48px);border-radius:0 0 22px 22px;background:rgba(4,7,24,.77);border:1px solid #8f7cff35;backdrop-filter:blur(24px)}
.topbar .logo{font-size:24px;white-space:nowrap}.nav{display:flex;gap:9px;flex-wrap:wrap;justify-content:center}.nav button{padding:10px 13px;border:1px solid transparent;border-radius:12px;background:rgba(20,21,57,.65);font-family:Orbitron,sans-serif;font-size:10px}.nav button:hover,.nav button.active{border-color:var(--cyan);box-shadow:0 0 18px #00f5ff35;color:var(--cyan)}
.avatar{width:42px;height:42px;border-radius:50%;border:1px solid var(--pink);background:linear-gradient(135deg,#17225a,#691d91);font-size:22px;box-shadow:0 0 18px #ff31d255}
main{width:min(1250px,94%);margin:28px auto 60px}.welcome{padding:clamp(22px,4vw,42px);display:flex;justify-content:space-between;align-items:center;gap:20px;min-height:205px;background:linear-gradient(100deg,rgba(5,9,30,.86),rgba(33,13,75,.5)),url('https://images.unsplash.com/photo-1511512578047-dfb367046420?auto=format&fit=crop&w=1500&q=80') center/cover}
.welcome h1{font-family:Orbitron,sans-serif;font-size:clamp(24px,4vw,42px);margin:8px 0}.welcome p{color:#d3defb;font-size:20px}.welcome-icon{font-size:clamp(60px,10vw,110px);filter:drop-shadow(0 0 20px var(--cyan))}
.quick-grid{display:grid;grid-template-columns:repeat(4,1fr);gap:16px;margin:20px 0}.quick{padding:22px 12px;text-align:center;cursor:pointer;transition:.2s}.quick:hover{transform:translateY(-5px);border-color:var(--pink);box-shadow:0 0 28px #ff31d233}.quick .emoji{font-size:38px;display:block;margin-bottom:8px;filter:drop-shadow(0 0 8px #00f5ff)}.quick strong{font-family:Orbitron,sans-serif;font-size:12px}
.section{padding:24px;margin:20px 0}.section-head{display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap}.section h2{font-family:Orbitron,sans-serif;font-size:19px;margin:0 0 16px}.search{max-width:440px;position:relative}.search input{background:#03040a;border:1px solid #363b56;color:white;border-radius:14px;padding-left:42px}.search:before{content:'⌕';position:absolute;left:15px;top:4px;font-size:28px;color:var(--cyan)}
.game-grid{display:grid;grid-template-columns:repeat(4,minmax(0,1fr));gap:15px}.game-card{overflow:hidden;border-radius:17px;background:rgba(4,7,24,.85);border:1px solid #8b83e855;box-shadow:0 10px 25px #0005;transition:.2s}.game-card:hover{transform:translateY(-4px);border-color:var(--cyan);box-shadow:0 0 22px #00f5ff22}.game-cover{height:125px;display:grid;place-items:center;font-size:50px;background:radial-gradient(circle at 50% 30%,#5144ac,#10182e 65%,#070914);border-bottom:1px solid #8b83e844}.game-cover img{width:100%;height:100%;object-fit:cover}.game-info{padding:12px}.game-info h3{font-size:18px;margin:0 0 5px}.game-info p{font-size:14px;color:#aab9db;margin:0 0 12px}.game-info button{width:100%;padding:9px 6px;font-size:10px}
.owner-tag{font-size:12px;color:var(--cyan);border:1px solid #00f5ff55;border-radius:99px;padding:5px 9px}
.profile-grid,.add-grid{display:grid;grid-template-columns:1fr 1.3fr;gap:20px}.profile-card{text-align:center;padding:25px}.profile-icon{font-size:75px}.profile-card h2{margin-bottom:5px}.profile-details{padding:25px}.detail-line{display:flex;justify-content:space-between;gap:12px;padding:12px 0;border-bottom:1px solid #ffffff16}
textarea{min-height:165px;resize:vertical;font-family:Consolas,monospace;font-size:14px}.small-note{font-size:14px;color:#aab9d9;line-height:1.5}.owner-only{border-color:#ff31d255}.empty{padding:30px;text-align:center;color:#aab9d9;border:1px dashed #8a85bc66;border-radius:16px}
#playerModal{position:fixed;inset:0;z-index:30;background:#02030de8;display:grid;place-items:center;padding:18px}.player-box{width:min(1100px,100%);height:min(82vh,760px);display:flex;flex-direction:column;padding:15px}.player-top{display:flex;align-items:center;justify-content:space-between;gap:12px;padding-bottom:12px}.player-frame{flex:1;width:100%;background:#000;border:1px solid #00f5ff77;border-radius:12px}.player-close{font-size:22px;padding:6px 13px}.toast{position:fixed;right:18px;bottom:18px;z-index:50;max-width:330px;padding:14px 18px;background:#090d26;border:1px solid var(--cyan);border-radius:14px;box-shadow:0 0 22px #00f5ff33}
footer{text-align:center;color:#9daed7;padding:25px;font-size:14px}
@media(max-width:800px){.login-layout{grid-template-columns:1fr}.hero{padding:12px}.hero-art{margin:0}.login-card{max-width:560px}.topbar{flex-wrap:wrap}.topbar .logo{font-size:20px}.nav{order:3;width:100%}.quick-grid{grid-template-columns:repeat(2,1fr)}.game-grid{grid-template-columns:repeat(2,minmax(0,1fr))}.profile-grid,.add-grid{grid-template-columns:1fr}.welcome-icon{display:none}}
@media(max-width:420px){.game-grid{grid-template-columns:1fr 1fr;gap:9px}.game-cover{height:95px}.section{padding:15px}.login-card{padding:22px}}
</style>
</head>
<body>
<section id="loginScreen">
  <div class="login-layout">
    <div class="hero">
      <div class="logo">NANA<span>GAMMING</span></div>
      <div class="hero-art">🎮</div>
      <p class="neon">PLAY · EXPLORE · ENJOY</p>
      <p class="hint">Your world. Your games. Your rules.</p>
    </div>
    <form class="login-card glass" id="accountForm">
      <h2>ENTER THE <span class="neon">GAME ZONE</span></h2>
      <p class="hint" id="formIntro">Create your player account to start.</p>
      <label for="username">Username</label><input id="username" required minlength="3" maxlength="24" autocomplete="username" placeholder="Choose a gamer name">
      <label for="password">Create password</label><input id="password" required minlength="6" type="password" autocomplete="new-password" placeholder="At least 6 characters">
      <label>Gender</label>
      <div class="gender-row">
        <label class="gender-choice"><input type="radio" name="gender" value="Male" required> ♂ Male</label>
        <label class="gender-choice"><input type="radio" name="gender" value="Female" required> ♀ Female</label>
      </div>
      <button class="console-btn full" type="submit">🎮 &nbsp; CREATE ACCOUNT / LOGIN &nbsp; 🎮</button>
      <div class="error" id="loginError" role="status"></div>
      <p class="hint">Demo note: this single-file version stores account data only in this browser. Do not use a real or reused password.</p>
    </form>
  </div>
</section>

<div id="app" class="hidden">
<header class="topbar">
  <div class="logo">NANA<span>GAMMING</span></div>
  <nav class="nav" aria-label="Main navigation">
    <button class="active" data-page="home">⌂ HOME</button>
    <button data-page="explore">🎮 EXPLORE GAMES</button>
    <button data-page="profile">👤 YOUR PROFILE</button>
    <button data-page="add">＋ ADD GAME</button>
  </nav>
  <button class="avatar" title="Your profile" data-goto="profile">👤</button>
</header>

<main>
  <section id="page-home" class="page">
    <div class="welcome glass">
      <div><span class="neon">WELCOME BACK, PLAYER</span><h1>READY TO <span class="neon">PLAY?</span></h1><p>Power up your next adventure.</p><button class="console-btn" data-goto="explore">EXPLORE GAMES ↗</button></div>
      <div class="welcome-icon">👾</div>
    </div>
    <div class="quick-grid">
      <div class="quick glass" data-goto="explore"><span class="emoji">🎮</span><strong>EXPLORE GAMES</strong></div>
      <div class="quick glass" data-goto="profile"><span class="emoji">🧑‍🚀</span><strong>YOUR PROFILE</strong></div>
      <div class="quick glass" data-goto="add"><span class="emoji">➕</span><strong>ADD A GAME</strong></div>
      <div class="quick glass" data-goto="mygames"><span class="emoji">🕹️</span><strong>MY GAMES</strong></div>
    </div>
    <section class="section glass">
      <div class="section-head"><h2>⚡ FEATURED GAMES</h2><button class="console-btn" data-goto="explore">VIEW ALL</button></div>
      <div id="featuredGrid" class="game-grid"></div>
    </section>
  </section>

  <section id="page-explore" class="page hidden">
    <section class="section glass">
      <div class="section-head"><h2>🎮 EXPLORE GAMES</h2><div class="search"><input id="gameSearch" type="search" placeholder="Search games..." aria-label="Search games"></div></div>
      <p class="hint">Search your saved games. Select Play to open a compatible HTML game or supported game URL.</p>
      <div id="exploreGrid" class="game-grid"></div>
    </section>
  </section>

  <section id="page-mygames" class="page hidden">
    <section class="section glass"><div class="section-head"><h2>🕹️ MY GAMES</h2><button class="console-btn" data-goto="add">＋ ADD GAME</button></div><div id="myGamesGrid" class="game-grid"></div></section>
  </section>

  <section id="page-profile" class="page hidden">
    <div class="profile-grid">
      <div class="profile-card glass"><div class="profile-icon">🧑‍🚀</div><h2 id="profileName">Player</h2><p class="neon">NANA GAMMING PLAYER</p><span class="owner-tag" id="roleBadge">PLAYER</span></div>
      <div class="profile-details glass"><h2>YOUR PROFILE</h2><div class="detail-line"><span>Username</span><strong id="profileUsername">—</strong></div><div class="detail-line"><span>Gender</span><strong id="profileGender">—</strong></div><div class="detail-line"><span>Account role</span><strong id="profileRole">Player</strong></div><div class="detail-line"><span>Games added</span><strong id="profileGameCount">0</strong></div><button class="console-btn secondary" id="logoutBtn">LOG OUT</button></div>
    </div>
  </section>

  <section id="page-add" class="page hidden">
    <div class="add-grid">
      <section class="section glass owner-only">
        <div class="section-head"><h2>＋ ADD A GAME</h2><span class="owner-tag" id="ownerStatus">OWNER ONLY</span></div>
        <p class="hint">Paste a game's HTML code or a URL to a playable web game. Compatible games can open in the game viewer.</p>
        <form id="addGameForm">
          <label for="gameTitle">Game name</label><input id="gameTitle" maxlength="60" placeholder="e.g. My Arcade Game" required>
          <label for="gameUrl">Game URL (optional if using HTML)</label><input id="gameUrl" type="url" placeholder="https://example.com/playable-game">
          <label for="gameHtml">Or paste HTML code</label><textarea id="gameHtml" placeholder="Paste a complete HTML game here..."></textarea>
          <label for="gameCategory">Category</label><select id="gameCategory"><option>Arcade</option><option>Action</option><option>Adventure</option><option>Racing</option><option>Sports</option><option>Puzzle</option><option>Other</option></select>
          <button class="console-btn full" type="submit">🚀 SAVE GAME TO LIBRARY</button>
          <p class="small-note">Only one source is needed: a URL or HTML. Only add games you own or are authorized to use. Many commercial games block embedding and cannot be converted from a link.</p>
        </form>
      </section>
      <section class="section glass">
        <h2>🔒 GAME CONTROL</h2>
        <p class="hint">In this demo, the first account created in this browser becomes the owner. Other accounts in the same browser can browse and play saved games but cannot add or remove them.</p>
        <div class="empty">💠 OWNER ACCESS<br><br>Manage your game library from this panel.</div>
        <h2 style="margin-top:24px">🧩 HOW IT WORKS</h2>
        <p class="small-note">• HTML games are loaded in a sandboxed frame.<br>• URLs are opened in an embedded viewer when the site permits it.<br>• Some websites prevent embedding; use their official Play page instead.<br>• This browser-only owner lock is not secure against technical users and does not sync across devices. A public website needs server-side accounts and permissions.</p>
      </section>
    </div>
  </section>
</main>
<footer>✦ NANA GAMMING · YOUR WORLD · YOUR GAMES · YOUR RULES ✦</footer>
</div>

<div id="playerModal" class="hidden" role="dialog" aria-modal="true" aria-label="Game player">
  <div class="player-box glass"><div class="player-top"><div><strong class="neon" id="playerTitle">NOW PLAYING</strong><div class="hint">If the game does not load, its host may block embedding.</div></div><button class="console-btn secondary player-close" id="closePlayer">✕ CLOSE</button></div><iframe class="player-frame" id="gameFrame" title="Game player" sandbox="allow-scripts allow-forms allow-pointer-lock allow-downloads" allow="fullscreen; gamepad; autoplay"></iframe></div>
</div>
<div id="toast" class="toast hidden" role="status"></div>

<script>
(() => {
 const $ = id => document.getElementById(id);
 const USERS_KEY='nanaGammingUsers_v1', OWNER_KEY='nanaGammingOwner_v1', GAMES_KEY='nanaGammingGames_v1', SESSION_KEY='nanaGammingSession_v1';
 let users=read(USERS_KEY,[]), games=read(GAMES_KEY,[]), current=null;
 const demoGames=[
  {id:'demo-1',title:'Neon Space Run',category:'Arcade',emoji:'🚀',description:'A glowing arcade adventure.',demo:true},
  {id:'demo-2',title:'Cyber Racer',category:'Racing',emoji:'🏎️',description:'Race through a neon city.',demo:true},
  {id:'demo-3',title:'Pixel Quest',category:'Adventure',emoji:'🗡️',description:'Explore a pixel world.',demo:true},
  {id:'demo-4',title:'Cosmic Blocks',category:'Puzzle',emoji:'🧩',description:'A quick puzzle challenge.',demo:true}
 ];
 function read(key,fallback){try{return JSON.parse(localStorage.getItem(key)) ?? fallback}catch{return fallback}}
 function save(){localStorage.setItem(USERS_KEY,JSON.stringify(users));localStorage.setItem(GAMES_KEY,JSON.stringify(games))}
 function toast(message){$('toast').textContent=message;$('toast').classList.remove('hidden');setTimeout(()=>$('toast').classList.add('hidden'),3200)}
 function isOwner(){return !!current && current.username===localStorage.getItem(OWNER_KEY)}
 function allGames(){return [...demoGames,...games]}
 function showLogin(){ $('loginScreen').classList.remove('hidden');$('app').classList.add('hidden'); }
 function showApp(){ $('loginScreen').classList.add('hidden');$('app').classList.remove('hidden');updateProfile();renderGames();go('home'); }
 function go(page){
  document.querySelectorAll('.page').forEach(p=>p.classList.add('hidden'));
  const target=$('page-'+page);if(target)target.classList.remove('hidden');else $('page-home').classList.remove('hidden');
  document.querySelectorAll('.nav button').forEach(b=>b.classList.toggle('active',b.dataset.page===page));
  if(page==='add'){$('ownerStatus').textContent=isOwner()?'OWNER ACCESS':'VIEW ONLY';$('addGameForm').querySelectorAll('input,textarea,select,button').forEach(el=>el.disabled=!isOwner());}
 }
 function updateProfile(){
  $('profileName').textContent=current.username;$('profileUsername').textContent=current.username;$('profileGender').textContent=current.gender;
  $('profileRole').textContent=isOwner()?'Owner':'Player';$('roleBadge').textContent=isOwner()?'👑 OWNER':'PLAYER';$('profileGameCount').textContent=games.length;
 }
 function card(game){
  const el=document.createElement('article');el.className='game-card';
  const cover=document.createElement('div');cover.className='game-cover';cover.textContent=game.emoji||'🎮';el.appendChild(cover);
  const info=document.createElement('div');info.className='game-info';
  const title=document.createElement('h3');title.textContent=game.title;const desc=document.createElement('p');desc.textContent=game.category||'Game';
  const play=document.createElement('button');play.className='console-btn';play.textContent='▶ PLAY NOW';play.addEventListener('click',()=>playGame(game));
  info.append(title,desc,play);
  if(isOwner() && !game.demo){const remove=document.createElement('button');remove.className='console-btn secondary';remove.style.marginTop='7px';remove.textContent='REMOVE';remove.addEventListener('click',()=>{if(confirm('Remove '+game.title+' from your library?')){games=games.filter(g=>g.id!==game.id);save();renderGames();updateProfile();toast('Game removed.')}});info.appendChild(remove)}
  el.appendChild(info);return el;
 }
 function fillGrid(id,list){const grid=$(id);grid.replaceChildren();if(!list.length){const empty=document.createElement('div');empty.className='empty';empty.textContent='No games found yet. Owner can add games from the Add Game page.';grid.appendChild(empty);return}list.forEach(g=>grid.appendChild(card(g)))}
 function renderGames(){const list=allGames();fillGrid('featuredGrid',list.slice(0,4));fillGrid('exploreGrid',filtered());fillGrid('myGamesGrid',games)}
 function filtered(){const q=$('gameSearch').value.trim().toLowerCase();return allGames().filter(g=>(g.title+' '+(g.category||'')+' '+(g.description||'')).toLowerCase().includes(q))}
 function playGame(game){
  $('playerTitle').textContent='NOW PLAYING: '+game.title;
  const frame=$('gameFrame');frame.removeAttribute('src');frame.src='about:blank';
  if(game.html){frame.srcdoc=game.html}
  else if(game.url){frame.src=game.url}
  else {frame.srcdoc=`<!doctype html><html><head><meta name="viewport" content="width=device-width,initial-scale=1"><style>body{margin:0;background:radial-gradient(circle,#22235d,#050611);color:white;font-family:Arial;display:grid;place-items:center;height:100vh;text-align:center}button{padding:14px 24px;background:#111c4a;color:#00f5ff;border:1px solid #00f5ff;border-radius:12px;font-size:18px}h1{color:#ff31d2}p{color:#cbd7ff}</style></head><body><div><div style="font-size:70px">${game.emoji||'🎮'}</div><h1>${escapeHtml(game.title)}</h1><p>This is a demo library card, not the original commercial game.</p><button onclick="this.textContent='READY PLAYER ONE! 🎮'">START DEMO</button></div></body></html>`}
  $('playerModal').classList.remove('hidden');
 }
 function escapeHtml(s){return String(s).replace(/[&<>"']/g,c=>({'&':'&amp;','<':'&lt;','>':'&gt;','"':'&quot;',"'":'&#39;'}[c]))}
 document.querySelectorAll('[data-page]').forEach(b=>b.addEventListener('click',()=>go(b.dataset.page)));
 document.querySelectorAll('[data-goto]').forEach(b=>b.addEventListener('click',()=>go(b.dataset.goto)));
 $('gameSearch').addEventListener('input',()=>fillGrid('exploreGrid',filtered()));
 $('closePlayer').addEventListener('click',()=>{$('playerModal').classList.add('hidden');$('gameFrame').src='about:blank';$('gameFrame').srcdoc='';});
 $('playerModal').addEventListener('click',e=>{if(e.target===$('playerModal'))$('closePlayer').click()});
 $('accountForm').addEventListener('submit',e=>{
  e.preventDefault();const username=$('username').value.trim();const password=$('password').value;const gender=document.querySelector('input[name="gender"]:checked')?.value;
  $('loginError').textContent='';
  if(username.length<3||password.length<6||!gender){$('loginError').textContent='Enter a username, password (6+ characters), and select Male or Female.';return}
  let user=users.find(u=>u.username.toLowerCase()===username.toLowerCase());
  if(user){if(user.password!==password){$('loginError').textContent='That username already exists. Check the password or choose another username.';return}user.gender=gender}
  else {user={username,password,gender};users.push(user);if(!localStorage.getItem(OWNER_KEY))localStorage.setItem(OWNER_KEY,username)}
  current=user;localStorage.setItem(SESSION_KEY,username);save();showApp();
 });
 $('logoutBtn').addEventListener('click',()=>{current=null;localStorage.removeItem(SESSION_KEY);showLogin();toast('Logged out.')});
 $('addGameForm').addEventListener('submit',e=>{
  e.preventDefault();if(!isOwner()){toast('Only the owner can add games.');return}
  const title=$('gameTitle').value.trim(),url=$('gameUrl').value.trim(),html=$('gameHtml').value.trim();
  if(!title||(!url&&!html)){toast('Enter a game name and either a URL or HTML.');return}
  if(url&&!/^https?:\/\//i.test(url)){toast('Use a valid http:// or https:// URL.');return}
  if(html&&!/<html[\s>]|<!doctype html/i.test(html)){toast('Paste a complete HTML document for best results.');return}
  games.unshift({id:'game-'+Date.now(),title,url,html,category:$('gameCategory').value,emoji:'🎮',description:'Added to your library'});
  save();$('addGameForm').reset();renderGames();updateProfile();toast('Game added to Nana Gamming!');go('mygames');
 });
 const savedSession=localStorage.getItem(SESSION_KEY);
 if(savedSession){current=users.find(u=>u.username===savedSession)||null}
 if(current)showApp();else showLogin();
})();
</script>
</body>
</html>
