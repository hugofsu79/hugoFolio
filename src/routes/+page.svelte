<script>
  import Card from "./element/Card.Widget.svelte";
  import Loop from "./element/Loop.Widget.svelte";
  import TextRide from "./element/textRide.Widget.svelte";
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
        <div class="thumb">
          <video controls loop autoplay width="640"
            ><source
              src="src/lib/video/profilHugo.mov"
              type="video/mp4"
            /></video
          >
        </div>
      </div>
      <div><TextRide /></div>
      <div class="formatIcone">
        <a href="https://github.com/hugofsu79" title="Github" target="_blank">
          <img src="src/routes/element/homeSource/gitHub.svg" alt="github" /></a
        >
        <a
          href="https://www.linkedin.com/in/hugo-foisseau-aa9b14100/"
          title="linkedin"
          target="_blank"
        >
          <img
            src="src/routes/element/homeSource/linkedin.svg"
            alt="linkedin"
          /></a
        >
        <a href="mailto:hugo266@icloud.com">
          <img src="src/routes/element/homeSource/mail.svg" alt="" /></a
        >
        <iframe
          style="border: none; width: 72%; height: 55px; border-radius: 10px; background-color: rgb(255, 255, 255);"
          src="https://bandcamp.com/EmbeddedPlayer/track=3675169527/size=small/bgcol=ffffff/linkcol=0687f5/transparent=true/"
          seamless
          ><a href="https://pragmanewmusic.bandcamp.com/track/our-way"
            >Our way by Pragma</a
          ></iframe
        >
      </div>
    </div>
    <div>
      <Loop />
      <Card />
    </div>
  </div>
</section>

<style>
  video {
    border-radius: 10px;
  }
  .formatIcone img {
    margin-top: 5px;
    width: 55px;
    cursor: pointer;
    transition-duration: 0.5s;
  }
  .formatIcone img:hover {
    filter: brightness(150%);
    transition-duration: 0.5s;
  }

  img {
    border-radius: 10px;
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
