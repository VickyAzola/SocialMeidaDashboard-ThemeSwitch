<script setup>
    defineProps({
        socialEngagement: String,
        socialTotal: Number,
        socialIcon: String,
        arrowIcon: String,
        totalToday: Number,
    })
</script>

<template>
    <article>
        <div class="overview-1">
            <p>{{ socialEngagement }}</p>
            <h4>{{ socialTotal }}</h4>
        </div>
        <div class="overview-2">
            <img :src="socialIcon" alt="" />
            <div>
                <img :src="arrowIcon" alt="" />
                <p class="total-p">{{ totalToday }}</p>
            </div>
        </div>
    </article>
</template>

<style scoped>

article {
    width: 100%;
    height: 100%;
    display: flex;
    justify-content: space-between;
    row-gap: 1.5rem;
    background-color: var(--CardBG);
    padding: 1.5rem;
    border-radius: .4rem;
    color: var(--Text);
}

.overview-1 {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    row-gap: 1.5rem;
}

.overview-1  p {
    font-weight: bold;
}

.overview-1 h4 {
    font-size: 2rem;
}

.overview-2 {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: flex-end;
}

.overview-2 div {
    display: flex;
    align-items: center;
    column-gap: .3rem;
}

.overview-2 p {
    font-size: .8rem;
    font-weight: 700;
}

@media screen and (min-width: 900px) {
    article {
        margin: .5rem 0;
    }

    article:hover {
        background-color: var(--BG-Hover);
        cursor: pointer;
    }
}

</style>