<script>
  let year = new Date().getFullYear();
  export let legal = "Copyright © " + year + ". All Rights reserved.";
  export let attribution = "Tom Foolery";
  export let attrLink = "https://mehder.com/";
</script>

<style>
  footer {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    margin-top: 4em;
    background-color: #111;
    color: #f1f1f1;
  }
  p {
    margin: 2em;
  }
  a {
    color: dodgerblue;
    text-decoration: none;
    font-weight: bold;
    font-size: 16px;
  }
  a:hover {
    text-decoration: underline;
  }
</style>

<footer>
  <p>{legal}</p>
  <p>
    Developed by
    <a href={attrLink} target="_blank">{attribution}</a>
  </p>
</footer>
