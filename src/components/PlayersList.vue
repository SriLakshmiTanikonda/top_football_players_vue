<template>
    <div class="players-list">
        <div v-for="player of players" :key="player.id">
            <SinglePlayer :player=player />
        </div>
    </div>
</template>
<script>
import SinglePlayer from './SinglePlayer.vue'

export default {
    name: 'PlayersList',
    props: {
        players: Array
    },
    components: {
        SinglePlayer
    }

}
</script>
<style scoped>
.players-list {
    display: flex;
    flex-wrap: wrap;
    width: 100%;
}

.players-list div {
    width: 100%;
}
</style>
