<template>
    <div class="appname">
        <h1> {{ appName }} </h1>
    </div>
</template>

<script>
export default {
    name: 'MyHeader',
    props: {
        appName: String,
    }
}
</script>

<style scoped>
.appname {
    text-align: center;
    padding: 1em 0;
}
</style>