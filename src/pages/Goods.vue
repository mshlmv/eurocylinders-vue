<template>
  <Layout>
    <section class="goods">
      <div class="container mx-auto">
        <div class="heading-group text-center mb-8">
          <h2 class="uppercase">Продукция</h2>
        </div>
        <div class="grid grid-cols-3 gap-6">
          <template v-for="i in 10">
            <div :key="i">
              <img src="https://via.placeholder.com/300" alt class="mb-4" />
              <p class="mb-2">Название продукта</p>
              <button v-on:click="show" class="btn btn-success">Подробнее</button>
            </div>
          </template>
        </div>
      </div>
    </section>
    <modal name="hello-world">Характеристики товара</modal>
  </Layout>
</template>

<script>
export default {
  metaInfo: {
    title: "Продукция"
  },
  methods: {
    show() {
      this.$modal.show("hello-world");
    }
  }
};
</script>

<style lang="scss" scoped>
.goods {
  margin-top: 80px;
  padding: 120px 0;
}
</style>