<template>
<header>
    <div class="header__container">
        <div class="header__block">
            <h1>Регистрация клиента</h1>
        </div>
    </div>
</header>
</template>

<script>
module.exports = {
props: {
 },
data: function() {
    return {

    }
}
}
</script>

<style lang="scss">
header {
    background-color: rgb(79, 148, 79);
    display: flex;
    justify-content: center;
    height: 4rem;
    align-items: center;

    &__block {
    width: 100%;
    }

    &__container {
    max-width: 48rem;
    flex-grow: 1;
    }
}

h1 {
    font-weight: 800;
    color: white;
    font-size: 1.5rem;
}
</style>