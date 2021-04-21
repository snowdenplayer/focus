<template>
  <footer class="f-footer">
    <div class="container">
      <a href="#" class="f-footer__logo">
        <img src="../assets/images/logo.png" alt="">
      </a>
      <div class="f-footer__row">
        <div class="f-footer__row-col">
          <ul class="f-footer__menu">
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Политика</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Украина</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Экономика</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Культура</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Мнение</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Рейтинги</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Доинный фокус</a>
            </li>
            <li class="f-footer__menu-item">
              <a href="#" class="f-footer__menu-link">Мир</a>
            </li>
          </ul>

        </div>
        <div class="f-footer__row-col">
          <div class="f-footer__subscribe">
            <div class="f-footer__subscribe-list">
              <li class="f-footer__subscribe-item">
                <img src="../assets/images/footer/book1.png" alt="">
              </li>
              <li class="f-footer__subscribe-item">
                <img src="../assets/images/footer/book2.png" alt="">
              </li>
              <li class="f-footer__subscribe-item">
                <img src="../assets/images/footer/book3.png" alt="">
              </li>
            </div>
            <div class="f-footer__subscribe-content">
              <div class="f-footer__subscribe-content--text">
                <p>
                  Гарантировано
                  <strong>получите скидку -10%</strong>
                </p>
              </div>
              <a href="#" class="btn f-footer__subscribe-btn">Подписаться</a>
            </div>
          </div>
        </div>
      </div>
      <div class="f-footer__row row__hr">
        <div class="f-footer__row-col f-footer__row-col--text">
          <p>
            Все права на материалы, опубликованные на данном ресурсе, принадлежат ООО "ФОКУС МЕДИА".
            Какое-либо использование материалов без письменного разрешения ООО "ФОКУС МЕДИА" - запрещено.
            При использовании материалов с данного ресурса гиперссылка focus.ua обязательна.
          </p>
          <p>
            Данный ресурс — для пользователей возрастом от 18 лет и старше.
          </p>
        </div>
        <div class="f-footer__row-col f-footer__row-col--text">
          <p>
            Перепечатка, копирование или воспроизведение информации, содержащей ссылку на агентство ИнА "Українські
            Новини", в каком-либо виде строго запрещены.
          </p>
          <p>
            Все материалы, которые размещены на этом сайте со ссылкой на агентство "Интерфакс-Украина", не подлежат
            дальнейшему воспроизведению и/или распространению в любой форме, кроме как с письменного разрешения
            агентства.
          </p>
          <p>Материалы с плашками "Р", "Новости партнеров", "Новости компаний", "Новости партий", "Инновации",
            "Позиция", "Спецпроект при поддержке" публикуются на коммерческой основе.</p>
        </div>
      </div>
      <div class="f-footer__row f-footer__row--copyright">
        <div class="f-footer__row-col">
          <p class="copyright__text">© 2020 Фокус. Все права защищены.</p>
        </div>
        <div class="f-footer__row-col">
          <p class="copyright__text">Політика конфіденційності</p>
        </div>
      </div>
    </div>

  </footer>
</template>

<script>
export default {
  name: "Footer"
}
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";

.f-footer {
  padding-top: 50px;
  padding-bottom: 15px;
  width: 100%;

  &__logo {
    display: inline-block;
    margin-bottom: 30px;
  }

  .row__hr {
    margin-top: 25px;
    padding-top: 25px;
    border-top: 1px solid gray;
  }

  &__row {
    display: flex;
    flex-wrap: wrap;

    &--copyright {
      margin-top: 25px;
    }

    &-col {
      width: 50%;
      padding: 0 15px;
      &--text{
        opacity: 0.5;
      }
      p {
        font-style: normal;
        font-weight: normal;
        font-size: 16px;
        line-height: 20px;
        color: #000000;
        margin-bottom: 15px;
      }
    }
  }

  &__menu {
    display: grid;
    grid-template-rows: 1fr 1fr;
    grid-template-columns: 1fr 1fr 1fr 1fr;

    &-item {
      padding: 0 0 15px;
      line-height: 1.2;
      white-space: nowrap;
    }

    &-link {
      font-weight: 600;
      font-size: 16px;
      line-height: 34px;
      text-transform: uppercase;
      color: $mainBlack;
    }
  }
  &__subscribe {
    display: flex;
    align-items: center;

    &-list {
      display: flex;
      list-style: none;
      justify-content: flex-start;
      margin-right: 40px;
    }
    &-content {
      width: 220px;
      text-align: left;
      display: flex;
      flex-direction: column;
      &--text {
        p {
          font-weight: bold;
          font-size: 18px;
          line-height: 20px;
          color: #000000;
          margin-bottom: 25px;
        }
      }
    }

    &-btn {
      margin-top: 15px;
      background: $mainBlack;
      padding: 17px 25px;
      font-size: 20px;
      line-height: 14px;
      text-align: center;
      color: #FFFFFF;
    }
  }
}
@media screen and (max-width: 1020px){
  .f-footer{
    &__menu{
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr 1fr 1fr;
      justify-items: center;
    }
    &__subscribe{
      flex-direction: column;
    }
  }
}
@media screen and (max-width: 768px){
  .f-footer{
    &__row{
      flex-direction: column;
      display: flex;
      align-items: flex-start;
      &-col{
        width: 100%;
      }
    }
    &__subscribe {
      flex-direction: column;
    }
    &__menu{
      grid-template-rows: 1fr 1fr;
      grid-template-columns: 1fr 1fr 1fr 1fr;
    }
  }
}
@media screen and (max-width: 768px){
  .f-footer{
    &__menu{
      grid-template-columns: 1fr 1fr;
      grid-template-rows: 1fr 1fr 1fr 1fr;
      justify-items: center;
    }
  }
}
</style>