<template>
    <div class="card">
        <div class="card__title">
            {{ title }}
        </div>
        <div class="card__content">
            <slot/>
        </div>
    </div>
</template>

<script>
    export default {
        name: 'card',
        props: {
            title: {
                type: String,
                required: true
            }
        }
    };
</script>

<style lang="scss" scoped>

    .card {
        --card-title-bg-color: coral;

        margin: 1rem;
        box-shadow: 0 3px 6px rgba(0, 0, 0, 0.16), 0 3px 6px rgba(0, 0, 0, 0.23);
        background-color: white;
        flex-grow: 1;

        &__title {
            padding: 1rem;
            font-weight: bold;
            background-color: var(--card-title-bg-color)
        }
        &__content {
            padding: 1rem;
        }
    }
</style>
