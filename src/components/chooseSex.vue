<template>
<div class="form__input--block">
    <span class="form__text">{{ formText }}:</span>
    <div class="form__input--radios-block">
        <div class="form__input--radios-choose">
            <label for="chooseMale">
                <span class="form__input--radios-text">Мужской</span>
            </label>
            <input type="radio" name="chooseSex" id="chooseMale" value="male" class="form__input--field">
        </div>
        <div class="form__input--radios-choose">
            <label for="chooseFemale">
                <span class="form__input--radios-text">Женский</span>
            </label>
            <input type="radio" id="chooseFemale" name="chooseSex" value="female" class="form__input--field">
        </div>
    </div>
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
    &__input {
        &--radios {
            &-block {
                display: flex;
                flex-wrap: wrap;
            }
            &-text {
                margin-right: 0.5rem;
            }
            &-text:hover {
                cursor: pointer;
            }
            &-choose:first-child {
                margin-right: 2rem;
            }
        }
        &--field {
            padding: 0.5rem;
            border-radius: 0.4rem;
            border: 1px solid gray;
        }
        &--block {
            display: flex;
            justify-content: space-between;
            width: 26rem;
            align-items: center;
            margin-bottom: 1rem;
        }
    }
}
</style>