<script setup>
    defineProps({
        socialIcon: String,
        socialUser: String,
        socialTotal: Number,
        of: String,
        arrowIcon: String,
        totalToday: Number,
    })
</script>

<template>
    <article>
        <div class="social-group">
            <img :src="socialIcon" alt="" />
            <p>{{ socialUser }}</p>
        </div>
        <div class="social-total">
            <h2>{{ socialTotal }}</h2>
            <p>{{ of }}</p>
        </div>
        <div class="total-today">
            <img :src="arrowIcon" alt=""/>
            <p class="total-p">{{ totalToday }} <span>Today</span></p>
        </div>
    </article>
</template>


<style scoped>
article {
    width: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    text-align: center;
    row-gap: 1rem;
    color: var(--Text);
    background-color: var(--CardBG);
    padding: 1.5rem;
    border-radius: .4rem;
}

.social-group {
    display: flex;
    align-items: center;
    column-gap: .5rem;
}

h2 {
    font-size: 3rem;
}

.social-total p {
    text-transform: uppercase;
    letter-spacing: .2rem;
    font-size: .8rem;
    color: var(--GrayText);
    margin-top: .5rem;
}

.total-today {
    display: flex;
    align-items: center;
    column-gap: .3rem;
}

.total-today p {
    font-size: .8rem;
    font-weight: 700;
}

@media screen and (min-width: 900px) {

    article {
        padding: 1.5rem 4rem;
        margin: 0;
    }

    article:hover {
        background-color: var(--BG-Hover);
        cursor: pointer;
    }
}

</style>
