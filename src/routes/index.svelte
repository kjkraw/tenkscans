<script lang="ts">
    import {onMount} from "svelte"

    let mounted = false

    onMount(() => {
        mounted = true
    })
</script>

<section id="hero">
  <div>
    <h1>Quarterly and Annual Financial Reports</h1>
    <h2>Processed and saved into one easy-to-use database for efficient stock scans</h2>
  </div>
  <div id="hero-buttons">
    <a href="/">learn more</a>
    <a href="/">view pricing</a>
  </div>
</section>
<div id="content">
  <section id="about">
    <h1>Features</h1>
    <h1>Use Cases</h1>
  </section>
  <section id="pricing">
    <h1>Pricing</h1>
  </section>
</div>

<style>
    :root {
        --hero-top: env(safe-area-inset-top);
        --hero-height: 78%;

        --z-index-bg: 1;
        --z-index-hero: 5;
        --z-index-content: 6;
    }

    #hero {
        position: fixed;
        top: var(--hero-top);
        left: 0;
        z-index: var(--z-index-hero);
        padding: 5%;

        height: var(--hero-height);
        width: 100%;
        box-sizing: border-box;

        display: flex;
        flex-direction: column;

        align-items: center;
        justify-content: center;
        gap: 10rem;
    }

    #hero h1 {
        margin: 0;
        text-align: left;
    }

    #hero h2 {
        margin: 0;
        color: white;
    }

    #hero-buttons {
        display: flex;
        flex-direction: row;
        align-items: center;
        width: 100%;
        justify-content: space-around;
    }

    #hero-buttons a {
        background-color: var(--theme-light-blue);
        color: var(--theme-black);
        text-decoration: none;
        font-variant-caps: small-caps;
        padding: 0.5rem;
        font-size: 1.25rem;
        border-radius: 0.5rem;
        box-shadow: -2px 2px 2px var(--theme-black);
    }

    #content {
        position: absolute;
        top: calc(var(--hero-height) + var(--hero-top));
        z-index: var(--z-index-content);
        width: 100%;
        background-color: var(--theme-black);
    }

    h1 {
        color: white;
        font-weight: bold;
        font-size: 2.5rem;
        text-align: center;
    }

    @media (min-width: 480px) {
        #hero {
            padding: 5%;
        }

        #hero-buttons {
            justify-content: center;
            gap: 4rem;
        }

        #hero-buttons a {
            font-size: 1.5rem;
        }

    }
    @media (min-width: 1024px) {
        #hero h1 {
            text-align: center;
        }
    }
</style>