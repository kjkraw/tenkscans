<script></script>

<nav>
  <a href="/">tenkscans.com</a>
  <ul>
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
        padding: 0.5rem 1rem;

        flex-direction: column;
        gap: 1rem;

        background-color: blue;
    }

    a {
        color: white;
        text-decoration: none;
    }

    nav a {
        font-size: 2rem;
    }

    ul {
        display: flex;
        flex-direction: column;
        padding: 0;
    }

    ul a {
        font-size: 1.25rem;
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
            gap: 1rem;
        }

        ul a {
            font-size: 1.5rem;
        }
    }
</style>
