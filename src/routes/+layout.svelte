<script>
    import '../styles.css';
    import logo from '$lib/images/logo.svg';
    import tmdb from '$lib/images/tmdb.svg';
</script>
<nav>
    <a href = "/">
        <img src={logo} alt="SvelteFlix Logo">
    </a>

    <div class="links">
        <a href = "/search">About</a>
        <a href = "/watchlist">watch List</a>
        <a href = "/login">Login</a>
    </div>
</nav>

<main>
    <slot />
</main>


<footer>
    <a href="https:www.moviedb.org/">
        Data Provided by
        <img src={tmdb} alt="footer"> 
    </a>
</footer>
<style>
    nav {
        display: flex;
        width: 100%;
        height: 3rem;
        font-family: system-ui, -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen, Ubuntu, Cantarell, 'Open Sans', 'Helvetica Neue', sans-serif;
        align-items: center;
        justify-content: space-between;
        max-width: var(--column);
        padding: 0 var(--side);
        color :var(--accent);
    }

    a{
        color: inherit;
        text-decoration: none;
    }

    img{
        height: 1.5rem;
        margin-top: 30px;
    }

    .links {
        display: flex;
        gap: 1rem;
    }

    footer {
        display: flex;
        justify-content: center;
        height: 2rem;
    }
</style>