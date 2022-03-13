<script>
  import "../app.css"
  import Navbar from "../lib/Navbar.svelte"
</script>

<Navbar links={[{name: "Log In", url: "/log-in"}]}/>
<slot></slot>