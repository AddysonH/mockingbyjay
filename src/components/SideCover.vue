<template>
    <div class="sidenav">    
        <h1>Hello World</h1>
    </div>
</template>
<script>

export default ({
    name:"SideCover"
})
</script>

<style>
.sidenav{
    height: 100%; /* Full-height: remove this if you want " auto height */
    width: 160px; /* Set the width of the sidebar */
    position: fixed; /* Fixed sidebar (stay in place on scroll)*/
    z-index: 1; /* Stay on top */
    top: 0; /* Stay at the top */
    left: 0;
    background-color: #111; /*black */
    overflow-x: hidden; /* Disable horizontal scroll */
    padding-top: 20px;
    color: #111;
}
/* .sideCover{
background-color: rgb(34, 33, 33);
position: absolute;
color: rgb(34, 33, 33);
width: 100%;
left: 0;
height: 800px;
} */

</style>