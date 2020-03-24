<template>
<section class="footer pt-10" id="footer">
  <div class="container mx-auto">
    <div class="grid grid-cols-3 gap-4">
      <div class="flex flex-col bg-map">
        <g-image src="~/assets/img/ecs-logo-white.png" alt="ECS logo" width="210" height="80" fit="contain"/>
        <h3 class="text-white my-4">eurocylinder systems AG</h3>
        <ul class="list-disc">
          <li>Auenstrasse 21</li>
          <li>D-99510 Apolda</li>
          <li>Tel.: +49 36 44 - 62 10</li>
          <li>Fax: +49 36 44 - 62 12 03</li>
          <li>info@eurocylinders.com</li>
        </ul>
      </div>
      <div class="flex flex-col justify-center items-center">
        <g-image src="~/assets/img/location-icon.svg" alt="location icon" width="50"/>
        <h3 class="text-white">Our location</h3>
        <a href="#" class="green-link">Find us</a>
      </div>
      <div class="flex flex-col justify-center items-center bg-quote">
        <g-image src="~/assets/img/envelope-icon.svg" alt="envelope icon" width="60"/>
        <h3 class="text-white">Contact</h3>
        <a href="#" class="green-link">Our contact form</a>
      </div>
    </div>
    <footer class="py-8">
      <p class="text-white text-xs">© 2020 <a href="#">Imprint</a> | <a href="#">Privacy Notice</a></p>
    </footer>
  </div>
</section> 
</template>

<script>
export default {
  name: 'Footer',
}
</script>

<style lang="scss" scoped>
.footer {
  background-color: $blue-color;
  color: #c1cde5;
}
.bg-map {
  background: url("~@/assets/img/bg-map.svg") no-repeat 50% 50%;
}
.bg-quote {
  background: url("~@/assets/img/bg-quote.svg") no-repeat 50% 50%;
}
.green-link {
  border-bottom: 2px solid $green-color;
  &:hover {
    border-bottom-color: currentColor;
  }
}
</style>