<template>
<div class="form__input--block">
    <label for="form__text">
        <span class="form__text">{{ formText }}:</span>
    </label>
    <input type="text" class="form__input--field" spellcheck="false" :placeholder="placeHolder">
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
        width: 20rem;
        align-items: center;
        margin-bottom: 1rem;
    }
}
</style>