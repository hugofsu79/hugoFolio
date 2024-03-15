<!-- <script>
  import { onMount } from "svelte";

  onMount(() => {
    // Code à exécuter lorsque le composant est monté sur le DOM
    typeWriterEffect();
  });

  const words = [
    "Hey !",
    "Je m'appelle Hugo",
    "je suis développeur front",
    "Concepteur d'application",
  ];
  let wordIndex = 0;
  let letterIndex = 0;
  let isDeleting = false;
  let delay = 200;
  let text = "";

  function typeWriterEffect() {
    const currentWord = words[wordIndex];
    text = isDeleting
      ? currentWord.slice(0, --letterIndex)
      : currentWord.slice(0, ++letterIndex);
    document.querySelector(".typewrite").textContent = text;

    delay = isDeleting ? 100 : 200;

    if (!isDeleting && text.length === currentWord.length) {
      delay = 1000;
      isDeleting = true;
    } else if (isDeleting && text === "") {
      delay = 500;
      isDeleting = false;
      wordIndex = (wordIndex + 1) % words.length;
    }

    setTimeout(typeWriterEffect, delay);
  }

  // Background Mouse
  document.addEventListener("mousemove", (e) => {
    const anchor = document.getElementById("anchor");
    const hue = (e.clientX / window.innerWidth) * 360;
    const hey = (e.clientY / window.innerWidth) * 360;
    anchor.style.backgroundColor = `hsl(${hue}, 50%, 50%)`;
    anchor.style.backgroundColor = `hsl(${hey}, 50%, 50%)`;
  });
</script> -->

<div class="anchor" id="anchor">
  <p class="title">&ZeroWidthSpace;</p>
  <p class="typewrite"></p>
</div>

<style>
  body {
    margin: 0;
    padding: 0;
    background-color: #000000;
  }

  .anchor {
    font-family: "Helvetica", "Arial", sans-serif;
    display: flex;
    align-items: center;
    justify-content: center;
    height: 9.8rem;
    color: white;
    background-color: blueviolet;
    border-radius: 10px;
  }

  .anchor p {
    font-size: 4em;
  }

  .typewrite {
    position: relative;
  }

  .typewrite::after {
    content: "";
    width: 1px;
    width: 1px;
    border-right: 15px solid white;
    border-radius: 2em;
    height: 100%;
    color: white;
    margin-left: 0.5rem;
    animation: blink 1s infinite;
  }

  @keyframes blink {
    0% {
      opacity: 0;
    }

    100% {
      opacity: 1;
    }
  }
</style>
