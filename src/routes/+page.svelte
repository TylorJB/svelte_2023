<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
    import { onMount } from "svelte";

    let imgs = [];
    let imgs2 = [];

    const BASE_URL = "https://api.unsplash.com";

    onMount(async () => {
        const res = await fetch (`${BASE_URL}/search/photos?query=scary&per_page=12&client_id=xvfLv8hfT8I1-MCioaETe-GF6N1-CpdiS_I4LXHYSi0`);
        let data = await res.json();
        imgs = data.results;
  
        const res2 = await fetch (`${BASE_URL}/search/photos?query=zombie-dead&per_page=1&client_id=xvfLv8hfT8I1-MCioaETe-GF6N1-CpdiS_I4LXHYSi0`);
        let data2 = await res2.json();
        imgs2 = data2.results;
    });
</script>

<div class="first-box">
    <div class="reviews">
        <div class="intro1">
            {#each imgs2 as img, index}
                <img src={img.urls.regular} alt="intro" class="intro2">
            {/each}
        </div>
        <div class="intro3">
            <p>Welcome to the Abyss of Fear, a virtual realm where the darkest corners of your imagination come to life. This is not a place for the faint of heart or the easily spooked, but rather an immersive journey into the chilling unknown. </p>
        </div>
    </div>
</div>

<div class= "scary-gallery-background">
    <div class= "scary-gallery">
        <h1>Scary Gallery</h1>
    </div>  
</div>
<div class="container">
    <div class="row">
        <div class= "gallery">
            <class class="gallery-block">
                {#each imgs as img, index}
                <img src={img.urls.regular} alt="PetPics" class="gallery-image">
                {/each}
            </class>
        </div>
    </div>
</div>


<style>
    @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap');

    .first-box{
        background-color: rgb(31, 30, 30);
    }

    .reviews{
        display: flex;
        align-items: center;
    }

    .intro1{
        margin-top: 20px;
        margin-bottom: 20px;
        margin-left: 20px;   
    }

    .intro2{
        width: 700px;
        height: 500px;
    }

    .intro3{
        color: white;
        margin-left: 20px;
        margin-right: 20px;
        font-family: 'Bebas Neue', sans-serif;
        font-size: 24px;
    }
</style>



   

