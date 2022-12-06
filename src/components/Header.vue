<template>
    <div class="header">
        <div class="title_image">
            <img src="../assets/unh.png" />
        </div>
        <div class="title-title">
            <h2>Find Dev</h2>
        </div>
    </div>

</template>
<script>
export default {
    name: 'HeaderTop',

}

</script>
<style >
.header {
    margin: 0 !important;
    grid-area: nav;
    background-color: #2d547e;

}



.title-title h2 {
    padding: 10px;
    color: #ffffff;
    display: inline;
}

.title_image img {
    padding: 10px;
    display: inline;
    width: 120px;
    height: 100px;
}
</style>