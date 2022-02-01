<template>
    <div>
        <select class="form-select dm-wd-select" aria-label="Default select example">
            <option value="" disabled selected>Seleziona genere</option>
            <option value="rock">Rock</option>
            <option value="pop">Pop</option>
            <option value="jazz">Jazz</option>
            <option value="metal">Metal</option>
        </select>
    </div>
</template>

<script>
export default {
    name: 'Search',
}
</script>

<style lang="scss" scoped>
    .dm-wd-select{
        width: 250px;
    }
</style>