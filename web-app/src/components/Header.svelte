<script>
import {
    page
} from '$app/stores';
</script>

<header class="flex justify-between p-4">
    <div class="text-3xl font-bold text-white">
        Sub-manager
    </div>

    <!-- <nav>
        <ul class="flex gap-4">
            <li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
                <a class="hover:text-gray-300 text-white" href="/">Home</a>
            </li>
            <li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
                <a class="hover:text-gray-300 text-white" href="/about">Compenents Testing</a>
            </li>
        </ul>
    </nav> -->
</header>

<style>
nav {
    display: flex;
    justify-content: center;
}

ul {
    position: relative;
    padding: 0;
    margin: 0;
    height: 3em;
    display: flex;
    justify-content: center;
    align-items: center;
    list-style: none;
    background: var(--background);
    background-size: contain;
}

li {
    position: relative;
    height: 100%;
}
</style>
