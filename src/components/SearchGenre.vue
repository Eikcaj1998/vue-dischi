<template>
        <div class="col-2">
            <h3>Scegli per genere</h3>
            <select class="form-select" v-model="selectedValue" @click="$emit('choosedGenre', selectedValue)">
                <option value="">Nessuna selezione</option>
                <option>Jazz</option>
                <option>Rock</option>
                <option>Pop</option>
                <option>Metal</option>
            </select>
        </div>
</template>

<script>
export default {
    name: 'searchForGenre',
    data: function(){
        return{
            selectedValue: '',
        }
    }

}
</script>