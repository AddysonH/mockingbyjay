<template>
    <div class="sidelineColor">
        <h1>Hello World</h1>
    </div>
</template>
<script>

export default ({
    name:"sideLine"
})
</script>
<style>
.sidelineColor{
background-color: #111;
position: absolute;
top: 50%;
left: 50%;
transform: translate(-50%, -800%);
width:100%;
z-index:0;
}
</style>
