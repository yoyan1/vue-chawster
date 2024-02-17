<script>
    const modal = document.querySelector(".nav-bar");
    const icon = document.querySelector(".icon");
    icon.addEventListener('click', function (){
       const modal_style = modal.style.display;

       if(modal_style == "grid"){
            modal.style.display = "none"; 
       } else{  
            modal.style.display = "grid";
       }
    })
</script>
<template>
    <div class="text">
            <h1>" Work hard in <b>silence</b> let <b>success</b><br> make noise "</h1>
    </div>
        <div class="footer">
            <div class="footer-wrap">
                <div class="title">
                    <h1>chawster</h1>
                </div>
                <div class="nav-bar">
                    <a href="">facebook:Roland Clarion</a>
                    <a href="">email:yoyan947@gmail.com</a>
                    <p>Powered by: Chawster</p>
                </div>
            </div>
        </div>
</template>