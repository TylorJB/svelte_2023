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
    
    .nav-words :hover{ /*adds a neat hover effect when the cursor moves over the words*/
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
            <a id="terror" href="https://www.google.com/search?q=cute+puppy&tbm=isch&ved=2ahUKEwiLj__brriCAxU45DgGHe_DBskQ2-cCegQIABAA&oq=cute+puppy&gs_lcp=CgNpbWcQAzIFCAAQgAQyBwgAEIoFEEMyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDIFCAAQgAQyBQgAEIAEMgUIABCABDoKCAAQigUQsQMQQzoICAAQgAQQsQM6BggAEAUQHjoGCAAQCBAeOgkIABAYEIAEEApQlghYmTNgiDRoBHAAeACAAb4BiAHVEJIBBDAuMTKYAQCgAQGqAQtnd3Mtd2l6LWltZ8ABAQ&sclient=img&ei=r5JNZcv7I7jI4-EP74ebyAw&bih=963&biw=1920&rlz=1C1GCEB_enNZ1069NZ1069" >
                <div>Click Here for Terror</div>
            </a> 
        </li>
        <li>
            <a id="home" href="/" >
                <div>Home</div>
            </a> 
        </li>
   </ul>
</nav>