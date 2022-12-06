<template>

    <div class="card">
        <h2>{{ proj.title }}</h2>
        <span> username:
            <b>{{ proj.username }}</b>
        </span>
        <hr />
        <img :src="proj.image" /><br />
        <div class="tags" v-for="tags in proj.tags" :key="tags">
            {{ tags }}
        </div>
        <hr />
        <div class="desc">
            <b>Description:</b>{{ proj.description }}
        </div>
        <div class="links">
            <a v-bind:href="proj.source_code_link" target="_blank">Source Code</a>&nbsp;
            <a v-bind:href="proj.deployed_link" target="_blank">Deploy Link</a>

        </div>

    </div>

</template>

<script>


export default {
    name: 'ProjectItem',
    props: {
        proj: Array
    }

}


</script>

<style>
h4 {
    margin: 2px;
}

.card h2,
.card span {
    padding: 8px;
}

.card img {
    width: 400px;
    height: 250px;
    margin-bottom: 15px;
}

.card .links {
    padding: 8px;

}

.card .links a {
    text-decoration: none;
    padding: 10px;
    border: 1px solid #2C547E;
    border-radius: 10px;
    border-color: #2C547E;
}

.card .links a:hover {
    background-color: #2C547E;
    color: #ffffff;
}

.card {
    float: left;
    box-shadow: 0 4px 8px 0 rgb(0 0 0 / 20%);
    margin: 20px;
    height: 600px;
    width: 400px;
}

.tags {
    margin-top: 20px;
    display: inline;
    padding: 5px;
    border-radius: 30px;
    border: 1px solid #179AB4;
}

.desc {
    margin-top: 10px;
    padding: 10px;
}
</style>