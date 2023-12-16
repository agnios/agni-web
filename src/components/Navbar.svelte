<script>
    import { page } from '$app/stores';
</script>

<style>
    nav ul li {
        transition: color 0.3s ease-in-out;
    }

    nav ul li:hover {
        color: #FFA500;
    }
</style>

<header>
    <nav>
        <ul class="flex flex-row items-center justify-end gap-5 text-white py-2 px-24 font-semibold  text-md">
            <li class:active={$page.url.pathname === '/docs'}>
                <a href="/docs">Documentation</a>
            </li>
            <li class:active={$page.url.pathname === '/downloads'}>
                <a href="/downloads">Downloads</a>
            </li>
            <li class:active={$page.url.pathname === '/'}>
                <a href="/">Home</a>
            </li>
            <li class:active={$page.url.pathname === '/about'}>
                <a href="/about">About Us</a>
            </li>
        </ul>
    </nav>
</header>
