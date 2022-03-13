<script>
  let screenWidth;
  $: hidden = screenWidth <= 480;
</script>

<svelte:window bind:innerWidth={screenWidth}/>

<nav>
  <a href="/">tenkscans.com</a>
  <ul class:hidden={hidden}>
    <a href="#">Log In</a>
  </ul>
</nav>

<style>
    nav {
        display: flex;
        box-sizing: border-box;

        z-index: 10;

        width: 100%;
        max-width: 100%;
        padding: 0.5rem 1rem 0.25rem 1rem;

        flex-direction: column;
        gap: 1rem;

        background-color: var(--primary-bg-color);
    }

    a {
        color: var(--primary-text-color);
        text-decoration: none;
    }

    nav a {
        font-size: 2rem;
        font-variant-caps: unicase;
    }

    ul {
        display: flex;
        flex-direction: column;
        padding: 0;
        margin: 0;
    }

    ul.hidden {
        display: none;
    }

    ul a {
        font-size: 1.25rem;
        font-variant-caps: normal;
    }


    @media (min-width: 480px) {
        nav {
            flex-direction: row;
            align-items: baseline;
            justify-content: space-between;
        }

        nav a {
            font-size: 2.5rem;
        }

        ul {
            visibility: visible;
            flex-direction: row;
            align-items: baseline;
            justify-content: end;
            row-gap: 1rem;
        }

        ul a {
            font-size: 1.5rem;
        }
    }
</style>
