<script>
  export let heading = "Title Heading";
</script>

<style>
  article {
    padding: 2em 4em;
    line-height: 1.5em;
    color: #333;
  }
  div {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
  }
  p,
  ul {
    font-size: 20px;
    line-height: 1.5em;
  }
  ul {
    margin: 1em 0 2.5em;
  }
  a {
    margin: 0;
    width: 40%;
    padding: 1.5em 2em;
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
  }
  a:hover {
    box-shadow: 0px 5px 30px rgba(0, 0, 0, 0.1),
      inset 0px 5px 30px rgba(0, 0, 0, 0.1);
  }
</style>

<section id="about">
  <article>
    <h1>{heading}</h1>
    <p>
      <slot />
    </p>
    <div>
      <ul>
        <li>Lorem, ipsum dolor.</li>
        <li>Lorem ipsum dolor sit amet consectetur.</li>
        <li>Lorem ipsum dolor sit amet.</li>
        <li>Lorem, ipsum dolor.</li>
        <li>Lorem ipsum dolor sit amet consectetur.</li>
        <li>Lorem ipsum dolor sit amet.</li>
      </ul>
      <a href="/" class="button">Call To Action Button</a>
    </div>
  </article>
</section>
