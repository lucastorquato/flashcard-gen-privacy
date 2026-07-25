<style>
  html {
    overflow-x: hidden;
  }

  body {
    margin: 0;
    padding: 0;
    overflow-x: hidden;
    background: #f3f6ff;
  }

  .wrapper {
    width: 100%;
    max-width: none;
    margin: 0;
    padding: 0;
  }

  .wrapper > header,
  .wrapper > footer {
    display: none;
  }

  .wrapper > section {
    width: 100%;
    float: none;
    padding: 0;
    border: 0;
  }

  .marketing-page {
    --ink: #f7f7f8;
    --dark: #202020;
    --near-black: #07070a;
    --paper: #f3f6ff;
    --blue: #0c2488;
    --muted-blue: #5267a7;
    --purple: #9f7cf7;
    --text: #15151a;
    --soft-line: rgba(12, 36, 136, 0.14);
    width: min(1120px, calc(100vw - 32px));
    margin: 0 auto;
    color: var(--text);
    font-family: -apple-system, BlinkMacSystemFont, "SF Pro Display", "Inter", "Segoe UI", sans-serif;
  }

  .marketing-page * {
    box-sizing: border-box;
  }

  .marketing-page a {
    color: inherit;
  }

  .marketing-hero {
    margin: 0 calc(50% - 50vw);
    padding: 64px max(24px, calc((100vw - 1120px) / 2)) 0;
    overflow: hidden;
    color: var(--ink);
    text-align: center;
    background: var(--dark);
  }

  .marketing-eyebrow {
    margin: 0 0 18px;
    color: rgba(255, 255, 255, 0.64);
    font-size: 14px;
    font-weight: 800;
    letter-spacing: 0.18em;
    text-transform: uppercase;
  }

  .marketing-title {
    max-width: 900px;
    margin: 0 auto;
    color: var(--ink);
    font-size: clamp(50px, 7.8vw, 96px);
    line-height: 0.98;
    font-weight: 900;
  }

  .marketing-subtitle {
    max-width: 780px;
    margin: 32px auto 38px;
    color: rgba(255, 255, 255, 0.9);
    font-size: clamp(26px, 4vw, 44px);
    line-height: 1.14;
    font-weight: 400;
  }

  .marketing-hero-image {
    display: block;
    width: auto;
    max-width: min(760px, 100%);
    max-height: 760px;
    margin: 0 auto;
    object-fit: contain;
  }

  .marketing-section {
    margin: 0 calc(50% - 50vw);
    padding: 72px max(24px, calc((100vw - 1120px) / 2));
    background: var(--paper);
  }

  .marketing-section:nth-of-type(odd) {
    background: #f7f8ff;
  }

  .feature-grid {
    display: grid;
    grid-template-columns: minmax(0, 1fr) minmax(280px, 420px);
    gap: 52px;
    align-items: center;
  }

  .feature-grid.reverse {
    grid-template-columns: minmax(280px, 420px) minmax(0, 1fr);
  }

  .feature-grid.reverse .feature-copy {
    order: 2;
  }

  .feature-grid.reverse .feature-shot {
    order: 1;
  }

  .feature-copy h2 {
    margin: 0;
    color: var(--blue);
    font-size: clamp(44px, 6.2vw, 76px);
    line-height: 0.98;
    font-weight: 900;
  }

  .feature-copy p {
    max-width: 620px;
    margin: 22px 0 0;
    color: var(--muted-blue);
    font-size: clamp(21px, 2.5vw, 31px);
    line-height: 1.25;
    font-weight: 400;
  }

  .feature-card {
    margin-top: 28px;
    padding: 22px;
    border: 1px solid var(--soft-line);
    border-radius: 8px;
    background: rgba(255, 255, 255, 0.62);
  }

  .feature-card strong {
    display: block;
    color: var(--blue);
    font-size: 18px;
  }

  .feature-card span {
    display: block;
    margin-top: 8px;
    color: #5f6280;
    font-size: 17px;
    line-height: 1.45;
  }

  .feature-shot {
    display: flex;
    justify-content: center;
  }

  .feature-shot img {
    display: block;
    width: auto;
    max-width: min(420px, 100%);
    max-height: 760px;
    height: auto;
    object-fit: contain;
  }

  .closing {
    margin: 0 calc(50% - 50vw);
    padding: 84px max(24px, calc((100vw - 1120px) / 2));
    color: var(--ink);
    text-align: center;
    background: var(--near-black);
  }

  .closing h2 {
    max-width: 860px;
    margin: 0 auto;
    color: var(--ink);
    font-size: clamp(42px, 6vw, 74px);
    line-height: 1;
    font-weight: 900;
  }

  .closing p {
    max-width: 680px;
    margin: 28px auto 0;
    color: rgba(255, 255, 255, 0.76);
    font-size: 24px;
    line-height: 1.35;
  }

  .cta-row {
    display: flex;
    flex-wrap: wrap;
    gap: 14px;
    justify-content: center;
    margin-top: 40px;
  }

  .cta {
    display: inline-flex;
    align-items: center;
    min-height: 52px;
    padding: 0 24px;
    border-radius: 8px;
    font-size: 17px;
    font-weight: 800;
    text-decoration: none;
  }

  .cta.primary {
    color: #0b0715;
    background: var(--purple);
  }

  .cta.secondary {
    color: var(--ink);
    border: 1px solid rgba(255, 255, 255, 0.2);
    background: rgba(255, 255, 255, 0.07);
  }

  @media (max-width: 780px) {
    .marketing-hero {
      padding-top: 58px;
    }

    .marketing-subtitle {
      margin-top: 30px;
    }

    .marketing-section {
      padding-top: 62px;
      padding-bottom: 62px;
    }

    .feature-grid,
    .feature-grid.reverse {
      grid-template-columns: 1fr;
      gap: 38px;
      text-align: center;
    }

    .feature-grid.reverse .feature-copy,
    .feature-grid.reverse .feature-shot {
      order: initial;
    }

    .feature-copy p {
      margin-right: auto;
      margin-left: auto;
    }

    .feature-card {
      text-align: left;
    }
  }

  @media (max-width: 560px) {
    .marketing-title {
      font-size: clamp(46px, 14vw, 68px);
    }

    .marketing-subtitle {
      font-size: clamp(26px, 8vw, 38px);
    }

    .marketing-hero-image,
    .feature-shot img {
      width: min(100%, 430px);
      max-height: none;
    }
  }
</style>

<div class="marketing-page">
  <section class="marketing-hero" aria-labelledby="marketing-title">
    <p class="marketing-eyebrow">FlipNote GEN</p>
    <h1 id="marketing-title" class="marketing-title">Turn Notes Into Flashcards</h1>
    <p class="marketing-subtitle">Type a topic to generate a study deck in seconds.</p>
    <img class="marketing-hero-image" src="./assets/marketing/turn-notes-into-flashcards.png" alt="FlipNote GEN generation screen showing a photosynthesis prompt and card settings.">
  </section>

  <section class="marketing-section">
    <div class="feature-grid">
      <div class="feature-copy">
        <h2>Study one card at a time</h2>
        <p>Move through a focused deck with a clean, tactile flashcard flow built for repetition and recall.</p>
        <div class="feature-card">
          <strong>Simple review flow</strong>
          <span>Each generated card keeps attention on one question before revealing the answer.</span>
        </div>
      </div>
      <div class="feature-shot">
        <img src="./assets/marketing/study-one-card-at-a-time.png" alt="FlipNote GEN study screen showing one photosynthesis flashcard question.">
      </div>
    </div>
  </section>

  <section class="marketing-section">
    <div class="feature-grid reverse">
      <div class="feature-copy">
        <h2>Tap to See the Answer</h2>
        <p>Reveal concise explanations when you are ready, then keep moving through the deck.</p>
        <div class="feature-card">
          <strong>Built for active recall</strong>
          <span>Try the answer first, then flip the card to check the generated explanation.</span>
        </div>
      </div>
      <div class="feature-shot">
        <img src="./assets/marketing/tap-to-see-answer.png" alt="FlipNote GEN answer screen explaining photosynthesis.">
      </div>
    </div>
  </section>

  <section class="marketing-section">
    <div class="feature-grid">
      <div class="feature-copy">
        <h2>Save your decks</h2>
        <p>Keep useful study sessions and return to them whenever you want to review.</p>
        <div class="feature-card">
          <strong>Review now, revisit later</strong>
          <span>Save completed decks so your best study material stays available.</span>
        </div>
      </div>
      <div class="feature-shot">
        <img src="./assets/marketing/save-your-decks.png" alt="FlipNote GEN completion dialog with save and exit options.">
      </div>
    </div>
  </section>

  <section class="marketing-section">
    <div class="feature-grid reverse">
      <div class="feature-copy">
        <h2>Study in Multiple Languages</h2>
        <p>Generate flashcards in the ideal language for your study routine.</p>
        <div class="feature-card">
          <strong>Flexible study material</strong>
          <span>Create decks for classes, exams, and personal learning across supported languages.</span>
        </div>
      </div>
      <div class="feature-shot">
        <img src="./assets/marketing/study-in-multiple-languages.png" alt="FlipNote GEN marketing screenshot for studying in multiple languages.">
      </div>
    </div>
  </section>

  <section class="closing">
    <h2>Flashcards from any topic, ready when you are.</h2>
    <p>FlipNote GEN reduces the gap between having notes and actually studying them.</p>
    <div class="cta-row" aria-label="Marketing page actions">
      <span class="cta primary">Coming soon on the App Store</span>
      <a class="cta secondary" href="./privacy-policy.html">Privacy Policy</a>
    </div>
  </section>
</div>
