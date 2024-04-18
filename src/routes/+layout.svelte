<script>
    import Header from "$lib/header.svelte";
</script>

<body>
    <Header />
    <section>
        <slot />
    </section>
</body>

<style>
    body {
        background-color: black;
    }

    section {
        position: absolute;

        top: calc(1vh + calc(2vh + 2em)); bottom: 1vh; left: 1vh; right: 1vh;
    }
</style>