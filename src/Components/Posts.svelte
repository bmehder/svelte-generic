<script>
  export let endpoint = "https://jsonplaceholder.typicode.com/posts?userId=1";

  async function getData() {
    const res = await fetch(endpoint);
    const data = await res.json();
    console.log(data);
    if (res.ok) {
      return data;
    } else {
      throw new Error(data);
    }
  }
  let promise = getData();
</script>

<style>
  section {
    margin: 4em 0 0;
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    padding: 2em;
    background: radial-gradient(black 15%, transparent 16%) 0 0,
      radial-gradient(black 15%, transparent 16%) 8px 8px,
      radial-gradient(rgba(255, 255, 255, 0.1) 15%, transparent 20%) 0 1px,
      radial-gradient(rgba(255, 255, 255, 0.1) 15%, transparent 20%) 8px 9px;
    background-color: #282828;
    background-size: 16px 16px;
  }

  article {
    width: 45%;
    margin: 2em 0;
    padding: 1em 2em 3em;
    background: #fff;
    border-left: 0.5em solid darkorange;
    border-radius: 5px;
  }

  h3 {
    margin: 1em auto 1em;
    color: darkorange;
    text-align: center;
    font-size: 2em;
    width: 100%;
    /* text-shadow: 3px 3px 5px rgba(0, 0, 0, 0.3); */
  }

  h4 {
    display: flex;
    align-items: center;
    margin: 1em 0 0.25em 20px;
    font-size: 1.5em;
    text-transform: capitalize;
  }

  a {
    color: dodgerblue;
    font-weight: bold;
    text-decoration: none;
  }

  a:hover {
    color: darkorange;
    border-bottom: 1px solid darkorange;
    border-bottom: 0;
  }

  img {
    width: 110px;
    height: 110px;
    margin-right: 15px;
    border: 1px solid #555;
  }

  p {
    margin: 1em 0 0 20px;
    line-height: 1.5em;
    color: #444;
  }
  small {
    padding: 0 0 0 20px;
    font-style: italic;
  }
</style>

{#await promise}

  <p>...loading</p>

{:then data}

  <section id="blog">
    <h3>Recent News</h3>
    {#each data as chunck}
      <article>
        <h4>
          <img
            src="https://source.unsplash.com/random/120x120"
            alt="featured post" />
          <a href="/">{chunck.title}</a>
        </h4>

        <small>
          by
          <a href="/">Tom Foolery</a>
          on February 30, 2020
        </small>

        <p>
          {chunck.body}...
          <a href="/">[Read More]</a>
        </p>
      </article>
    {/each}
  </section>

{:catch error}

  <p>Something has gone horribly wrong. :-(</p>
  <p style="color: red">{error.message}</p>

{/await}
