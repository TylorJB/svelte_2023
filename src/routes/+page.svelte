<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>
    import { onMount } from "svelte";
//fetching 2 sets of data from unsplash, one with 12 images and another with a single image.
    let imgs = [];  //declared 2 empty arrays, each will store fetched data. 
    let imgs2 = []; //

    const BASE_URL = "https://api.unsplash.com";

    onMount(async () => {
        const res = await fetch (`${BASE_URL}/search/photos?query=scary&per_page=12&client_id=xvfLv8hfT8I1-MCioaETe-GF6N1-CpdiS_I4LXHYSi0`);//fetching 12 scary images from unsplash
        let data = await res.json();
        imgs = data.results; // storing the 12 images in imgs
  
        const res2 = await fetch (`${BASE_URL}/search/photos?query=zombie-dead&per_page=1&client_id=xvfLv8hfT8I1-MCioaETe-GF6N1-CpdiS_I4LXHYSi0`);
        let data2 = await res2.json();
        imgs2 = data2.results; //storing a single image in imgs2
    });
</script>

<div class="intro-container">
    <div class="intro">
        <!-- looping through imgs2 array and creates an img element for each item in array.  -->
        <div class="intro-margin">
            {#each imgs2 as img, index} lll
                <img src={img.urls.regular} alt="intro" class="intro-size">
            {/each}
        </div>
        <div class="intro-text">
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
    /* importing a bold font from google  */
    @import url('https://fonts.googleapis.com/css2?family=Bebas+Neue&display=swap'); 

    .intro-container{
        background-color: rgb(31, 30, 30);
    }

    .intro{
        display: flex;
        align-items: center;
    }

    .intro-margin{
        margin-top: 20px;
        margin-bottom: 20px;
        margin-left: 20px;   
    }

    .intro-size{
        width: 700px;
        height: 500px;
    }

/* styling text to use the imported font, adjust spacing and font colour  */
    .intro-text{  
        color: white;
        margin-left: 20px;
        margin-right: 20px;
        font-family: 'Bebas Neue', sans-serif;
        font-size: 24px;
    }
</style>



   

