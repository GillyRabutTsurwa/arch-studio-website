<script>
        import { page } from '@roxi/routify';
        import Navigation from "../components/shared/Navigation.svelte";
        import Footer from "../components/Footer.svelte";
        $: currentPageTitle = $page.title === "index" ? "home" : $page.title;
</script>

<Navigation pageTitle={currentPageTitle}/>

<!-- routify:options preload="proximity" -->
<slot />
<Footer/>
