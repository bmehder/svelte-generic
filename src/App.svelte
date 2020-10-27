<script>
  import Header from "./Layouts/Header/Header.svelte";
  import Hero from "./Components/Hero.svelte";
  import Footer from "./Layouts/Footer.svelte";
  import Card from "./Components/Card.svelte";
  import CTA from "./Components/CTA.svelte";
  import Article from "./Components/Article.svelte";
  import Fetcher from "./Components/Fetcher.svelte";
  import Posts from "./Components/Posts.svelte";
  import Audio from "./Components/Audio.svelte";
  import Form from "./Components/Form.svelte";
</script>

<style>
  main {
    width: 1120px;
    margin: auto;
    background: #fff;
    box-shadow: 0 10px 20px rgba(0, 0, 0, 0.2);
  }
  section {
    padding: 2em 4em 2em;
    line-height: 1.5em;
    color: #333;
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    background: radial-gradient(black 15%, transparent 16%) 0 0,
      radial-gradient(black 15%, transparent 16%) 8px 8px,
      radial-gradient(rgba(255, 255, 255, 0.1) 15%, transparent 20%) 0 1px,
      radial-gradient(rgba(255, 255, 255, 0.1) 15%, transparent 20%) 8px 9px;
    background-color: #282828;
    background-size: 16px 16px;
  }
  a {
    color: dodgerblue;
    text-decoration: none;
    font-weight: 600;
  }

  a:hover {
    border-bottom: 3px solid darkorange;
    color: darkorange;
  }
</style>

<main>
  <Header />

  <Hero id="home" />

  <Article>
    Lorem ipsum dolor sit amet consectetur, adipisicing elit. Error, assumenda!
    Omnis aperiam ad sed sequi ducimus temporibus, recusandae eum rerum
    <a href="/">sed placeat molestiae incidunt</a>
    officiis obcaecati ipsa amet consectetur ea ut eveniet. Sunt, nobis, non
    mollitia amet, maiores possimus nulla omnis? Repudiandae adipisci laudantium
    dolores impedit magnam maxime officia facilis non obcaecati, suscipit minima
    ducimus accusantium doloremque eius. Sapiente iure vitae eaque! Perspiciatis
    ab consequatur ratione eius odio officia omnis?
  </Article>

  <section id="services">
    <Card
      title="JS"
      subtitle="Programming Language"
      description="Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Laudantium, odit!"
      img="https://picsum.photos/300/201"
      link="https://apple.com/"
      buttonText="Learn More" />

    <Card
      title="APIs"
      subtitle="Microservices"
      description="Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Laudantium, odit!"
      img="https://picsum.photos/300/202"
      link="https://macrumors.com/"
      buttonText="Learn Less" />

    <Card
      title="Svelte"
      subtitle="Reactive Framework"
      description="Lorem ipsum dolor sit amet consectetur adipisicing elit.
      Laudantium, odit!"
      img="https://picsum.photos/300/203"
      link="https://svelte.dev/"
      buttonText="Less Is More" />
  </section>

  <Fetcher />

  <Posts />

  <Audio />

  <Form />

  <Footer
    legal="Copyright © 2020 Wrigley Publishing. All Rights reserved."
    attribution="Brad the Web Guy" />
</main>
