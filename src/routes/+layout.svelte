<script>
    import Header from '$lib/Header.svelte';   /*Importing header and footer components, the header contains the navbar component as well*/
    import Footer from '$lib/Footer.svelte';    
</script>

<Header/>
<slot />
<Footer/>
