<script>
    import { metatags } from '@roxi/routify';
    metatags.title = 'My Routify app'
    metatags.description = 'Description coming soon...'

    let photo = "./static/image-welcome.jpg"

    import Header from "../components/Header.svelte"; 
    import Welcome from "../components/Welcome.svelte";  
    import Featured from "../components/Featured.svelte";
    import Footer from "../components/Footer.svelte";
</script>

<Header/>
<Welcome/>
<Featured/>
<Footer/>