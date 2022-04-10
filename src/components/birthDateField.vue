<template>
<div class="form__input--block">
    <label for="form__birthdate">
        <span class="form__text">{{ formText }}:</span>
    </label>
    <input type="date" min="1900-01-01" max="2022-01-01" class="form__input--field">
</div>
</template>

<script>
module.exports = {
props: {
    formText: String,
 }

}
</script>

<style lang="scss">
.form {
    &__input--field {
        padding: 0.5rem;
        border-radius: 0.4rem;
        border: 1px solid gray;
    }
    &__input--block {
        display: flex;
        justify-content: space-between;
        width: 26rem;
        align-items: center;
        margin-bottom: 1rem;
    }
}
</style>