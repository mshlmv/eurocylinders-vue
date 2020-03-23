<template>
  <header>
    <div class="container mx-auto">
      <div class="flex items-center">
        <a href="/">
          <g-image src="~/assets/img/ecs-logo.png" alt="ECS Logo" width="150" height="60" class="logotype pr-8"/>
        </a>
        <nav class="flex justify-between items-center w-full pl-6">
          <a href="/#about" class="nav-item">Компания</a>
          <a href="/#assortment" class="nav-item">Предложения</a>
          <a href="/#quality" class="nav-item">Стандарты</a>
          <g-link to="/production/" class="nav-item" active-class="is-active">Производство</g-link>
          <g-link to="/goods/" class="nav-item" active-class="is-active">Продукция</g-link>
          <g-link to="/dilers/" class="nav-item" active-class="is-active">Дилеры</g-link>
          <g-link to="/contacts/" class="nav-item" active-class="is-active">Контакты</g-link>
          <a href="https://eurocylinders.com/" target="_blank" class="ex-link">EN</a>
        </nav>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header',
}
</script>

<style lang="scss">
header {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  z-index: 99;
  background-color: rgba(255,255,255, .75);
}

.logotype {
  box-sizing: content-box;
}

.nav-item {
  padding: rem(25) 0;
  border-bottom: 7px solid transparent;

  &:hover, &.is-active {
    border-bottom-color: $green-color;
  }
}
</style>