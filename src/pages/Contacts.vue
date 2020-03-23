<template>
  <Layout>
    <yandex-map :coords="coords" :zoom="18">
      <ymap-marker :coords="coords" marker-id="1"/>
    </yandex-map>
    <section class="grid grid-cols-2 grid-gap-4 my-12">
      <div class="px-32">
        <h2 class="contact-title mb-8">Rufen Sie uns an<br> <strong>oder senden Sie uns eine Mail.</strong></h2>
        <div class="contact-block">
          <g-image src="~/assets/img/phone.svg" alt="phone icon" width="40" class="contact-block__image"/>
          <div>
            <div class="heading-text">+49 36 44 - 62 10</div>
            <div>Zögern Sie nicht uns anzurufen!</div>
          </div>
        </div>
        <div class="contact-block">
          <g-image src="~/assets/img/clock.svg" alt="clock icon" width="40" class="contact-block__image"/>
          <div>
            <div class="heading-text">Öffnungszeiten</div>
            <div>Montag - Freitag: 7:00 - 16:00</div>
          </div>
        </div>
        <div class="contact-block">
          <g-image src="~/assets/img/marker.svg" alt="marker icon" width="40" class="contact-block__image"/>
          <div>
            <div class="heading-text">Firmensitz</div>
            <div>Auenstraße 21, 99510 Apolda</div>
          </div>
        </div>
      </div>
      <div class="mt-12">
        <form @submit="onSubmit">
          <div class="form-row">
            <div class="form-group">
              <input v-model="contact.fname" name="fname" type="text" placeholder="Name" class="form-control">
            </div>
            <div class="form-group">
              <input v-model="contact.lname" name="lname" type="text" placeholder="Unternehmen" class="form-control">
            </div>
          </div>
          <div class="form-row">
            <div class="form-group">
              <input v-model="contact.email" name="email" type="text" placeholder="E-Mail" class="form-control">
            </div>
            <div class="form-group">
              <input v-model="contact.telefon" name="telefon" type="text" placeholder="Telefon" class="form-control">
            </div>
          </div>
          <div class="form-row">
            <div class="form-group">
              <textarea v-model="contact.message" name="message" class="form-control" rows="6"></textarea>
            </div>
          </div>
          <div class="form-row">
            <div class="form-group">
              <button class="btn btn-success">Отправить</button>
            </div>
          </div>
        </form>
      </div>
    </section>
  </Layout>
</template>

<script>
import { yandexMap, ymapMarker } from 'vue-yandex-maps'
import axios from 'axios'

export default {
  metaInfo: {
    title: 'Контакты'
  },
  components: {
    yandexMap,
    ymapMarker
  },
  data: () => ({
    coords: [
      51.033133,
      11.519483
    ],
    contact: {
      fname: '',
      lname: '',
      email: '',
      telefon: '',
      message: ''
    },
    isSending: false
  }),
  methods: {
    clearForm() {
      for (let field in this.contact) {
        this.contact[field] = ''
      }
    },
    onSubmit(event) {
      event.preventDefault();
      this.isSending = true;

      setTimeout(() => {
        let form = new FormData();
        for (let field in this.contact) {
          form.append(field, this.contact[field]);
        }
        axios.post('/post.php', form).then((response) => {
          console.log(response);
          this.clearForm();
          this.isSending = false;
        }).catch((e) => {
          console.log(e);
        });
      }, 1000);
    }
  }
}
</script>

<style lang="scss">
.ymap-container {
  height: 480px;
  margin-top: 80px;
}
.contact-title {
  color: $blue-color;
  font-size: rem(48);
  line-height: 1.1;
  
  strong {
    font-weight: 700;
  }
}
.contact-block {
  display: flex;
  color: $blue-color;
  margin-bottom: rem(20);
  .heading-text {
    font-size: rem(22);
  }
}
.contact-block__image {
  margin-right: rem(20);
}
.form-row {
  display: flex;
}
.form-group {
  margin-bottom: 1rem;
  width: 100%;
  padding: 0 10px;
}
.form-control {
  display: block;
  width: 100%;
  padding: .375rem .75rem;
  font-size: 1rem;
  line-height: 1.5;
  color: #495057;
  background-color: #fff;
  background-clip: padding-box;
  border: 1px solid #ced4da;
  border-radius: .25rem;
  transition: border-color .15s ease-in-out,box-shadow .15s ease-in-out;
}
</style>