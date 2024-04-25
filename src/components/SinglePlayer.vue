<template>
    <div class="player-container">
        <div class="img-container">
            <img class="playerimage" width="150" height="150" :src="player.image" alt="">
        </div>
        <div class="player-details">
            <h2 class="player-name">{{ player.name }}</h2>
            <table>
                <tr>
                    <th>Nationality : </th>
                    <td>{{ player.nationality }}</td>
                </tr>
                <tr>
                    <th>Clubs :</th>
                    <td>{{ player.clubs }}</td>
                </tr>
                <tr>
                    <th>Goals :</th>
                    <td>{{ player.goals }}</td>
                </tr>
                <tr>
                    <th>Matches :</th>
                    <td>{{ player.matches }}</td>
                </tr>
            </table>
        </div>
    </div>
</template>

<script>

export default {
    name: 'SinglePlayer',
    props: {
        player: Object
    }
}
</script>

<style scoped>


.player-container {
    display: flex;
    width: 80% !important;
    margin: 0.5em auto;
    border: 0.3em solid black;
    padding: 30px;
    border-radius: 5px;
    background-color: #fff;

}

.img-container {
    margin: 0 15px;
    display: flex;
    align-items: center;
    justify-content: center;
}

.player-details {
    margin: 0 15px;
    width: 100%;
}

.player-name {
    margin-bottom: 20px;
    text-align: center;
}

.playerimage {
    border-radius: 50%;
}
th{
text-align:center;
}

tr, table {
    width: 100%;
    text-align: left;
}
th, td {
    width: 50%
}

th,
td,
tr {
    margin-bottom: 10px;
    line-height: 25px;
}

@media screen and (max-width: 750px) {
    .player-container {
        flex-direction: column;
    }
}

@media screen and (max-width: 476px) {
    .player-container {
        width: 100% !important;
    }
    th{
        text-align:left;
    }
}
</style>