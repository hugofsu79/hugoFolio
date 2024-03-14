<script>
  import Card from "./element/Card.Widget.svelte";
  import Loop from "./element/Loop.Widget.svelte";
  import
</script>

<svelte:head>
  <title>Home</title>
  <meta name="description" content="Svelte demo app" />
</svelte:head>

<section>
  <div id="container">
    <div class="profil">
      <div>
        <img src="src/lib/svg/logoHugoFolio.svg" alt="Hugo Foisseau" />
        <img src="src/lib/png/photoDescription.png" alt="Moi" />
      </div>
      
    </div>
    <div>
      <Loop />
      <Card />
    </div>
  </div>
</section>

<style>
  img {
    border-radius: 1rem;
  }
  #container {
    display: flex;
    flex-direction: row;
    gap: 4px;
  }
  div img {
    width: 40rem;
  }
</style>
