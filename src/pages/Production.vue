<template>
  <Layout>
    <section class="banner"></section>
    <section class="content">
      <div class="container mx-auto">
        <div class="heading-group text-center mb-8">
          <h2 class="uppercase">Production process</h2>
        </div>
        <p>For more than 60 years we’ve been producing seamless high-pressure steel cylinders on our company site in Apolda, Thuringia, Germany. Our equipment and processes have been constantly evolving ever since and are subject to relentless continuous improvement every single day. With an annualproduction capacity of more than 500,000 cylinders, manufactured on two production lines, we’re among the World’s most efficient steel cylinder manufacturers.</p>
        <div class="grid grid-cols-2 gap-6 my-16">
          <div class="text text-lg">
            <p>1. The production cycle starts with seamless precision steel tube from certified manufacturers.</p>
            <p>2. The tubes are cut to length by a plasma beam.</p>
            <p>3. Cylinder base and neck are formed by spinning and / or flow forming.</p>
            <p>4. During quenching and tempering the required material properties are set.</p>
          </div>
          <div>
            <g-image src="/media/produktion1.jpg" alt="produktion1"/>
          </div>
          <div>
            <g-image src="/media/produktion2.jpg" alt="produktion2"/>
          </div>
          <div class="text text-lg">
            <p>5. The machining of the neck is performed on CNC controlled machining centers.</p>
            <p>6. The steel cylinders are internally and externally shot-blasted thereafter.</p>
            <p>7. In cold condition neck ring and foot ring are pressed on the cylinder.</p>
            <p>8. Special electronic balances determine the exact weight of the cylinder.</p>
          </div>
          <div class="text text-lg">
            <p>9. According to customers specification and legal requirements the cylinders are stamp marked.</p>
            <p>10. Numerous quality checks such as automated hardness and ultrasonic tests, hydraulic test and visual inspection are performed on each cylinder.</p>
            <p>11. Environmentally friendly powder coat or water varnish I used for surface coating.</p>
          </div>
          <div>
            <g-image src="/media/produktion3.jpg" alt="produktion3"/>
          </div>
          <div>
            <g-image src="/media/produktion4.jpg" alt="produktion4"/>
          </div>
          <div class="text text-lg">
            <p>12. Upon customer’s request the cylinders can be completely assembled, including valve and valve protection.</p>
            <p>13. After packing the cylinders are ready for shipping.</p>
          </div>
        </div>
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Производство'
  }
}
</script>

<style lang="scss" scoped>
.banner {
  margin-top: 80px;
  background: url("~@/assets/img/production-banner.jpg");
  background-size: cover;
  min-height: 50vh;
}
.heading-group {
  margin-top: 65px;
}
</style>