<template>
    <div class="justify-content-start mb-3">
        <select 
        class="me-2 form-select dm-wd-select" 
        aria-label="Default select example" 
        v-model="genre"
        @change="$emit('filter', genre)">
            <option value="">All</option>
            <option value="Rock">Rock</option>
            <option value="Pop">Pop</option>
            <option value="Jazz">Jazz</option>
            <option value="Metal">Metal</option>
            
        </select>
        <span class="dm-txt-selection">Seleziona genere</span>
    </div>
</template>

<script>
export default { 
    name: 'Search', 

    data(){
        return{
            genre: ""
        }        
    }
}
</script>

<style lang="scss" scoped>
@import '../../assets/style/global.scss';

    .dm-wd-select{
        width: 250px;
        display: inline-block;
    }

    .dm-txt-selection{
        color: $text-color
    }
</style>