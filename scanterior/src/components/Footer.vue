<template>
  <header :class="['site-header', { visible: isVisible }]">
    <div class="container">
    
      <nav class="nav" aria-label="Main navigation">
        <a href="#pricing">Lizenz</a>
        <a href="#about">Kontakt</a>
        <a href="#about">Barrierefreiheit</a>
        <RouterLink to="/datenschutz">Datenschutz</RouterLink>
        <RouterLink to="/impressum">Impressum</RouterLink>
      </nav>

    </div>
  </header>
</template>

<script setup>
import { onMounted, onUnmounted, ref } from 'vue'
import logoSvg from '@/assets/rect1.svg'

const isVisible = ref(false)

const checkFooterVisibility = () => {
  const doc = document.documentElement
  isVisible.value = Math.ceil(window.scrollY + window.innerHeight) >= doc.scrollHeight - 2
}

onMounted(() => {
  checkFooterVisibility()
  window.addEventListener('scroll', checkFooterVisibility, { passive: true })
  window.addEventListener('resize', checkFooterVisibility)
})

onUnmounted(() => {
  window.removeEventListener('scroll', checkFooterVisibility)
  window.removeEventListener('resize', checkFooterVisibility)
})
</script>

<style scoped>
@font-face {
  font-family: 'LunaObscura';
  src: url('@/assets/HS_LunaObscura.ttf') format('truetype');
}

:root{
  --bg:#0f1724; --muted:#94a3b8; --accent:#4f46e5; --surface:#0b1220; --glass: rgba(255,255,255,0.04);
}
.site-header{
  position:fixed;
  bottom:0;
  left:0;
  right:0;
  top:auto;
  z-index:1000;
  transform: translateY(100%);
  opacity: 0;
  pointer-events: none;
  background: linear-gradient(180deg, rgba(11, 18, 32, 0.2), rgba(11, 18, 32, 0.5));
  backdrop-filter: blur(5px);
  border-top: 1px solid rgba(255, 255, 255, 0.08);
  transition: transform 0.3s ease, opacity 0.25s ease;
}

.site-header.visible {
  transform: translateY(0);
  opacity: 1;
  pointer-events: auto;
}

.container{
  max-width:1800px;
  margin:0 auto;
  display:flex;
  align-items:center;
  justify-content:space-between;
  padding:14px 20px;
  gap:16px;
  width:100%;
  box-sizing:border-box;
}
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

</style>
