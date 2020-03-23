<template>
<div class="layout">
  <Header/>
  <slot/>
  <Footer/>
</div>
</template>

<script>
import Header from '~/components/Header.vue'
import Footer from '~/components/Footer.vue'

export default {
  components: {
    Header,
    Footer
  }
}
</script>

<style lang="scss">
body {
  font-family: 'Rubik', sans-serif;
  font-size: 16px;
  line-height: 1.5;
  font-weight: normal;
  color: $text-color;
}

h2 {
  font-size: rem(48);
  font-weight: 300;
}
h3 {
  font-size: rem(26);
  font-weight: 500;
}

section.colored {
  background-color: #e2e2e2;
}

.text p:not(:last-child) {
  margin-bottom: 1rem;
}

.btn {
  display: inline-block;
  font-family: Arial, sans-serif;
  font-weight: 400;
  text-align: center;
  white-space: nowrap;
  vertical-align: middle;
  user-select: none;
  border: 1px solid transparent;
  padding: .375rem .75rem;
  font-size: 1rem;
  line-height: 1.5;
  transition: color .15s ease-in-out, background-color .15s ease-in-out,
  border-color .15s ease-in-out, box-shadow .15s ease-in-out;

  &:not(:disabled):not(.disabled) {
    cursor: pointer;
  } 
}
.btn-success {
  color: #fff;
  background-color: $green-color;
  border-color: $green-color;

  &:hover, &:active {
    background-color: darken($green-color, 5);
    border-color: darken($green-color, 5);
  }
  &:focus {
    outline: none;
    box-shadow: 0 0 0 0.2rem rgba($green-color,.5);
  }
}
.btn-lg {
  font-size: 17px;
  font-weight: 500;
  line-height: 1;
  padding: rem(12) rem(35);
  min-width: 265px;
}
.btn-medium {
  padding: .5rem 1rem;
}
.btn-rounded {
  border-radius: rem(30);
}
</style>
