<div id="traits">
  <div class="traits-slide">
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
  </div>
  <div class="traits-slide">
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
  </div>
  <div class="traits-slide">
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
    <img class="trait" src="src/routes/element/trait.svg" alt="trait" />
  </div>
</div>

<style>
  * {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
    border-radius: 10px;
    width: 52.3rem;
    height: 50px;
  }

  @keyframes slide {
    from {
      transform: translateX(0);
    }

    to {
      transform: translateX(-100%);
    }
  }

  #traits {
    overflow: hidden;
    /* padding: -60px 0; */
    background: #ffffff;
    white-space: nowrap;
  }

  .traits-slide {
    height: 10px;
    display: inline-block;
    animation: 10s slide infinite linear;
  }

  .trait {
  }
</style>
