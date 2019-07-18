<template>
  <div>
    <section>
      <article class="profile">
        <img class="profile__img" src="http://obsil.pl/wp-content/uploads/2015/12/male-placeholder-image.jpeg" alt="photo">
        <a class="profile__title" href="#">Virginia Freeman</a>
        <p class="profile__text">агенство</p>
      </article>
    </section>
    <section class="feedback">
      <div>
        <a class="feedback__first" href="#">
          <p class="feedback__text">Сотрудничества <span class="feedback__text feedback__text--amount">24</span></p>
          <img src="../assets/navigation _ lm-chevron-right.svg" alt="arrow-right">
        </a>
      </div>
      <div>
        <a class="feedback__second" href="#">
          <p class="feedback__text">Отклики <span class="feedback__text feedback__text--amount">8</span></p>
          <img src="../assets/navigation _ lm-chevron-right.svg" alt="arrow-right">
        </a>
      </div>
    </section>
  </div>
</template>

<script>
export default {
  name: 'Profile'
}
</script>

<style scoped>
.profile {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  padding: 32px 69px;
  width: 272px;
  height: 216px;
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(40, 42, 54, 0.06);
  background-color: #ffffff;
}

.profile__img {
  width: 96px;
  height: 96px;
  border-radius: 16px;
}

.profile__title {
  padding-top: 24px;
  padding-bottom: 4px;
  font-size: 18px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: normal;
  color: #282a36;
}

.profile__text {
  text-transform: uppercase;
  font-size: 12px;
  font-weight: 600;
  font-style: normal;
  font-stretch: normal;
  line-height: 1.33;
  letter-spacing: 1px;
  color: #808792;
}

.feedback {
  margin-top: 16px;
  padding: 16px;
  background: #ffffff;
  border-radius: 4px;
  box-shadow: 0 1px 4px 0 rgba(40, 42, 54, 0.06);
  width: 272px;
}

.feedback__first,
.feedback__second {
  display: flex;
  justify-content: space-between;
}

.feedback__first {
  padding-bottom: 16px;
  border-bottom: solid 1px #f3f4f6;
}

.feedback__second {
  padding-top: 16px;
}

.feedback__text--amount {
  font-size: 12px;
  color: #808792;
  line-height: 1.33;
  letter-spacing: 1px;
  padding-left: 8px;
}
</style>
