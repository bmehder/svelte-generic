<script>
  export let image = "bg.jpg";
  export let source =
    "https://file-examples-com.github.io/uploads/2017/11/file_example_MP3_700KB.mp3";
</script>

<style>
  section {
    min-height: 100vh;
    /* background: linear-gradient(45deg, #e91e63, #fffde7); */
    background: linear-gradient(45deg, darkorange, #fffde7);
    display: flex;
    justify-content: center;
    align-items: center;
  }
  article {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    width: 350px;
    height: 350px;
    background: #f1f3f4;
    box-shadow: 0 50px 80px rgba(0, 0, 0, 0.25);
  }
  figure {
    position: relative;
    width: 100%;
    height: 350px;
  }
  img {
    position: absolute;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    object-fit: cover;
  }
  audio {
    width: 100%;
    outline: none;
    display: block;
  }
</style>

<section id="audio">
  <article>
    <figure>
      <img src="assets/{image}" alt="Background" />
    </figure>
    <audio controls loop>
      <source src={source} type="audio/mp3" />
    </audio>
  </article>
</section>
