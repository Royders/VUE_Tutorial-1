<template>
    <div>
        <input @input="onInput" />
    </div>
</template>

<script>
export default {
    name: 'Searchbar',
    methods: {
        onInput: function (event)  {
            //termChange is just a name
            //$emit just to give the user of the framework the freedom to decale a own "emit" function
            this.$emit('termChange', event.target.value)
        }    
    }
}
    
</script>

<style scoped>
input{
    width: 75%
}
div{
    text-align: center;
    margin: 20px;
}

</style>

