<style>
  section {
    margin: 4em;
  }
  form {
    padding: 4em;
    box-shadow: 0px 10px 20px rgba(0, 0, 0, 0.2);
    font-weight: bold;
  }
  h3 {
    text-align: center;
    color: darkorange;
    font-size: 2em;
  }
  label {
    color: #333;
  }
  label,
  input,
  textarea {
    display: block;
    margin: auto;
    width: 400px;
  }
  input,
  textarea {
    margin-top: 0.5em;
    padding: 1em;
  }
  div {
    margin: 1em 0;
  }
  input[type="submit"] {
    background: darkorange;
    color: #fff;
    outline: none;
    border: none;
    padding: 1.5em 2em;
    font-size: 20px;
    text-transform: uppercase;
    letter-spacing: 1px;
    transition: 0.2s ease-in-out;
  }
  input[type="submit"]:hover {
    transform: scale(0.99);
    transition: 0.2s ease-in-out;
  }
</style>

<section id="contact">
  <form on:submit|preventDefault>
    <h3>Send Us A Message</h3>
    <div>
      <label for="name">Name</label>
      <input type="text" name="name" />
    </div>
    <div>
      <label for="email">Email</label>
      <input type="email" name="email" />
    </div>
    <div>
      <label for="message">Message</label>
      <textarea name="message" cols="30" rows="10" />
    </div>
    <div>
      <input type="submit" />
    </div>
  </form>
</section>
