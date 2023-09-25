<template>
    <div id="header">
        <ul>
            <li><a href="#">Home</a></li>
            <li><a href="#">My Account</a></li>
        </ul>
    </div>
</template>

<style scoped>
#header {
    background-color: rgb(55, 107, 55);
    color: white;
}

ul {
    list-style-type: none;
    display: inline-flex;
    column-gap: 2rem;
}

a {
    /* color:unset; */
    color: rgb(230, 230, 230);
    text-decoration: none;
    transition: all ease-out 100ms;
}

a:hover {
    color: white;
    text-shadow: white 0 0 10px;
}
</style>