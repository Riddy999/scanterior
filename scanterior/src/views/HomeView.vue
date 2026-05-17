<script setup lang="ts">
import churchImage from '@/assets/michael_pointner-church-7353292.jpg'
import Footer from '@/components/Footer.vue';
</script>

<template>
  <main class="home-view mt-20">
    <section class="hero" :style="{ backgroundImage: `linear-gradient(rgba(6, 12, 28, 0.45), rgba(6, 12, 28, 0.85)), url(${churchImage})` }">
      <div class="hero-content">
        <h1 class="mt-3.5">Scanterior <br> - <br>Scan your Interior</h1>
        <p class="subtitle">
          Scannen Sie Räume und Gebäude mit Ihrer Kamera. Erhalten Sie präzise 3D-Modelle für die professionelle Weiterbearbeitung in CAD-Programmen. Entwickelt für Architekt_innen, Designer und Kreative.
        </p>
        <div class="hero-actions">
          <a class="btn primary" href="#experience">Experience</a>
          <a class="btn ghost" href="#details">Discover</a>
        </div>
      </div>
    </section>

    <section class="summary" id="experience">
      <article class="card">
        <span class="card-label">Technologie</span>
        <h2>3D-Photogrammetrie</h2>
        <p>Wandeln Sie einfache Fotoaufnahmen in präzise 3D-Modelle um. Unsere fortschrittliche Scanning-Technologie erfasst jedes Detail von Innenräumen und Gebäudefassaden.</p>
      </article>

      <article class="card">
        <span class="card-label">Integration</span>
        <h2>CAD-Export</h2>
        <p>Exportieren Sie Ihre 3D-Scans in gängigen Dateiformaten direkt für die Weiterbearbeitung in professionellen CAD-Programmen wie AutoCAD, Revit und SketchUp.</p>
      </article>

      <article class="card">
        <span class="card-label">Mobilität</span>
        <h2>Kamera-Anbindung</h2>
        <p>Verbinden Sie Ihre Kamera mit dem Gerät und scannen Sie mobil verschiedene Innenräume und Fassaden. Optimiert für leistungsstarke PCs und Laptops.</p>
      </article>
    </section>

    <section class="details" id="details">
      <div class="details-card">
        <h3>Professionelle Anwendungen</h3>
        <p>Scanterior ist die Lösung für Architekt_innen, Fassadenrestaurateur_innen und Interior Designer, die schnell und präzise digitale 3D-Modelle ihrer Projekte benötigen.</p>
      </div>
      <div class="details-card highlight">
        <h3>Kreative Anwendungen</h3>
        <p>Gamedesigner und digitale Künstler_innen nutzen unsere 3D-Scans als Basis für immersive Umgebungen und realistische virtuelle Welten.</p>
      </div>
    </section>
  </main>
</template>

<style scoped>
@font-face {
  font-family: 'LunaObscura';
  src: url('@/assets/HS_LunaObscura.ttf') format('truetype');
  font-display: swap;
}

.home-view {
  flex: 1;
  min-height: 0;
  display: flex;
  flex-direction: column;
  gap: 2.25rem;
  background: radial-gradient(circle at top, rgba(255, 255, 255, 0.05), transparent 32%),
    #060c1c;
  color: #f8fafc;
  font-family: Inter, system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

.hero {
  position: relative;
  display: grid;
  place-items: center;
  min-height: 72vh;
  border-radius: 32px;
  overflow: hidden;
  background-size: cover;
  background-position: center;
  box-shadow: 0 40px 120px rgba(0, 0, 0, 0.35);
}

.hero::before {
  content: '';
  position: absolute;
  inset: 0;
  background: radial-gradient(circle at 20% 20%, rgba(255, 255, 255, 0.12), transparent 35%);
}

.hero-content {
  position: relative;
  z-index: 1;
  max-width: 760px;
  padding: 3rem 2rem;
  text-align: center;
}

.hero-content h1 {
  margin-top: 50px;
  font-family: 'LunaObscura', sans-serif;
  font-size: clamp(2.8rem, 4vw, 4.5rem);
  line-height: 1.02;
  letter-spacing: -0.04em;
}

.subtitle {
  margin: 1.6rem auto 0;
  max-width: 640px;
  color: rgba(248, 250, 252, 0.88);
  font-size: 1.05rem;
  line-height: 1.85;
}

.hero-actions {
  margin-top: 2.4rem;
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1rem;
}

.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  min-width: 150px;
  padding: 0.95rem 1.75rem;
  border-radius: 999px;
  font-weight: 700;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.btn:hover {
  transform: translateY(-1px);
}

.btn.primary {
  background: linear-gradient(90deg, #7c3aed, #4338ca);
  color: white;
  box-shadow: 0 18px 40px rgba(124, 58, 237, 0.28);
}

.btn.ghost {
  border: 1px solid rgba(248, 250, 252, 0.18);
  color: #e2e8f0;
  background: rgba(255, 255, 255, 0.06);
}

.summary,
.details {
  display: grid;
  gap: 1.25rem;
}

.summary {
  grid-template-columns: repeat(3, minmax(0, 1fr));
  padding: 0 1rem;
}

.card,
.details-card {
  background: rgba(15, 23, 42, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: 28px;
  padding: 1.75rem;
  box-shadow: 0 20px 45px rgba(15, 23, 42, 0.22);
}

.card-label {
  display: inline-block;
  margin-bottom: 1rem;
  color: #c7d2fe;
  text-transform: uppercase;
  letter-spacing: 0.2em;
  font-size: 0.75rem;
}

.card h2,
.details-card h3 {
  margin: 0 0 1rem;
  font-family: 'LunaObscura', sans-serif;
  font-size: 1.6rem;
}

.card p,
.details-card p {
  margin: 0;
  color: rgba(248, 250, 252, 0.82);
  line-height: 1.8;
}

.details {
  grid-template-columns: 1.2fr 0.8fr;
  padding: 0 1rem;
  margin-bottom: 6rem;
}

.details-card.highlight {
  background: linear-gradient(180deg, rgba(67, 56, 202, 0.18), rgba(15, 23, 42, 0.9));
}

@media (max-width: 1024px) {
  .summary,
  .details {
    grid-template-columns: 1fr;
  }

  .hero-content {
    padding: 2.5rem 1.5rem;
  }
}

@media (max-width: 640px) {
  .home-view {
    gap: 1.5rem;
  }

  .hero {
    min-height: 62vh;
  }

  .hero-content h1 {
    font-size: 2.35rem;
  }

  .hero-actions {
    flex-direction: column;
  }
}
</style>