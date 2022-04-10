<template>
<div class="form__input--block">
    <label for="form__text">
        <span class="form__text">{{ formText }}:</span>
    </label>
    <input type="tel" class="form__input--field" :placeholder="placeHolder">
</div>
</template>

<script>
module.exports = {
props: {
    formText: String,
    placeHolder: String,
 }
}
window.addEventListener("DOMContentLoaded", function() {
  function setCursorPosition(pos, elem) {
  elem.focus();
  if (elem.setSelectionRange) elem.setSelectionRange(pos, pos);
    else if (elem.createTextRange) {
    let range = elem.createTextRange();
    range.collapse(true);
    range.moveEnd("character", pos);
    range.moveStart("character", pos);
    range.select()
  }
}
function mask(event) {
  let matrix = "7 (___) ___ ____",
  i = 0,
  def = matrix.replace(/\D/g, ""),
  val = this.value.replace(/\D/g, "");
  if (def.length >= val.length) val = def;
  this.value = matrix.replace(/./g, function(a) {
    return /[_\d]/.test(a) && i < val.length ? val.charAt(i++) : i >= val.length ? "" : a
  });
  if (event.type == "blur") {
    if (this.value.length == 2) this.value = ""
  }     else setCursorPosition(this.value.length, this)
}
let input = document.querySelector('input[type="tel"]');
input.addEventListener("input", mask, false);
input.addEventListener("focus", mask, false);
input.addEventListener("blur", mask, false);
});
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