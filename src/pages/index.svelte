<script>
    import { metatags, page } from '@roxi/routify';
    import { onMount } from "svelte";
    metatags.title = 'My Routify app'
    metatags.description = 'Description coming soon...'

    let photo = "./static/image-welcome.jpg"

    import Header from "../components/Header.svelte"; 
    import Welcome from "../components/Welcome.svelte";  
    import Featured from "../components/Featured.svelte";

    onMount(() => {
        console.log($page)
    })
</script>

<Header/>
<Welcome/>
<Featured/>