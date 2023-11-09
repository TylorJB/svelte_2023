<script>
    import Nav from '$lib/Nav.svelte'; //created nav first then imported it in header to put it all together
</script>

<style>
    .scary-logo{
        width: 200px;
        height: 200px;
    }

</style>

<header>
    <title> Pretty Nuts</title>
    <div class= 'nav-logo'>       
        <img src="/img/SoScary-logos_transparent.png" class="scary-logo"/>    
        <Nav/>
    </div>
</header>





