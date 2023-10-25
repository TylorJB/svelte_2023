<svelte:head>
    <link rel="stylesheet" href="css/main.css" />
</svelte:head>

<script>//it worked
import { onMount } from "svelte";

let imgs = [];
const BASE_URL = "https://api.unsplash.com"

onMount(async () => {
    const res = await fetch (`${BASE_URL}`);
    let data = await res.json();
    imgs = data.results;
});
</script>

<div class="container">

    <div class="row">
        <div class= "gallery">
            <div class="gallery-block">
                <img src="" class="gallery-image">
            </div>
        </div>
        <div class= "gallery">
            <div class="gallery-block">
                <img src="" class="gallery-image">
            </div>
        </div>
        <div class= "gallery">
            <div class="gallery-block">
                <img src="" class="gallery-image">
            </div>
        </div>
        <div class= "gallery">
            <div class="gallery-block">
                <img src="" class="gallery-image">
            </div>
        </div>


    </div>



</div>


<!-- <div class="container">
    <div class="item item-1">1</div>
    <div class="item item-2">2</div>
    <div class="item item-3">3</div>
    <div class="item item-4">4</div>
</div>

<div class="page1">
    <div class="top"></div>
    <div class="bottom"></div>
</div>

<div class="outside">
    <div class="text">
        yoyoyoyoyoy
    </div>
    <div class="pics">
        <div class = "pic1">
            <img src = "/img/Man-with-Well-Groomed-Beard.jpg">/img/SoScary-logos_transparent.png
        </div>
        <div class = "pic2">
        </div>

    </div> -->

   

