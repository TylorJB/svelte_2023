<style>
    nav
    {
        display:flex ;
        justify-content:center;
        flex-wrap: wrap;    
        overflow: hidden;
        /* width:100%; */
    }
    nav a
    {
        text-decoration: none;    
        text-align: center;  
    }
    
    .nav-words :hover{
        background-color: #17d8ce!important;
        color: black;
    }


    nav ul{/*This arranges the 4 words into landscape instead of a vertical row*/
        display:flex;
        list-style:none;
        margin:0;
        padding:0;
    }

    nav ul li a div, nav > div {/*This spaces the 4 words(padding) so they arent squished together*/
        padding: 15px 25px;
    }

</style>

<nav>
    <ul class="nav-words">   
        <li>    
            <a id="more-info" href= "/more-info" >
                <div>More Info</div>
            </a> 
        </li>    
        <li>        
            <a id="gallery" href="https://www.google.com/search?q=foxy+fnaf&tbm=isch&ved=2ahUKEwjUnbz6r7yAAxUVo-kKHUY4BucQ2-cCegQIABAA&oq=foxy+fnaf&gs_lcp=CgNpbWcQAzIHCAAQigUQQzIHCAAQigUQQzIHCAAQigUQQzIHCAAQigUQQzIHCAAQigUQQzIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEOgYIABAHEB5QwgxYvxlg_RtoAHAAeACAAbUBiAGWDJIBAzAuOZgBAKABAaoBC2d3cy13aXotaW1nwAEB&sclient=img&ei=HXXJZJSbNZXGpgfG8Ji4Dg&bih=963&biw=1903&rlz=1C1GCEB_enNZ1069NZ1069&hl=en-US" >
                <div>Gallery</div>
            </a> 
        </li>
        <li>        
            <a id="terror" href="https://www.google.com/search?rlz=1C1GCEB_enNZ1069NZ1069&q=freddy+fnaf&tbm=isch&source=lnms&sa=X&ved=2ahUKEwiPrdCrr7yAAxULgFYBHfWzDb8Q0pQJegQIChAB&biw=1920&bih=963&dpr=1" >
                <div>Terror</div>
            </a> 
        </li>
        <li>
            <a id="home" href="/" >
                <div>Home</div>
            </a> 
        </li>
   </ul>
</nav>