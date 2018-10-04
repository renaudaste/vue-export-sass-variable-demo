<template>
    <div class="home">
        <template v-for="i in 6">
            <card :key="i" :title="getTitle(i)">
                <div>{{ getLabel(i) }}</div>
            </card>
        </template>
        <card :title="getTitle(7)" :style="{'--card-title-bg-color': getColor()}">
            <div>{{ getLabel(7) }}</div>
        </card>
    </div>
</template>

<script>
    import Card from './card.component';
    import styles from '../styles.scss'
    export default {
        name: 'home',
        components: { Card },
        methods: {
            getTitle(i) {
                return `Card n°${i}.`;
            },
            getLabel(i) {
                return `Super contenu de la card n°${i}.`;
            },
            getColor () {
                return styles['osb-green']
            }
        }
    };
</script>

<style lang="scss" scoped>
    $test: red;
    .home {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
    }
</style>
