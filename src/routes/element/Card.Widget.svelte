<script>
  import { onMount } from "svelte";

  // Tableau des couleurs possibles
  const colors = ["#333333", "#F1F1F1", "#A0A0A0", "#656563"];

  let cards;

  onMount(() => {
    cards = document.querySelectorAll(".card");

    // Fonction pour générer une couleur aléatoire
    const getRandomColor = () => {
      return colors[Math.floor(Math.random() * colors.length)];
    };

    cards.forEach((card) => {
      card.style.backgroundColor = getRandomColor();
    });

    document.getElementById("cardProjet").onmousemove = (e) => {
      for (const card of cards) {
        const rect = card.getBoundingClientRect(),
          x = e.clientX - rect.left,
          y = e.clientY - rect.top;

        card.style.setProperty("--mouse-x", `${x}px`);
        card.style.setProperty("--mouse-y", `${y}px`);
      }
    };
  });
</script>

<div id="cardProjet">
  <div class="gridLeft">
    <!-- Rhizome -->
    <div class="card">
      <img
        class="logo"
        src="src/routes/element/cardSource/rhizome.svg"
        alt="Rhizome"
      />

      <img
        class="arrow"
        src="src/routes/element/cardSource/arrow.svg"
        alt="Allez"
      />
      <div class="card-border"></div>
      <div class="card-content"></div>
    </div>

    <!-- Kahwas -->
    <div class="card">
      <img
        class="logo"
        src="src/routes/element/cardSource/kahwas.svg"
        alt="kahwas"
      />

      <img
        class="arrow"
        src="src/routes/element/cardSource/arrow.svg"
        alt="Allez"
      />
      <div class="card-border"></div>
      <div class="card-content"></div>
    </div>
  </div>

  <!-- Bombino -->
  <div class="gridRBombino">
    <div class="card">
      <img
        class="logo" 
        src="src/routes/element/cardSource/bombino.svg"
        alt="bombino"
      />

      <img
        class="arrow"
        src="src/routes/element/cardSource/arrow.svg"
        alt="Allez"
      />
      <div class="card-border"></div>
      <div class="card-content"></div>
    </div>
  </div>
</div>

<!-- Kinema -->
<div class="cardBottom">
  <div class="card">
    <img
      class="logo"
      src="src/routes/element/cardSource/kinema.svg"
      alt="kinema"
    />

    <img
      class="arrow"
      src="src/routes/element/cardSource/arrow.svg"
      alt="Allez"
    />
    <div class="card-border"></div>
    <div class="card-content"></div>
  </div>
</div>

<style>
  #cardProjet {
    padding: 0;
    margin: 0;
    /* max-width: 65rem; */
    display: flex;
    justify-content: space-between;
    width: calc(60% - 40px);
  }
  .gridLeft {
    display: flex;
    flex-direction: column;
  }
  .gridRBombino .card {
    height: 100%;
    width: 31rem;
  }

  .cardBottom .card {
    width: 66.3rem;
    height: 23.2rem;
  }
  .card {
    border-radius: 10px;
    cursor: pointer;
    height: 260px;
    position: relative;
    width: 35rem;
    margin: 5px 5px 0px 0px;
  }

  .card:hover::before,
  .card:hover > .card-border {
    opacity: 1;
  }

  .card::before {
    border-radius: inherit;
    content: "";
    height: 100%;
    left: 0px;
    opacity: 0;
    position: absolute;
    top: 0px;
    transition: opacity 500ms;
    width: 35rem;
  }

  .card::before {
    background: radial-gradient(
      800px circle at var(--mouse-x) var(--mouse-y),
      rgba(255, 255, 255, 0.212),
      transparent 40%
    );
    z-index: 3;
  }

  .card > .card-border {
    background: radial-gradient(
      400px circle at var(--mouse-x) var(--mouse-y),
      rgba(255, 255, 255, 0.03)
    );
    z-index: 1;
  }

  .card > .card-content {
    background-color: var(--card-color);
    border-radius: inherit;
    height: calc(100% - 2px);
    margin: 1px;
    position: relative;
    width: calc(100% - 2px);
    z-index: 1;
  }
  .logo::before {
    transform: translateY(100%);
  }
  .logo {
    width: 6rem;
    display: block;
    margin: 0 auto;
    transform: translateY(50%);
    transition: 1s;
  }
  .arrow {
    width: 2rem;
    position: relative;
    padding-left: 1rem;
    top: 90px;
  }
  .arrow::after {
    transform: rotate(45deg);
  }
</style>
