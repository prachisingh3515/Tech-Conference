 

<script>
    import "../lib/styles.css";
    let isOpen = false;
</script>

<nav>
    <div class="nav-container">
        <div class="logo">TechConf</div>
        <button class="menu-toggle" on:click={() => (isOpen = !isOpen)}>
            ☰
        </button>
        <ul class:isOpen={isOpen}>
            <li><a href="/">Home</a></li>
            <li><a href="/speakers">Speakers</a></li>
            <li><a href="/schedule">Schedule</a></li>
            <li><a href="/sponsors">Sponsors</a></li>
            <li><a href="/about">About</a></li>
            <li><a href="/contact">Contact</a></li>
        </ul>
    </div>
</nav>

<slot />


