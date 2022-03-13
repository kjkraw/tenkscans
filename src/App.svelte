<script>
  import Navbar from './lib/Navbar.svelte'
</script>

<main>
  <Navbar/>
  <section id="hero">
    <h1>Annual Financial Reports</h1>
    <h2>in an all-in-one, easy-to-use database</h2>
  </section>
  <section id="use-cases">
    <h1>Use Cases</h1>
    <ul>
      <li>Scan recent reports for highly performing companies</li>
      <li>Automate in-depth research on specific companies</li>
      <li>Backtest investment strategies with financial data dating back to 2010</li>
    </ul>
  </section>
  <section id="pricing">
    <!--Pricing elements-->
  </section>
</main>

<style>
    :root {
        --primary-bg-color: blue;
        --primary-text-color: white;

        font-family:  Roboto, sans-serif;
    }
</style>
