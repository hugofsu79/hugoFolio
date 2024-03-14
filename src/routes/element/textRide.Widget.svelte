<script>
  function typeWriterEffect() {
    const words = [
      "Hey !",
      "Je m'appelle Hugo",
      "je suis développeur front",
      "Concepteur d'application",
    ];
    let wordCount = 0, // Compteur de mots
      letterCount = 0, // Compteur de lettres
      currentText = "",
      currentWord = "",
      timeOut = 200, // durée par défaut avant la prochaine action
      isDeleting = false; // Indicateur de suppression de lettres
    function type() {
      wordCount === words.length && (wordCount = 0),
        (currentWord = words[wordCount]),
        (currentText = isDeleting
          ? currentWord.slice(0, --letterCount)
          : currentWord.slice(0, ++letterCount)),
        (document.querySelector(".typewrite").textContent = currentText),
        (timeOut = isDeleting ? 100 : 200),
        (!isDeleting &&
          currentText.length === currentWord.length &&
          ((timeOut = 1e3), (isDeleting = !0))) ||
          (isDeleting &&
            0 === currentText.length &&
            ((timeOut = 500), (isDeleting = !1), wordCount++)),
        setTimeout(type, timeOut);
    }
    type();
  }
  typeWriterEffect();

  //background Mouse
  document.addEventListener("mousemove", (e) => {
    const anchor = document.getElementById("anchor");
    const hue = (e.clientX / window.innerWidth) * 360; // Calculer la teinte en fonction de la position horizontale de la souris
    const hey = (e.clientY / window.innerWidth) * 360; // Calculer la teinte en fonction de la position verticale de la souris
    anchor.style.backgroundColor = `hsl(${hue}, 50%, 50%)`; // Appliquer la couleur de fond en utilisant HSL
    anchor.style.backgroundColor = `hsl(${hey}, 50%, 50%)`; // Appliquer la couleur de fond en utilisant HSL
  });
</script>

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
    height: 100vh;
    color: white;
    background-color: blueviolet;
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
