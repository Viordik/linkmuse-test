<template>
  <header class="header">
    <div>
      <a href="#">
        <img src="../assets/Group 2.1.svg" alt="LINKMUSE">
      </a>
    </div>
    <nav class="nav-menu">
      <ul class="menu-list">
        <li>
          <a href="#">Объявления</a>
        </li>
        <li>
          <a href="#">Таланты</a>
        </li>
        <li>
          <a href="#">Заказчики</a>
        </li>
        <li>
          <a href="#">Верификация</a>
        </li>
        <li>
          <a href="#" class="menu-list__link">
            <img src="../assets/navigation _ lm-more-horizontal.svg" alt="more">
          </a>
        </li>
      </ul>
    </nav>
    <div class="create-chat-follow">
      <a href="#" class="ccf create-chat-follow__first">
        <img src="../assets/lm-delete_close.svg" alt="PLUS">
        Создать
      </a>
      <a href="#" class="ccf create-chat-follow__second">
        <img src="../assets/social _ lm-chat.svg" alt="chat">
      </a>
      <a href="#" class="ccf create-chat-follow__third">
        <img src="../assets/navigation _ lm-notification.svg" alt="follow">
      </a>
    </div>
    <div class="user">
      <a href="#" class="user__photo-name">
        <img src="http://obsil.pl/wp-content/uploads/2015/12/male-placeholder-image.jpeg" alt="photo" width="20">
        <span>Name</span>
      </a>
      <a href="#" class="user__dropdown">
        <img src="../assets/controls _ lm-dropdown.svg" alt="dropdown">
      </a>
    </div>
  </header>
</template>

<script>
export default {
  name: 'Header'
}
</script>

<style scoped>
.header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  padding: 17px 152px;
  background: #ffffff;
  box-shadow: 0 1px 4px 0 rgba(40, 42, 54, 0.06);
}

.nav-menu {
  margin: 0 115px 0 48px;
  flex-grow: 1;
}

.menu-list {
  display: flex;
  list-style: none;
  justify-content: space-between;
  align-items: center;
}

.menu-list__link {
  display: flex;
}

.menu-list a:hover {
  color: #0063da;
}

.create-chat-follow {
  display: flex;
  align-items: center;
  flex-grow: 1;
}

.create-chat-follow__first {
  color: #0063da;
  padding-right: 48px;
}

.ccf {
  display: flex;
}

.create-chat-follow__first > img {
  padding-right: 8px;
}

.create-chat-follow__second {
  position: relative;
  padding-right: 36px;
}

.create-chat-follow__third {
  position: relative;
}

.create-chat-follow__second::after,
.create-chat-follow__third::after {
  content: '';
  position: absolute;
  top: -3px;
  left: 8px;
  width: 8px;
  height: 8px;
  border: solid 2px #ffffff;
  border-radius: 50%;
  background: #0063da;
}

.user {
  display: flex;
  align-items: center;
}

.user__photo-name {
  display: flex;
  align-items: center;
  margin-right: 8px;
}

.user__photo-name > img {
  border-radius: 50%;
  margin-right: 8px;
}

.usesr__dropdown {
  display: flex;
}
</style>
