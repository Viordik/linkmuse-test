<template>
  <div class="ad">
    <section class="caption">
      <h1 class="caption__h1">Объявления</h1>
    </section>
    <section class="content">
      <article class="content__item" v-for="item in items" :key="item.id">
        <div class="content__header">
          <p class="content__category">{{item.category}}</p>
          <a href="#" v-on:click="item.isMore === false ? item.isMore = true : item.isMore = false">
            <img src="../assets/navigation _ lm-more-horizontal.svg" alt="more">
          </a>
          <div class="archive" v-if="item.isMore">
            <a href="#">В архив</a>
          </div>
        </div>
        <h1 class="content__h1">{{item.role}}</h1>
        <p class="content__description">{{item.actor}}</p>
        <div class="content__center">
          <p class="content__data">{{item.casting}}</p>
          <p class="content__data">{{item.work}}</p>
          <p class="content__price">{{item.price}}</p>
        </div>
        <a class="content__respond" href="#" v-on:click="item.isModal = true" v-if="!item.isSend">откликнуться</a>
        <a class="content__send" href="#" v-else>Отклик отправлен</a>
      </article>
    </section>

    <!-- modal -->
    <section class="modal" id="modal" v-if="item.isModal" v-for="item in items" :key="item.id">
      <img class="modal__img" src="../assets/social _ lm-casting-invite.svg" alt="casting-invite">
      <button class="modal__btn-close" type="buttin" v-on:click="item.isModal = false"></button>
      <h2 class="modal__h2">Отклик на кастинг</h2>
      <p class="modal__text">{{item.role}}</p>
      <button class="modal__btn" type="button" v-on:click="item.isSend = true; item.isModal = false">отправить</button>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Ad',
  data() {
    return {
      items: [
        {
          id: 1,
          isMore: false,
          isModal: false,
          isSend: false,
          category: 'полнометражный фильм',
          role: 'Требуется рыба на роль аквамена',
          actor: 'Актер, модель • Мужской • 20-24',
          casting: 'Дата кастинга: 20.06.19-30.06.19',
          work: 'Дата работы: 12.07.19-24.09.19',
          price: '1 400 000 ₽'
        },
        {
          id: 2,
          isMore: false,
          isModal: false,
          isSend: false,
          category: 'короткометражный фильм',
          role: 'Требуется индюк на роль героя в новом фильме',
          actor: 'Актер, модель • Мужской • 20-24',
          casting: 'Дата кастинга: 20.06.19-30.06.19',
          work: 'Дата работы: 12.07.19-24.09.19',
          price: '1 500 000 ₽'
        },
        {
          id: 3,
          isMore: false,
          isModal: false,
          isSend: false,
          category: 'полнометражный фильм',
          role: 'Требуется актер на роль самца в новом фильме',
          actor: 'Актер, модель • Мужской • 20-24',
          casting: 'Дата кастинга: 20.06.19-30.06.19',
          work: 'Дата работы: 12.07.19-24.09.19',
          price: '1 600 000 ₽'
        }
      ]
    }
  },
  watch: {
    isSend() {
      if (item.isSend === true) {
        this.isModal = false;
      }
    }
  }
}
</script>

<style scoped>
.ad {
  position: relative;
  max-width: 848px;
  width: 100%;
}

.caption {
  padding: 20px 0 20px 16px;
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(40, 42, 54, 0.06);
  background-color: #ffffff;
}

.caption__h1 {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 1px;
}

.content {
  display: flex;
  margin-top: 2px;
  background: #ffffff;
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(40, 42, 54, 0.06);
  background-color: #ffffff;
}

.content__item {
  max-width: 282px;
  width: 100%;
}

.content__header {
  position: relative;
  display: flex;
  justify-content: space-between;
}

.archive {
  position: absolute;
  right: 0;
  top: 16px;
  padding: 16px 20px;
  background: #ffffff;
  border-radius: 16px;
  box-shadow: 0 4px 16px 0 rgba(40, 42, 54, 0.16);
}

.content__item {
  margin: 20px 0;
  padding: 0 20px 16px;
}

.content__item:not(:nth-child(3n)) {
  border-right: solid 1px rgba(40, 42, 54, 0.08);
}

.content__category {
  padding-bottom: 10px;
  text-transform: uppercase;
  font-size: 8px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.5;
  letter-spacing: 1px;
  color: #0063da;
}

.content__h1 {
  padding-bottom: 8px;
  font-size: 14px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.29;
  letter-spacing: 0.5px;
  color: #282a36;
}

.content__description {
  font-size: 12px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 0.5px;
  color: #515562;
}

.content__center {
  margin: 12px 0 16px 0;
  padding: 14px 0 12px 0;
  border-top: solid 1px rgba(40, 42, 54, 0.08);
  border-bottom: solid 1px rgba(40, 42, 54, 0.08);
}

.content__data {
  padding-bottom: 8px;
  font-size: 14px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.29;
  letter-spacing: 0.25px;
  color: #515562;
}

.content__price {
  font-size: 14px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.29;
  letter-spacing: 0.5px;
  color: #282a36;
}

.content__respond {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 1px;
  color: #0063da;
}

.content__send {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 1px;
  color: rgba(40, 42, 54, 0.32);
}

.modal {
  position: absolute;
  top: 50%;
  left: 20%;
  display: flex;
  flex-direction: column;
  align-items: center;
  padding: 32px 36px;
  border-radius: 16px;
  background-color: #ffffff;
  max-width: 262px;
}

.modal__img {
  position: relative;
  width: 64px;
  height: 64px;
}

.modal__btn-close {
  cursor: pointer;
  position: absolute;
  top: 0;
  right: 0;
  width: 16px;
  height: 16px;
  background: transparent;
  border: none;
}

.modal__btn-close::after {
  position: absolute;
  content: '';
  top: 50%;
  left: 0px;
  width: 16px;
  height: 2px;
  transform: rotateZ(45deg);
  background: #888a8f;
}

.modal__btn-close::before {
  position: absolute;
  content: '';
  top: 50%;
  left: 0px;
  width: 16px;
  height: 2px;
  transform: rotateZ(-45deg);
  background: #888a8f;
}

.modal__h2 {
  padding-top: 20px;
  font-size: 18px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 0.25px;
  color: #282a36;
}

.modal__text {
  padding: 12px 0 24px;
  text-align: center;
  font-size: 14px;
  font-weight: normal;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.29;
  letter-spacing: 0.25px;
  color: #515562;
}

.modal__btn {
  cursor: pointer;
  max-width: 190px;
  width: 100%;
  border: none;
  text-transform: uppercase;
  color: #ffffff;
  border-radius: 16px;
  background-color: #0063da;
  padding: 12px 0;
  text-align: center;
}

.modal__btn:hover {
  background: #004faf;
}
</style>
