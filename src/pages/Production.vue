<template>
  <Layout>
    <section class="banner"></section>
    <section class="content">
      <div class="container mx-auto">
        <div class="heading-group text-center mb-8">
          <h2 class="uppercase">Production process</h2>
        </div>
        <p>For more than 60 years we’ve been producing seamless high-pressure steel cylinders on our company site in Apolda, Thuringia, Germany. Our equipment and processes have been constantly evolving ever since and are subject to relentless continuous improvement every single day. With an annualproduction capacity of more than 500,000 cylinders, manufactured on two production lines, we’re among the World’s most efficient steel cylinder manufacturers.</p>
        <div class="flex flex-row mt-16">
          <div class="text text-lg">
            <p>1. The production cycle starts with seamless precision steel tube from certified manufacturers.</p>
            <p>2. The tubes are cut to length by a plasma beam.</p>
            <p>3. Cylinder base and neck are formed by spinning and / or flow forming.</p>
            <p>4. During quenching and tempering the required material properties are set.</p>
          </div>
          <div>
            <g-image src="/media/produktion4-768x437.jpg" alt="produktion4-768x437"/>
          </div>
        </div>
        <div class="flex flex-row-reverse">
          <div></div>
          <div></div>
        </div>
        <div class="flex flex-row">
          <div></div>
          <div></div>
        </div>
        <div class="flex flex-row-reverse">
          <div></div>
          <div></div>
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