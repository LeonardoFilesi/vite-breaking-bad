<script>
import AppCard from "./AppCard.vue"


export default {
    name: "AppMain",
    components: {
        AppCard,
    }
}
</script>

<template>
    <div class="wrapper-main">
        <div class="wrapper-container ">
            <section class="container">
                <select class="mb-4"  name="" id="">
                    <option value="">Alien</option>
                    <option value="">Ally of Justice</option>
                    <option value="">Ancient Gear</option>
                    <option value="">All</option>
                </select>

                <AppCard />
            </section>
        </div>
    </div>
</template>

<style scoped lang="scss">
@use "../styles/partials/variables" as *;


.wrapper-main {
    width: 100%;
    background-color: $maincolor;
    section {
        padding: 40px 0 0 0;
        select {
            width: 180px;
        }
    }
}
</style>
