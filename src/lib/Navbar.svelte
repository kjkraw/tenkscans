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
        display: flex;
        width: 100%;
        box-sizing: border-box;
        padding: 1rem;

        flex-direction: column;
        align-items: baseline;

        background-color: var(--primary-color-bg)
    }

    ul {
        display: flex;
        flex-direction: column;
        gap: 1rem;
        margin: 0;
    }

    a {
        color: var(--primary-color-text);
        font-weight: bold;
        font-size: 2.5rem;
        text-decoration: none;
    }

    li {
        list-style: none;
    }

    li a {
        font-weight: normal;
        font-size: 1.5rem;
    }

    @media (min-width: 480px) {
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