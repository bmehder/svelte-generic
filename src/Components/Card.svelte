<script>
  export let title = "Title";
  export let subtitle = "Subtitle";
  export let description = "This is a short description right here.";
  export let img = "https://picsum.photos/300/200";
  export let link = "/";
  export let buttonText = "Learn More";
</script>

<style>
  article {
    width: 300px;
    height: auto;
    margin: 4em 0;
    background: #fff;
    /* border: 1px solid #e1e1e1; */
    border-radius: 5px;
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
    text-align: center;
  }
  h4,
  h5,
  p,
  a {
    margin: 1em;
  }
  h4 {
    font-size: 2em;
  }
  h5 {
    color: darkorange;
    font-size: 1.25em;
  }

  a {
    display: block;
    background: dodgerblue;
    color: #fff;
    font-weight: bold;
    padding: 1em 2em;
    border-radius: 4px;
    text-decoration: none;
    transition: 0.3s ease-in-out;
  }
  a:hover {
    transform: scale(0.98);
  }
</style>

<article>
  <img src={img} alt="Hero" />
  <h4>{title}</h4>
  <h5>{subtitle}</h5>
  <p>{description}</p>
  <a href={link} class="button">{buttonText}</a>
</article>
