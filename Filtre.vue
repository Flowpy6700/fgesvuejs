<template>
    <div>
        <ul>
            <li v-for="l in list" :key="l">{{l | uppercase}}</li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'Exo2',
    data: () => {
        return {
            list: [
                'index0',
                'index1',
                'index2'
            ]
        }
    },
    filters: {
        uppercase(val){
            return val.toUpperCase();
        }
    }
}
</script>
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>