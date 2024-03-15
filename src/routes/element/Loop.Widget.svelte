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
    width: 66rem;
    /* padding: -60px 0; */
    background: #ffffff;
    white-space: nowrap;
    border-radius: 10px;
  }

  .traits-slide {
    height: 10px;
    display: inline-block;
    animation: 10s slide infinite linear;
  }

  .trait {
  }
</style>
