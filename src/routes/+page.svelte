<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
import { onMount } from "svelte";

let imgs = [];
const BASE_URL = "https://api.unsplash.com";

onMount(async () => {
    const res = await fetch (`${BASE_URL}/search/photos?query=scary&per_page=12&client_id=xvfLv8hfT8I1-MCioaETe-GF6N1-CpdiS_I4LXHYSi0`);
    let data = await res.json();
    imgs = data.results;
});
</script>


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



   

