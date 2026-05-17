<template>
  <header class="site-header">
    <div class="container">
      <a class="brand" href="#">
        <img class="logo" :src="logoSvg" alt="Scanterior Logo" />
        <div>
          <span class="title">Scanterior</span>
        </div>  
      </a>

      <nav class="nav" aria-label="Main navigation">
        <a href="#features">Features</a>
        <a href="#pricing">Pricing</a>
        <a href="#docs">Docs</a>
        <a href="#about">About us</a>
      </nav>

      <div class="actions">
        <a class="btn ghost" href="#login">Log in</a>
        <a class="btn primary" href="#get-started">Get Started</a>
      </div>
    </div>
  </header>
</template>

<script setup>
// Lightweight presentational header for the Scanterior site
import logoSvg from '@/assets/rect1.svg'
</script>

<style scoped>
@font-face {
  font-family: 'LunaObscura';
  src: url('@/assets/HS_LunaObscura.ttf') format('truetype');
}

:root{
  --bg:#0f1724; --muted:#94a3b8; --accent:#4f46e5; --surface:#0b1220; --glass: rgba(255,255,255,0.04);
}
.site-header{position:fixed;top:0;left:0;right:0;z-index:1000;background:linear-gradient(180deg,rgba(11,18,32,0.2),rgba(11,18,32,0.5));backdrop-filter:blur(5px);border-bottom:1px solid rgba(255,255,255,0.08);}
.container{max-width:1800px;margin:0 auto;display:flex;align-items:center;justify-content:space-between;padding:14px 20px;gap:16px;width:100%;box-sizing:border-box}
.brand{display:flex;align-items:center;gap:10px;color:white;text-decoration:none;font-family:'LunaObscura',sans-serif}
.logo{width:36px;height:36px;color:var(--accent)}
.title{font-weight:700;font-size:2rem;font-family:'LunaObscura',sans-serif}
.tag{display:block;font-size:0.65rem;color:var(--muted);margin-top:-2px}
.nav{display:flex;gap:14px;align-items:center;font-family:'LunaObscura',sans-serif}
.nav a{color:var(--muted);text-decoration:none;font-weight:600;padding:8px;border-radius:6px}
.nav a:hover{color:white;background:var(--glass)}
.actions{display:flex;gap:10px;align-items:center}
.btn{font-weight:700;padding:8px 12px;border-radius:8px;text-decoration:none;font-family:'LunaObscura',sans-serif}
.btn.ghost{color:var(--muted);background:transparent;border:1px solid rgba(255,255,255,0.03)}
.btn.primary{background:linear-gradient(90deg,var(--accent),#7c3aed);color:white}

@media (max-width:1100px){
  .nav{display:none}
  .title{font-size:1rem}
  .container{padding:10px}
}
</style>
