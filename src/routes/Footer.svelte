<footer>
  <div id="container">
    <div class="flexLeft">
      <p>Hugo Foisseau</p>
    </div>
    <div class="flexCenter">
      <img src="src/lib/svg/hugoPoint.svg" alt="" />
      <img src="src/lib/svg/merci.svg" alt="" />
      <img src="src/lib/svg/foisseauPoint.svg" alt="" />
    </div>
    <div class="flexRight">
      <p>Niort N 46° 19’ 51.168’’ O 46° 28’ 14.989’’</p>
    </div>
  </div>
</footer>

<style>
  footer {
    /* justify-content: center;
    align-items: center; */
    background-color: #e5431e;
  }

  footer #container {
    display: flex;
    flex-direction: row;
    align-content: center;
    justify-content: space-between;
    padding: 0em 1em 0em 1em;
  }
  footer .flexCenter {
    display: block;
  }
  footer .flexCenter img {
    display: flex;
    padding: 4rem;
    flex-direction: row;
    justify-content: space-between;
    height: 4em;
    margin: 0 auto;
  }

  @media (min-width: 480px) {
    footer {
      padding: 12px 0;
    }
  }
</style>
