<template>
  <Layout>
    <section class="dilers-list">
      <div class="container mx-auto">
        <div class="heading-group text-center mb-8">
          <h2 class="uppercase">Список дилеров</h2>
        </div>
        <div class="grid grid-cols-4 gap-6">
          <template v-for="i in 6">
            <div>
              <img src="https://via.placeholder.com/150" alt="" class="mb-4">
              <p class="mb-2">Название дилера</p>
              <a href="#" class="underline">Адрес сайта</a>
            </div>
          </template>
        </div>    
      </div>
    </section>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: 'Дилеры'
  }
}
</script>

<style lang="scss" scoped>
.dilers-list {
  margin-top: 80px;
  padding: 120px 0;
}
a {
  color: $green-color;
}
</style>