<script>
  import Logo from "./pieces/Logo.svelte";
  import Nav from "./pieces/Nav.svelte";
</script>

<style>
  header {
    display: flex;
    align-items: center;
    justify-content: space-between;
    width: 100%;
    min-height: 120px;
    /* background-color: dodgerblue; */
    background: radial-gradient(
          circle at 0% 50%,
          rgba(96, 16, 48, 0) 9px,
          #613 10px,
          rgba(96, 16, 48, 0) 11px
        )
        0px 10px,
      radial-gradient(
        at 100% 100%,
        rgba(96, 16, 48, 0) 9px,
        #613 10px,
        rgba(96, 16, 48, 0) 11px
      ),
      #8a3;
    background-size: 50px 50px;
  }
</style>

<header>
  <Logo />
  <Nav />
</header>
