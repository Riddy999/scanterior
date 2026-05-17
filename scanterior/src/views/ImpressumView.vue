<template>
  <div class="page">
    <div class="about text-white">
      <h3 class="pt-3">Impressum</h3>

      <p>
        Angaben gemäß § 5 ECG, § 25 Mediengesetz und § 14 UGB
      </p>

      <p>
        <strong>Scanterior GmbH</strong><br />
        Karlsplatz 13, Stiege 4, Tür 8<br />
        1040 Wien<br />
        Österreich
      </p>

      <p>
        <strong>Telefon:</strong> +43 664 123 456<br />
        <strong>E-Mail:</strong> felixe@scanterior.at<br />
        <strong>Website:</strong> <a href="https://riddy999.github.io/scanterior/">www.scanterior.at</a>
      </p>

      <h5>Unternehmensgegenstand</h5>
      <p>
        Scanterior entwickelt Desktop-Software zur Erfassung von Innenräumen und Gebäudefassaden
        mittels Fotoaufnahmen. Die Anwendung wandelt eine Serie von Bildern in hochauflösende
        3D-Scans um, die in gängigen Formaten (z. B. OBJ, PLY, IFC) exportiert und in CAD-Programmen
        weiterverarbeitet werden können. Die Software ist für leistungsfähige PCs und Laptops
        optimiert und unterstützt die Anbindung externer Kameras für mobile Scanvorgänge.
      </p>

      <p>
        <strong>Firmenbuchnummer:</strong> 55822w<br />
        <strong>Firmenbuchgericht:</strong> Handelsgericht Wien
      </p>

      <p>
        <strong>UID-Nummer:</strong> ATU14712303
      </p>

      <p>
        <strong>Geschäftsführer:</strong><br />
        Felix Effenberg
      </p>

      <p>
        <strong>Mitglied der:</strong><br />
        Wirtschaftskammer Wien
      </p>

      <p>
        <strong>Aufsichtsbehörde:</strong><br />
        Magistratisches Bezirksamt des 4. Gemeindebezirk Wiens
      </p>

      <h5>Anwendbare Rechtsvorschriften</h5>
      <p>Gewerbeordnung: <a href="https://www.ris.bka.gv.at">www.ris.bka.gv.at</a></p>

      <h5>Medieninhaber und Herausgeber</h5>
      <p>
        <strong>Scanterior GmbH</strong><br />
        Karlsplatz 13, Stiege 4, Tür 8<br />
        1040 Wien<br />
        Österreich
      </p>

      <h5>Online-Streitbeilegung</h5>
      <p>
        <a href="https://ec.europa.eu/consumers/odr">https://ec.europa.eu/consumers/odr</a>
      </p>

      <p>
        Verbraucher haben die Möglichkeit, Beschwerden an die oben genannte
        Online-Streitbeilegungsplattform zu richten.
      </p>

    </div>
  </div>
</template>

<style>
.page {
  min-height: 100vh;
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 2rem 1rem;
}

.about {
  width: min(900px, 100%);
  padding: 2rem 1rem 3rem;
  display: flex;
  flex-direction: column;
  gap: 1.5rem;
  line-height: 1.75;
  margin: 0;
}

.about h3,
.about h5 {
  margin: 0;
  font-size: 1.5rem;
}

.about h3 {
  font-size: 2rem;
}

.headline {
  text-align: center;
  margin: 0;
  font-size: 1.1rem;
  font-weight: 700;
}

.about p {
  margin: 0;
}

.about ul {
  margin: 0;
  padding-left: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}

.about a {
  color: inherit;
  text-decoration: underline;
}

@media (min-width: 1024px) {
  .page {
    padding: 3rem 2rem;
  }
}
</style>
