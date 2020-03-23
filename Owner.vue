<template>
    <div class="owner">
        <h3>Propriétaire</h3>

        <p>
        <input type="text" v-model="owner"> 
        <button @click="displayOwner">{{ buttonText }}</button><br>
        </p>

        <p v-if="ownerSeen">
        Le créateur s'avère s'appeler {{ owner }}
        </p>
    </div>
</template>

<script>
export default {
  name: 'Owner',
  props: {
    owner: String, 
    ownerSeen: Boolean,
    buttonText: String,
    displayOwner: Function
  }
}
</script>

<style>
    input {
        height: 19px;
        border: 1px solid darkcyan;
        padding: 3px;
    }
    button {
        background-color: darkcyan;
        margin-top: 20px;
        margin-left: 10px;
        padding: 5px;
        border: 0;
        color: #fff;
        border-radius: 5px;
        cursor: pointer;
    }
</style>