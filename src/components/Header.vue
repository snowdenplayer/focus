<template>
  <header class="header container--fluid ">
      <div class="header__burger" @click.stop="showSideBar">
        <span></span>
        <span></span>
        <span></span>
      </div>
      <div class="header__sidebar" :class="{'header__sidebar--active': isVisibleSideBar}">
        <div class="sidebar__group">
          <div class="sidebar__group-title">Разделы</div>
          <ul class="sidebar__list">
            <li
                class="sidebar__list-item"
                v-for="item in sections"
                :key="item.key"
                @click.stop="showSideBar"
            >
              <a href="#" class="sidebar__list-link">{{ item.name }}</a>
            </li>
          </ul>
        </div>
        <div class="sidebar__group sidebar__group--visible">
          <div class="sidebar__group-title">Материалы</div>
          <ul class="sidebar__list">
            <li
                class="sidebar__list-item"
                v-for="item in navigationItems"
                :key="item"
                @click.stop="showSideBar"
            >
              <a href="#" class="sidebar__list-link">{{ item }}</a>
            </li>

          </ul>
        </div>
      </div>
      <h1>
        <a href="#" class="header__logo">
          <img src="../assets/images/logo.png" alt="">
        </a>
      </h1>
      <ul class="header__navigation">
        <div class="header__navigation-item"
             v-for="(item,idx) in navigationItems"
             :key="idx"
        >{{ item }}
        </div>
      </ul>
      <div class="header__lang">
        <a href="#" class="lang__item lang__item-active">UA</a>
        <a href="#" class="lang__item">RU</a>
      </div>
      <button class="header__search" @click="$emit('showModal')">
        <img src="../assets/images/search.svg" alt="">
      </button>

  </header>
</template>

<script>
export default {
  name: "Header",
  data() {
    return {
      isVisibleSideBar: false,
      navigationItems: [
        'Категории', 'Спецтема', 'РЕЙТИНГИ', 'Подписка'
      ],
      sections: [
        {
          id: 1,
          name: 'Политика'
        },
        {
          id: 2,
          name: 'Украина'
        },
        {
          id: 3,
          name: 'Мир'
        },
        {
          id: 4,
          name: 'Авто'
        }
      ]
    }
  },
  methods: {
    showSideBar() {
      this.isVisibleSideBar = !this.isVisibleSideBar
    }
  },
  created() {
    document.addEventListener('click', () => {
      this.isVisibleSideBar = false
    })
  },
  watch: {
    isVisibleSideBar: function () {
      if (this.isVisibleSideBar) {
        document.documentElement.style.overflow = 'hidden'
      } else {
        document.documentElement.style.overflow = 'auto'
      }
    }
  }
}
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.header {
  display: flex;
  width: 100%;
  align-items: center;
  height: 77px;
  position: sticky;
  top: 0;
  left: 0;
  z-index: 150;
  background: #fff;

  &__burger {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    width: 27px;
    height: 18px;
    cursor: pointer;
    margin-right: 16px;

    span {
      background-color: $mainBlack;
      width: 100%;
      height: 3px;
    }
  }

  &__sidebar {
    position: fixed;
    top: 77px;
    left: 0;
    padding-left: 30px;
    padding-top: 20px;
    transform: translateX(-100%);
    overflow-y: auto;
    width: 330px;
    height: 100vh;
    background-color: #fff;
    transition: all 0.3s;

    &--active {
      transform: translateX(0);
    }

    .sidebar__group {
      margin-bottom: 20px;

      &--visible {
        display: none;
      }

      &-title {
        margin-bottom: 15px;
        font-size: 1.4rem;
        color: #929292;
        font-weight: 700;
        text-transform: uppercase;
      }

      .sidebar__list {
        &-item:not(:last-child) {
          margin-bottom: 10px;
        }

        &-link {
          font-size: 1.7rem;
          text-transform: uppercase;
          font-weight: 700;
          line-height: 1;
          color: $mainBlack;

          &:hover {
            color: #929292;
          }
        }
      }
    }
  }

  &__navigation {
    display: flex;
    justify-content: center;
    flex-grow: 1;
    font-size: 18px;
    line-height: 23px;

    &-item {
      text-transform: uppercase;
      font-weight: 600;
      margin-left: 50px;
      cursor: pointer;

      &:first-child {
        margin-left: 0;
      }

      &:hover {
        color: gray;
      }
    }
  }

  &__lang {

    .lang__item {
      font-weight: 500;
      font-size: 18px;
      line-height: 23px;
      text-transform: uppercase;
      text-decoration: none;
      color: $mainBlack;
      font-weight: 600;

      &:first-child {
        margin-right: 10px;
      }

      &-active {
        color: #ED3237;
      }
    }
  }

  &__search {
    background-color: transparent;
    border: none;
    margin-left: 15px;
  }
}

@media (max-width: 992px) {
  .header {
    height: 67px;

    &__navigation {
      display: none;
    }

    &__lang {
      display: flex;
      justify-content: flex-end;
      flex-grow: 1;
    }

    &__sidebar {
      top: 67px;
    }

    .sidebar__group {
      &--visible {
        display: block;
      }
    }
  }

}
</style>