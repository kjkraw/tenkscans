<script>
  import Navbar from './lib/Navbar.svelte'
</script>

<main>
  <Navbar/>
  <div id="content">
    <section id="hero">
      <h1>Quarterly and Annual Financial Reports</h1>
      <h2>Gathered, processed, and stored in one easy-to-use database</h2>
      <div style="display: flex; flex-direction: row; justify-content: space-evenly; width: 100%; margin: 1.5rem 0;">
        <a href="#" class="button">Learn more</a>
        <a href="#" class="button primary">See pricing</a>
      </div>
    </section>
    <section id="about">
      <h1>Features</h1>
      <h1>Use Cases</h1>
    </section>
    <section id="pricing">
    </section>
  </div>
</main>

<style>
    :root {
        --primary-bg-color: blue;
        --primary-text-color: white;

        font-family:  Roboto, sans-serif;
    }

    #hero {
        padding: 25% 0;
    }

    #hero h1 {
        font-size: 2.75rem;
        margin: 0;
    }

    #hero h2 {
        font-size: 2rem;
        margin: 0;
    }

    a.button {
        padding: 0.5rem;
        border-radius: 0.25rem;

        box-shadow: black 2px 2px;
    }

    .primary {
        background-color: var(--primary-bg-color);
        color: var(--primary-text-color);
    }

    h1 {
        font-size: 2rem;
        font-weight: bold;
        font-variant-caps: small-caps;
        text-align: center;
        margin: 1rem;
    }

    h2 {
        font-size: 1.5rem;
        font-weight: normal;
        font-variant-caps: normal;
        text-align: center;
    }

    #content {
        display: flex;
        flex-direction: column;
        justify-items: center;
        width: 100%;
    }

    #hero {
        display: flex;
        flex-direction: column;
        justify-items: center;
    }

    @media (min-width: 480px){
        h1 {
            font-size: 2.25rem;
        }

        #hero h1 {
            font-size: 4rem;
        }
    }
</style>
