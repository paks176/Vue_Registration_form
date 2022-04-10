<template>
  <div class="container__page">
    <pageHeader></pageHeader>
    <main>
      <div class="container__main">
        <div class="container__form">
          <div class="form">
            <textField formText="Фамилия" placeHolder="Введите фамилию"></textField>
            <textField formText="Имя" placeHolder="Введите имя"></textField>
            <textField formText="Отчество" placeHolder="Введите отчество"></textField>
            <birthDateField formText="Ваша дата рождения"></birthDateField>
            <passportField formText="Серия паспорта" placeHolder="Серия паспорта"></passportField>
            <telField formText="Телефон" placeHolder="+7(XXX)XXX-XX-XX"></telField>
            <chooseSex formText="Укажите Ваш пол"></chooseSex>
            <multiSelect></multiSelect>
          </div>
          <span>* - Обязательно для заполнения</span>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
import textField from "./components/textField";
import pageHeader from "./components/pageHeader";
import birthDateField from "./components/birthDateField";
import passportField from "./components/passportField";
import telField from "./components/telField";
import chooseSex from "./components/chooseSex";
import multiSelect from "./components/multiSelect";

export default {
  name: "App",
  components: {
    textField,
    pageHeader,
    birthDateField,
    passportField,
    telField,
    chooseSex,
    multiSelect,
},
  data: function () {
    return {
      search: "",
      isEnabled: false,
      boxArray: [],
    };
  },
};
</script>

<style lang="scss">
* {
  font-family: Arial, Helvetica, sans-serif;
  font-size: 16px;
  padding: 0;
  margin: 0;
}

.container {

  &__main {
  display: flex;
  justify-content: center;
  }

  &__form {
  max-width: 48rem;
  flex-grow: 1;
  margin: 1.5rem 0 1.5rem 0;
  }
}
</style>
 