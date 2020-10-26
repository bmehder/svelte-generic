<script>
  export let endpoint =
    "https://raw.githubusercontent.com/bmehder/projects/master/json/covid.json";

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
    margin: 4em 4em 6em;
    padding: 2em 4em;
    border: 1px solid #e1e1e1;
    border-radius: 5px;
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
  }
  h3 {
    margin-bottom: 2em;
  }
  article {
    display: flex;
    justify-content: space-around;
    padding: 1em 0;
  }
  article:nth-child(odd) {
    background-color: #fff;
  }
  article:nth-child(even) {
    background-color: #f1f1f1;
  }
  article div {
    flex-basis: 25%;
    line-height: 2em;
    padding-left: 3em;
  }
  .heading {
    background-color: darkorange !important;
    color: #fff;
  }
  p {
    display: flex;
    justify-content: center;
    margin: 1em 0;
    text-align: center;
  }
  a {
    color: dodgerblue;
    text-decoration: none;
  }
  a:hover {
    color: darkorange;
    border-bottom: 1px solid darkorange;
  }
</style>

<section id="reports">
  {#await promise}

    <p>...loading</p>

  {:then data}

    <h3>Data fetched from remote JSON file</h3>
    <article class="heading">
      <div>
        <strong>Business</strong>
      </div>
      <div>
        <strong>Address</strong>
      </div>
      <div>
        <strong>Category</strong>
      </div>
      <div>
        <strong>Rating</strong>
      </div>
    </article>
    {#each data as chunck, i}
      <article>
        <div>{chunck.business}</div>
        <div>{chunck.address}</div>
        <div>{chunck.cat}</div>
        <div>{chunck.rating}%</div>
      </article>
    {/each}
    <p>
      <small>
        <a
          href="https://raw.githubusercontent.com/bmehder/projects/master/json/covid.json"
          target="_blank">
          https://raw.githubusercontent.com/bmehder/projects/master/json/covid.json
        </a>
      </small>
    </p>

  {:catch error}

    <p>Something has gone horribly wrong. :-(</p>
    <p style="color: red">{error.message}</p>

  {/await}

</section>
