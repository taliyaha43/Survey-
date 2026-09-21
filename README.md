
<!doctype html>
<html lang="en">
<head>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">

  <meta
    name="description"
    content="A technology interest survey created by Taliyah Divine."
  >

  <title>Technology Interest Survey | Taliyah Divine</title>

  <link
    rel="icon"
    type="image/svg+xml"
    href="data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 64 64'%3E%3Crect width='64' height='64' rx='14' fill='%230b281d'/%3E%3Cpath d='M16 20h32v8H36v22h-8V28H16z' fill='%2378e7ad'/%3E%3C/svg%3E"
  >

  <style>
    :root {
      color-scheme: dark;
      --ink: #f2f7f4;
      --muted: #a9bcb2;
      --page: #07110d;
      --panel: #10251b;
      --line: #2c5742;
      --accent: #78e7ad;
      --accent-dark: #133a28;
      --focus: #b7ffd7;
    }

    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system,
        BlinkMacSystemFont, "Segoe UI", sans-serif;
      color: var(--ink);
      background:
        radial-gradient(
          circle at 12% 8%,
          rgba(120, 231, 173, 0.13),
          transparent 28rem
        ),
        linear-gradient(
          145deg,
          #07110d 0%,
          #0b1711 52%,
          #07110d 100%
        );
    }

    .shell {
      width: min(100% - 32px, 760px);
      margin: 0 auto;
      padding: 48px 0 64px;
    }

    header {
      margin-bottom: 28px;
    }

    .eyebrow {
      display: inline-flex;
      align-items: center;
      gap: 8px;
      margin: 0 0 14px;
      color: var(--accent);
      font-size: 0.8rem;
      font-weight: 750;
      letter-spacing: 0.14em;
      text-transform: uppercase;
    }

    .eyebrow::before {
      content: "";
      width: 28px;
      height: 2px;
      background: currentColor;
    }

    h1 {
      margin: 0;
      max-width: 650px;
      font-size: clamp(2.35rem, 8vw, 4.7rem);
      line-height: 0.98;
      letter-spacing: -0.055em;
    }

    #description {
      max-width: 620px;
      margin: 20px 0 0;
      color: var(--muted);
      font-size: 1.05rem;
      line-height: 1.7;
    }

    form {
      display: grid;
      gap: 24px;
      padding: clamp(22px, 5vw, 40px);
      border: 1px solid var(--line);
      border-radius: 24px;
      background: rgba(16, 37, 27, 0.91);
      box-shadow: 0 28px 70px rgba(0, 0, 0, 0.3);
      backdrop-filter: blur(12px);
    }

    .grid {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 18px;
    }

    .field,
    fieldset {
      min-width: 0;
    }

    label,
    legend {
      display: block;
      margin-bottom: 9px;
      font-size: 0.93rem;
      font-weight: 720;
    }

    .optional {
      color: var(--muted);
      font-size: 0.78rem;
      font-weight: 500;
    }

    input,
    select,
    textarea,
    button {
      font: inherit;
    }

    input[type="text"],
    input[type="email"],
    input[type="number"],
    select,
    textarea {
      width: 100%;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: #0a1a12;
      color: var(--ink);
      padding: 13px 14px;
      font-size: 1rem;
      outline: none;
      transition:
        border-color 0.18s ease,
        box-shadow 0.18s ease,
        transform 0.18s ease;
    }

    input:focus,
    select:focus,
    textarea:focus {
      border-color: var(--focus);
      box-shadow: 0 0 0 4px rgba(120, 231, 173, 0.16);
    }

    textarea {
      min-height: 126px;
      resize: vertical;
    }

    fieldset {
      margin: 0;
      padding: 0;
      border: 0;
    }

    .choices {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 10px;
    }

    .choice {
      display: flex;
      align-items: center;
      gap: 11px;
      min-height: 48px;
      margin: 0;
      padding: 10px 12px;
      border: 1px solid var(--line);
      border-radius: 12px;
      background: rgba(7, 17, 13, 0.46);
      font-weight: 560;
      cursor: pointer;
    }

    .choice:hover {
      border-color: #4b8b6a;
    }

    .choice input {
      width: 18px;
      height: 18px;
      accent-color: var(--accent);
    }

    button {
      width: 100%;
      border: 0;
      border-radius: 13px;
      padding: 15px 20px;
      background: var(--accent);
      color: #062014;
      font-weight: 800;
      cursor: pointer;
      transition:
        transform 0.18s ease,
        box-shadow 0.18s ease,
        filter 0.18s ease;
    }

    button:hover {
      transform: translateY(-2px);
      box-shadow: 0 12px 28px rgba(120, 231, 173, 0.18);
      filter: brightness(1.04);
    }

    button:focus-visible {
      outline: 3px solid var(--focus);
      outline-offset: 4px;
    }

    .success {
      display: none;
      margin: 0;
      padding: 13px 15px;
      border: 1px solid #4b8b6a;
      border-radius: 12px;
      background: var(--accent-dark);
      color: #d9ffea;
      line-height: 1.5;
    }

    .success.show {
      display: block;
    }

    footer {
      margin-top: 20px;
      color: var(--muted);
      font-size: 0.9rem;
      text-align: center;
    }

    @media (max-width: 620px) {
      .shell {
        width: min(100% - 24px, 760px);
        padding-top: 32px;
      }

      .grid,
      .choices {
        grid-template-columns: 1fr;
      }

      h1 {
        font-size: clamp(2.3rem, 14vw, 3.8rem);
      }
    }

    @media (prefers-reduced-motion: reduce) {
      *,
      *::before,
      *::after {
        scroll-behavior: auto !important;
        transition: none !important;
      }
    }
  </style>
</head>

<body>
  <main class="shell">
    <header>
      <p class="eyebrow">HTML Project</p>

      <h1 id="title">Technology Interest Survey</h1>

      <p id="description">
        Share what interests you most about technology and the skills you want
        to explore. This project was created by Taliyah Divine.
      </p>
    </header>

    <form id="survey-form">
      <div class="grid">
        <div class="field">
          <label id="name-label" for="name">Name</label>

          <input
            id="name"
            name="name"
            type="text"
            placeholder="Enter your name"
            autocomplete="name"
            required
          >
        </div>

        <div class="field">
          <label id="email-label" for="email">Email</label>

          <input
            id="email"
            name="email"
            type="email"
            placeholder="you@example.com"
            autocomplete="email"
            required
          >
        </div>
      </div>

      <div class="grid">
        <div class="field">
          <label id="number-label" for="number">
            Age <span class="optional">(optional)</span>
          </label>

          <input
            id="number"
            name="age"
            type="number"
            min="13"
            max="100"
            placeholder="18"
          >
        </div>

        <div class="field">
          <label for="dropdown">Favorite area of technology</label>

          <select id="dropdown" name="technology" required>
            <option value="" disabled selected>Select one</option>
            <option value="cloud">Cloud computing</option>
            <option value="cybersecurity">Cybersecurity</option>
            <option value="web-development">Web development</option>
            <option value="data-ai">Data and AI</option>
          </select>
        </div>
      </div>

      <fieldset>
        <legend>Would you consider a career in technology?</legend>

        <div class="choices">
          <label class="choice">
            <input
              type="radio"
              name="career"
              value="yes"
              required
            >
            Yes
          </label>

          <label class="choice">
            <input
              type="radio"
              name="career"
              value="maybe"
            >
            Maybe
          </label>

          <label class="choice">
            <input
              type="radio"
              name="career"
              value="no"
            >
            Not right now
          </label>
        </div>
      </fieldset>

      <fieldset>
        <legend>
          Which skills interest you?
          <span class="optional">Choose all that apply</span>
        </legend>

        <div class="choices">
          <label class="choice">
            <input
              type="checkbox"
              name="skills"
              value="html-css"
            >
            HTML &amp; CSS
          </label>

          <label class="choice">
            <input
              type="checkbox"
              name="skills"
              value="python"
            >
            Python
          </label>

          <label class="choice">
            <input
              type="checkbox"
              name="skills"
              value="aws"
            >
            AWS Cloud
          </label>

          <label class="choice">
            <input
              type="checkbox"
              name="skills"
              value="security"
            >
            Cybersecurity
          </label>
        </div>
      </fieldset>

      <div class="field">
        <label for="comments">
          Anything else you want to share?
          <span class="optional">(optional)</span>
        </label>

        <textarea
          id="comments"
          name="comments"
          placeholder="Tell us about your technology goals..."
        ></textarea>
      </div>

      <p
        id="success-message"
        class="success"
        role="status"
        aria-live="polite"
      >
        Thanks! Your response was recorded for this project demonstration.
      </p>

      <button id="submit" type="submit">
        Submit survey
      </button>
    </form>

    <footer>
      Built with HTML and CSS by Taliyah Divine.
    </footer>
  </main>

  <script>
    const form = document.getElementById("survey-form");
    const message = document.getElementById("success-message");

    form.addEventListener("submit", (event) => {
      event.preventDefault();

      message.classList.add("show");

      message.scrollIntoView({
        behavior: "smooth",
        block: "nearest"
      });
    });

    form.addEventListener("input", () => {
      message.classList.remove("show");
    });
  </script>
</body>
</html>