<template>
<div class="form__input--block">
    <label for="form__text">
        <span class="form__text">{{ formText }}:</span>
    </label>
    <input type="number" class="form__input--field" :placeholder="placeHolder">
</div>
</template>

<script>
module.exports = {
props: {
    formText: String,
    placeHolder: String,
 }

}
</script>

<style>
.form__input--field {
    padding: 0.5rem;
    border-radius: 0.4rem;
    border: 1px solid gray;
}
.form__input--block {
    display: flex;
    justify-content: space-between;
    width: 26rem;
    align-items: center;
    margin-bottom: 1rem;
}
</style>