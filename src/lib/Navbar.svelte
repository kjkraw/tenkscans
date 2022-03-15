<script lang="ts">
    export let links: { url: string, name: string }[];

    let innerWidth: number;
    $: hidden = innerWidth < 480;
</script>

<svelte:window bind:innerWidth={innerWidth}/>

<div>
  <a href="/">tenkscans.com</a>
  <!--Todo: Attach this to a button :)-->
  <nav class:hidden={hidden}>
    <ul>
      {#each links as link}
        <li><a href={link.url}>{link.name}</a></li>
      {/each}
    </ul>
  </nav>

</div>

<style>
    div {
        position: fixed;
        top: 0;
        left: 0;

        display: flex;
        width: 100%;
        box-sizing: border-box;
        padding: 1rem;
        z-index: var(--z-index-navbar);

        box-shadow: 0 2px 4px;

        flex-direction: column;
        align-items: baseline;

        background-color: var(--theme-black);
    }

    ul {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin: 0;
    }

    a {
        color: white;
        font-weight: bold;
        font-size: 2.25rem;
        text-decoration: none;
        font-variant-caps: small-caps;
    }

    li {
        list-style: none;
    }

    li a {
        font-weight: normal;
        font-size: 1.25rem;
    }

    @media (min-width: 480px) {
        a {
            font-size: 2.75rem;
        }

        li a {
            font-size: 1.5rem
        }

        div {
            flex-direction: row;
            justify-content: space-between;
        }

        ul {
            flex-direction: row;
            justify-content: end;
        }
    }
</style>