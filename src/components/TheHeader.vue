<script setup>
import Toggle from './Toggle.vue'
</script>


<template>
    <header>
        <div class="title">
            <h1>Social Media Dashboard</h1>
            <p>Total Followers: 23,004</p>
            <hr>
        </div>
        <Toggle />
    </header>
</template>


<style scoped>

header {
    padding: 2rem;
    color: var(--Text);
}

header::before {
    content: "";
    position: absolute;
    background: var(--TopBGPattern);
    min-width: 100vw;
    height: 15rem;
    right: 0;
    top: 0;
    z-index: -1;
}

.title hr {
    margin: 1rem 0;
}
.title h1 {
    font-size: 1.6rem;
    margin-bottom: .5rem;
}

@media screen and (min-width: 900px) {
    header {
        display: flex;
        justify-content: space-between;
        margin-inline: 2rem;
    }

    hr {
        display: none;
    }
}


</style>