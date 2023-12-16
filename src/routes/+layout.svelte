<script>
    import "../app.css";
    import Downloads from "../components/DownloadsCard.svelte";
    import Cards from "../components/Cards.svelte";
    import Intro from "../components/Hero.svelte";
    import Footer from "../components/Footer.svelte";
</script>


<div class="h-screen">
    <Intro />
    <div class="">
    <Downloads />
        <Cards />
        <Footer />
    </div>
    <slot />
</div>
