<template>
  <main class="main">
    <div class="container main__slider-wrapper">
      <div class="slider__items-small-wrap">
        <div
            class="slider__items-small"
            v-for="item in mainSliderContent"
            :key="item.id"
            :style="{ backgroundImage: 'url(' + item.img + ')' }"
            @click="setCuurentSlide(item)"
        >
          <p>{{ item.name }}</p>
        </div>
      </div>
      <div class="slider__items-big-wrap">
        <div
            class="slider__slide-big"
            :style="{ backgroundImage: 'linear-gradient(76.81deg, #000000 14.51%, rgba(0, 0, 0, 0) 74.23%),url(' + mainSliderContent[currentSlide].img + ')' }"
        >
          <div class="f__badge f__badge--lite">Политика</div>
          <div class="slide__header">{{ mainSliderContent[currentSlide].name }}</div>
          <div class="slider__descr">{{ mainSliderContent[currentSlide].description }}</div>
        </div>
      </div>
    </div>
    <section class="container news-big news">
      <a href="#" class="news-big__item">
        <div class="big-item__img">
          <img src="../assets/images/cardsBigNews/firstitem.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">УКраина</div>
        </div>
        <div class="big-item__header">
          Наказание карантином. Чем грозит Украине вторая волна борьбы с коронавирусом
        </div>
        <div class="big-item__time item__time">15:44</div>
      </a>
      <a href="#" class="news-big__item">
        <div class="big-item__img">
          <img src="../assets/images/cardsBigNews/secondItem.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Технологии и наука</div>
        </div>
        <div class="big-item__header">
          Заговоренная связь. Все, что известно о 5G и его влиянии на здоровье
        </div>
        <div class="big-item__time item__time">15:44</div>
      </a>
      <a href="#" class="news-big__item news-big__item-dark">
        <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
        <div class="big-item-dark__header">100</div>
        <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
          самые успешные звезды шоу-бизнеса
        </div>
      </a>
      <a href="#" class="news-big__item">
        <div class="big-item__img">
          <img src="../assets/images/cardsBigNews/fourthItem.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Политика</div>
        </div>
        <div class="big-item__header">
          Дубы и сосны. В соцсетях обсуждают сексистский скандал в "Слуге народа"
        </div>
        <div class="big-item__time item__time">15:44</div>
      </a>
    </section>
    <section class="container news-small news">
      <a href="#" class="news__item-small news__item-small--fill">
        <div class="f__badge f__badge--lite f__badge--position">УКраина</div>
        <div class="small-item__header">
          Заговоренная связь. Все, что известно о 5G и его влиянии на здоровье
        </div>
        <div class="item__time">15:44</div>
      </a>
      <a href="#" class="news__item-small">
        <div class="small-item__img">
          <img src="../assets/images/cardsSmallNews/secondItem.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Политика</div>
        </div>
        <div class="small-item__header">
          Кабмин назначил главой МОН Сергея Шкарлета в обход Рады
        </div>
        <div class="small-item__time item__time">15:44</div>
      </a>
      <a href="#" class="news__item-small">
        <div class="small-item__img">
          <img src="../assets/images/cardsSmallNews/thirdItem.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Технологии и наука</div>
        </div>
        <div class="small-item__header">
          Агент изменений. Денис Малюська — о частных СИЗО, продаже тюрем и будущем люстрации
        </div>
        <div class="small-item__time item__time">15:44</div>
      </a>
      <a href="#" class="news__item-small news__item-small--fill">
        <div class="f__badge f__badge--lite f__badge--position">УКраина</div>
        <div class="small-item__header">
          Заговоренная связь. Все, что известно о 5G и его влиянии на здоровье
        </div>
        <div class="item__time">15:44</div>
      </a>
    </section>
    <section class="container special-topic"
             :style="{'background-image': 'url('+ `${mainSliderContent[specialCurrentSlide].img}`  +')'}">
      <div class="special-topic__content">
        <div class="special-topic__left">
          <div class="special-topic__header">
            {{ mainSliderContent[specialCurrentSlide].name }}
          </div>
          <a href="#" class="special-topic__link">смотреть все материалы</a>
        </div>
        <div class="special-topic__right">
          <ul class="special-topic__list" id="special__list">
            <li class="list__item"
                v-for="item in mainSliderContent"
                :key="item.id"
                @click="changeSpecialSlide(item)"
            >
              <div class="item__header">{{ item.name }}</div>
              <div class="item__time">14:26</div>
              <div class="item__line"></div>
            </li>
          </ul>
        </div>
      </div>
    </section>
    <section class="container n-block">
      <ul class="l-list">
        <li class="l-list__item l-list__item-2">
          <div class="xl-card">
            <img src="../assets/images/aleksej.png" class="xl-card__bg-image" alt="">
            <div class="xl-card__title">Как Юлия Тимошенко меня в Египет отправила</div>
            <div class="xl-card__descr">В середине нулевых Киев переживал немыслимый ипотечный бум. Банки выдавали
              кредиты на десять и двадцать лет.
            </div>
            <div class="xl-card__author">
              <div class="xl-card__author-name">
                Алексей Газубей
              </div>
              <div class="xl-card__author-work">
                Главний редактор focus.ua
              </div>
            </div>
          </div>
        </li>
        <li class="l-list__item l-list__item-1">
          <div class="l-card">
            <div class="l-card__preview">
              <div class="f__badge f__badge--dark">Технологии и наука</div>
              <img src="../assets/images/tikTok.png" alt="">
            </div>
            <div class="l-card__main">
              <div class="l-card__title">
                <a href="#">
                  Счастье за 16 секунд. В чем секрет популярности TikTok и как соцсеть влияет на психику подростков
                </a>
              </div>
              <div class="l-card__time item__time">14:55</div>
            </div>
          </div>
          <div class="d-card">
            <div class="d-card__title">мнение</div>
            <div class="d-card__main">
              <div class="d-card__images">
                <img src="../assets/images/apostrof.png" alt="">
                <img src="../assets/images/apostrof.png" alt="">
              </div>
              <div class="d-card__text">“Too much против
                me too. Почему сексистские скандалы
                в Украине ничем не заканчиваются”
              </div>
            </div>
            <div class="d-card__author">
              <div class="d-card__author-img">
                <img src="../assets/images/authorPhoto.png" alt="">
              </div>
              <div class="d-card__author-name">Мария Бабенко</div>
            </div>
          </div>
        </li>
      </ul>
    </section>
    <section class="container news-small news">
      <a href="#" class="news__item-small">
        <div class="small-item__img">
          <img src="../assets/images/ocean.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Технологии и наука</div>
        </div>
        <div class="small-item__header">
          Новая нефть. Как ученые ищут редкие элементы на дне океана, в космосе и мусоре
        </div>
        <div class="small-item__time item__time">15:44</div>
      </a>
      <a href="#" class="news__item-small news__item-small--text">
        <div class="f__badge f__badge--dark ">Технологии и наука</div>
        <div class="small-item__header">
          Все в масках и проверка температуры: в Украине стартовала основная сессия ВНО-2020
        </div>
        <div class="small-item__descr">
          Первый тест – по математике. Для его прохождения зарегистрировались 186 072 человека.
        </div>
        <div class="item__time small-item__time">15:44</div>
      </a>
      <a href="#" class="news__item-small item__advertisment">
        <img src="../assets/images/advertising/firstItem.png" alt="">
      </a>
      <a href="#" class="news__item-small">
        <div class="small-item__img">
          <img src="../assets/images/culture.png" alt="">
          <div class="f__badge f__badge--dark f__badge--position">Культура</div>
        </div>
        <div class="small-item__header">
          Обзор Юрия Володарского: 5 книг для тех, кто предпочитает "короткий метр" в литературе
        </div>
        <div class="small-item__time item__time">15:44</div>
      </a>
    </section>
    <section class="container b-advertising">
      <div class="book__block">
        <img src="../assets/images/advertising/book1.png" alt="">
        <img src="../assets/images/advertising/book2.png" alt="">
        <img src="../assets/images/advertising/book3.png" alt="">
        <img src="../assets/images/advertising/book4.png" alt="">
      </div>
      <div class="book__text">Подпишись с другом! <span>-10% каждому</span></div>
      <button class="btn book__btn">
        Подписаться
      </button>
    </section>
    <section class="container--fluid o--block">

      <div class="container">
        <div class="o--block__title h2">Рейтинги</div>
      </div>
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
    </section>
    <section class="container--fluid u--block m-block">
      <div class="u--block__title h2">Украина</div>
      <ul class="l-list">
        <li class="l-list__item l-list__item-1">
          <div class="l-card">
            <div class="l-card__preview">
              <div class="f__badge f__badge--dark">УКраина</div>
              <img src="../assets/images/ukraine/uSecondItem.png" alt="">
            </div>
            <div class="l-card__main">
              <div class="l-card__title">
                <a href="#">
                  Выход из карантина: Кабмин разрешил открыть кинотеатры со 2 июля </a>
              </div>
              <div class="l-card__time item__time">14:55</div>
            </div>
          </div>
          <div class="l-card">
            <div class="l-card__preview">
              <div class="f__badge f__badge--dark">УКраина</div>
              <img src="../assets/images/ukraine/uFirstItem.png" alt="">
            </div>
            <div class="l-card__main">
              <div class="l-card__title">
                <a href="#">
                  Проверка доверия: владелец «Три Н» Максим Криппа о махинациях в благотворительности
                </a>
              </div>
              <div class="l-card__time item__time">14:55</div>
            </div>
          </div>
        </li>
        <li class="l-list__item l-list__item-2">
          <div class="u-xl-card">
            <div href="#" class="f__badge f__badge--lite">фото дня</div>
            <div class="u-xl-card__text">Бизнес и немного удовольствия: Grand Hotel Lviv Luxury & SPA</div>
          </div>
        </li>

      </ul>
      <div class=" news-big news">
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/ukraine/u3.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">УКраина</div>
          </div>
          <div class="big-item__header">
            Наказание карантином. Чем грозит Украине вторая волна борьбы с коронавирусом
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/ukraine/u4.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">УКраина</div>
          </div>
          <div class="big-item__header">
            Бетонная пята. Как застройщики превращают украинские города в ад
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news-big__item news-big__item-fill">
          <div class="item-fill__title">мнение</div>
          <div class="item-fill__main">
            <div class="item-fill__images">
              <img src="../assets/images/apostrof.png" alt="">
              <img src="../assets/images/apostrof.png" alt="">
            </div>
            <div class="item-fill__text">“Государство или смерть. Какой кризис станет для Украины последним”</div>
          </div>
          <div class="item-fill__author">
            <div class="item-fill__author-img">
              <img src="../assets/images/authorPhoto.png" alt="">
            </div>
            <div class="item-fill__author-name">Михаил Багинский</div>
          </div>
        </a>
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/ukraine/u5.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">Политика</div>
          </div>
          <div class="big-item__header">
            Смерть марафонца. Можно ли было спасти Екатерину Катющеву
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
      </div>
    </section>
    <section class="container--fluid o--block">
      <div class="container">
        <div class="o--block__title h2">СЕЙЧАС ПОПУЛЯРНО</div>
      </div>
      <swiper class="swiper" :options="swiperOption">
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>
        <swiper-slide class="bg-option"><a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a></swiper-slide>

        <div class="swiper-pagination" slot="pagination"></div>
        <div class="swiper-button-prev" slot="button-prev"></div>
        <div class="swiper-button-next" slot="button-next"></div>
      </swiper>
    </section>
    <section class="container--fluid  m-block">
      <div class="o--block__title h2">красивая страна</div>
      <div class="news">
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/cardsBigNews/firstitem.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">УКраина</div>
          </div>
          <div class="big-item__header">
            Наказание карантином. Чем грозит Украине вторая волна борьбы с коронавирусом
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/cardsBigNews/secondItem.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">Технологии и наука</div>
          </div>
          <div class="big-item__header">
            Небоскребы советских времен. Три маршрута к памятникам советского модернизма в Киеве
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news-big__item news-big__item-dark">
          <div class="f__badge f__badge--lite f__badge--position">Технологии и наука</div>
          <div class="big-item-dark__header">100</div>
          <div class="big-item-dark__text">Из песни слов не выкинешь. Рейтинг Фокуса:
            самые успешные звезды шоу-бизнеса
          </div>
        </a>
        <a href="#" class="news-big__item">
          <div class="big-item__img">
            <img src="../assets/images/cardsBigNews/fourthItem.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">Политика</div>
          </div>
          <div class="big-item__header">
            Как закалилась сталь. Музей Островского в Шепетовке — памятник архитектуры, а не идеологии
          </div>
          <div class="big-item__time item__time">15:44</div>
        </a>
      </div>
      <div class="swiper-loop">
        <swiper class="swiper" :options="swiperOption2">
          <swiper-slide class="l-slider__slide">
            <img src="../assets/images/mainSlider/fifth.png" alt="">
            <div class="slide__text">Ни тоски, ни жалости</div>
            <div class="slide__sub-text">Почему украинки участвуют в боях без правил</div>
          </swiper-slide>
          <swiper-slide class="l-slider__slide">
            <img src="../assets/images/mainSlider/secontItem.png" alt="">
          </swiper-slide>
          <swiper-slide class="l-slider__slide">
            <img src="../assets/images/mainSlider/thirdItem.png" alt="">
          </swiper-slide>
          <swiper-slide class="l-slider__slide">
            <img src="../assets/images/mainSlider/fourthItem.png" alt="">
          </swiper-slide>
          <div class="swiper-pagination" slot="pagination"></div>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>
      <div class="news">
        <a href="#" class="news__item-small">
          <div class="small-item__img">
            <img src="../assets/images/ocean.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">Технологии и наука</div>
          </div>
          <div class="small-item__header">
            Новая нефть. Как ученые ищут редкие элементы на дне океана, в космосе и мусоре
          </div>
          <div class="small-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news__item-small news__item-small--text">
          <div class="f__badge f__badge--dark ">Технологии и наука</div>
          <div class="small-item__header">
            Все в масках и проверка температуры: в Украине стартовала основная сессия ВНО-2020
          </div>
          <div class="small-item__descr">
            Первый тест – по математике. Для его прохождения зарегистрировались 186 072 человека.
          </div>
          <div class="item__time small-item__time">15:44</div>
        </a>
        <a href="#" class="news__item-small">
          <div class="small-item__img">
            <img src="../assets/images/culture.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">Культура</div>
          </div>
          <div class="small-item__header">
            Обзор Юрия Володарского: 5 книг для тех, кто предпочитает "короткий метр" в литературе
          </div>
          <div class="small-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news__item-small item__advertisment">
          <img src="../assets/images/advertising/firstItem.png" alt="">
        </a>
        <a href="#" class="news__item-small">
          <div class="small-item__img">
            <img src="../assets/images/ocean.png" alt="">
            <div class="f__badge f__badge--dark f__badge--position">авто</div>
          </div>
          <div class="small-item__header">
            Новая нефть. Как ученые ищут редкие элементы на дне океана, в космосе и мусоре
          </div>
          <div class="small-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news__item-small item__advertisment">
          <img src="../assets/images/advertising/firstItem.png" alt="">
        </a>
        <a href="#" class="news__item-small news__item-small-bg">
          <img class="item-small-bg__image" src="../assets/images/cardsSmallNews/fifthItem.png" alt="">
          <a class="f__badge f__badge--lite f__badge--position">Длинный фокус</a>
          <div class="small-item__header item-small-bg__header">
            КОГДА ТЫ ДОМА: как «умный дом» LG приходит на выручку во времена турбулентности
          </div>
          <div class="small-item__time item__time">15:44</div>
        </a>
        <a href="#" class="news__item-small news__item-small--text">
          <div class="f__badge f__badge--dark ">Архивариус</div>
          <div class="small-item__header">
            Мосты всей жизни. В жизни Евгения Патона не было случайностей
          </div>
          <div class="small-item__descr">
            Его называли человеком из будущего, гениальные идеи которого по сей день используются при изготовлении
            сверхпрочных сплавов для мостов, железных дорог и даже космических станций.
          </div>
          <div class="item__time small-item__time">15:44</div>
        </a>

      </div>

      <div class="a-block">
        <div class="a-block__inner">
          <img src="../assets/images/advertising2.png" alt="">
          <img src="../assets/images/advertising3.png" alt="">
        </div>
      </div>
    </section>
  </main>
</template>

<script>
import {Swiper, SwiperSlide} from 'vue-awesome-swiper'
import 'swiper/swiper-bundle.min.css'

export default {
  name: "Main",
  components: {
    Swiper,
    SwiperSlide
  },
  data() {
    return {
      currentSlide: 0,
      specialCurrentSlide: 0,
      swiperOption: {
        slidesPerView: 1,
        spaceBetween: 10,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        },
        breakpoints: {
          980: {
            slidesPerView: 3,
            spaceBetween: 30
          },
          700: {
            slidesPerView: 2,
            spaceBetween: 20
          },

        }
      },
      swiperOption2: {
        slidesPerView: 1,
        spaceBetween: 30,
        loop: true,
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      },
      mainSliderContent: [
        {
          id: 0,
          name: 'Леди в законе. Особый статус для жены президетна',
          description: 'Владимир Зеленский загорелся идеей разработки закона о первой леди. Для чего ему ' +
              'это понадобилось, и какие права и обязанности возлагаются на супругу главы государства в Украине ',
          img: require('../assets/images/mainSlider/firstItem.png')
        },
        {
          id: 1,
          name: 'Взрыв на Позняках в Киеве',
          description: 'Владимир Зеленский загорелся идеей разработки закона о первой леди. Для чего ему ' +
              'это понадобилось, и какие права и обязанности возлагаются на супругу главы государства в Украине ',
          img: require('../assets/images/mainSlider/fourthItem.png')
        },
        {
          id: 2,
          name: 'Потоп на западной Украине',
          description: 'Владимир Зеленский загорелся идеей разработки закона о первой леди. Для чего ему ' +
              'это понадобилось, и какие права и обязанности возлагаются на супругу главы государства в Украине ',
          img: require('../assets/images/mainSlider/thirdItem.png')
        },
        {
          id: 3,
          name: 'Цифровая трансформация бизнеса Украины',
          description: 'Владимир Зеленский загорелся идеей разработки закона о первой леди. Для чего ему ' +
              'это понадобилось, и какие права и обязанности возлагаются на супругу главы государства в Украине ',
          img: require('../assets/images/mainSlider/secontItem.png')
        }
      ],
      currentBgImageSlide: require('../assets/images/mainSlider/thirdItem.png')
    }
  },
  methods: {
    setCuurentSlide(el) {
      this.currentSlide = el.id
    },
    startSlide() {
      setInterval(() => {
        if (this.currentSlide < this.mainSliderContent.length - 1) {
          this.currentSlide += 1
        } else {
          this.currentSlide = 0;
        }
      }, 7000)
    },
    changeSpecialSlide(item) {
      this.specialCurrentSlide = item.id
    },
  },
  mounted: function () {
    this.startSlide();

  },
  watch: {
    currentSlide() {
      let slides = document.querySelectorAll('.slider__items-small')
      slides[this.currentSlide].classList.add('active')
      slides.forEach(x => {
        if (x.classList.contains('active')) {
          if (x !== slides[this.currentSlide]) {
            x.classList.remove('active')
          }
        }
      })
    }
  }

}
</script>

<style scoped lang="scss">
@import "../assets/styles/variables";


main {
  padding-top: 20px;
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: center;


  .main__slider-wrapper {
    width: 100%;
    margin-bottom: 40px;
  }

  .f__badge {
    position: relative;
    z-index: 5;
  }

  .slider__items-small-wrap {
    display: flex;
    justify-content: space-between;
  }

  .slider__items-small {
    padding: 12px 18px;
    width: 24%;
    height: 60px;
    display: flex;
    justify-content: center;
    align-items: center;
    text-align: center;
    font-weight: bold;
    font-size: 16px;
    line-height: 20px;
    color: #FFFFFF;
    background-repeat: no-repeat;
    background-position: 0 -25px;
    background-size: cover;
    box-sizing: border-box;
    cursor: pointer;

    p {
      z-index: 5;
    }
  }

  .active {
    position: relative;

    &:before {
      content: '';
      position: absolute;
      top: 0;
      left: 0;
      height: 100%;
      background: rgba(0, 0, 0, 0.5);
      border-bottom: 2px solid red;
      box-sizing: border-box;
      opacity: 0.7;
      animation-name: paintBlock;
      animation-duration: 7s;
      animation-timing-function: linear;
    }

    @keyframes paintBlock {
      from {
        width: 0;
      }
      to {
        width: 100%;

      }
    }
  }

  .slider__items-big-wrap {
    margin-top: 15px;
    width: 100%;
    height: 466px;
    position: relative;

  }

  .slider__slide-big {
    padding: 30px 30px;
    background-size: cover;
    min-width: 100%;
    height: 100%;

  }

  .slide__header {
    margin-top: 20px;
    font-weight: bold;
    font-size: 36px;
    line-height: 40px;
    text-align: left;
    max-width: 600px;
    color: $mainWhite;
  }

  .slider__descr {
    margin-top: 30px;
    font-size: 20px;
    line-height: 24px;
    color: $mainWhite;
    max-width: 600px;
  }

  .news {
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
  }

  .news-big {
    &__item {
      display: flex;
      flex-direction: column;
      padding-bottom: 9px;
      width: 300px;
      margin-left: 5px;
      margin-right: 5px;
      min-height: 400px;
      margin-bottom: 10px;
      border-bottom: 1px solid white;

      .big-item__time {
        margin-top: auto;
      }

      .big-item__img {
        margin-bottom: 10px;
        position: relative;

        img {
          width: 100%;
          height: 260px;
        }

        .f__badge--position {
          position: absolute;
          bottom: 20px;
          left: 17px;
        }
      }

      .big-item__header {
        font-weight: 600;
        font-size: 20px;
        line-height: 24px;
        color: $mainBlack
      }


    }

    &__item-fill {
      display: flex;
      align-items: center;
      justify-content: space-between;
      padding: 26px 25px;
      box-sizing: border-box;
      background-color: $mainBlack;
      border-bottom: none;
    }

    .item-fill__title {
      font-size: 14px;
      line-height: 14px;
      text-align: center;
      text-transform: uppercase;
      color: $mainWhite;
    }

    .item-fill__main {
      display: flex;
      flex-direction: column;
      align-items: center;
    }

    .item-fill__images {
      img {
        margin-right: 3px;
      }
    }

    .item-fill__text {
      margin-top: 20px;
      font-weight: bold;
      font-size: 20px;
      line-height: 22px;
      text-align: center;
      color: $mainWhite;
    }

    .item-fill__author {
      display: flex;
      flex-direction: column;
      align-items: center;

      &-name {
        margin-top: 8px;
        font-weight: normal;
        font-size: 14px;
        line-height: 18px;
        color: #FFFFFF;
      }
    }

    &__item-dark {
      background-image: url('../assets/images/cardsBigNews/thirdItem.png');
      background-size: cover;
      padding: 0 15px 33px;
      position: relative;
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;

      .f__badge--position {
        position: absolute;
        left: 25px;
        top: 15px;
      }

      .big-item-dark__header {
        font-size: 100px;
        color: $mainWhite;
      }

      .big-item-dark__text {
        font-size: 20px;
        color: $mainWhite;
      }
    }
  }

  .news {

    &__item-small {
      min-height: 290px;
      width: 300px;
      margin-left: 5px;
      margin-right: 5px;
      margin-bottom: 10px;
      box-sizing: border-box;
      display: flex;
      flex-direction: column;
      border-bottom: 1px solid $mainWhite;
      padding-bottom: 10px;
    }

    &__item-small-bg {
      border-bottom: none;
      position: relative;
      padding: 18px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      .item-small-bg__image{
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
      }
      .f__badge{
        position: absolute;
        top: 20px;
        left: 15px;
      }
      .item-small-bg__header{
        position: absolute;
        max-width: 250px;
        color: $mainWhite!important;
      }
    }

    &__item-small--text {
      .small-item__header {
        margin-top: 35px;
      }

      .f__badge {
        position: absolute;
      }
    }

    .small-item__header {
      font-weight: 600;
      font-size: 20px;
      line-height: 24px;
      margin-bottom: 20px;
      color: #000000;
    }

    .small-item__img {
      position: relative;
      margin-bottom: 10px;

      .f__badge--position {
        position: absolute;
        bottom: 20px;
        left: 15px;
      }
    }

    .small-item__descr {
      font-size: 16px;
      line-height: 20px;
      color: $mainBlack;
    }

    .small-item__time {
      margin-top: auto;
    }

    &__item-small--fill {
      background-image: url('../assets/images/cardsSmallNews/firstItem.png');
      background-size: cover;
      position: relative;
      padding: 15px 20px;
      display: flex;
      flex-direction: column;
      justify-content: flex-end;
      border-bottom: none;

      &:last-child {
        background-image: url('../assets/images/cardsSmallNews/fouthItem.png');
      }

      .f__badge--position {
        position: absolute;
        top: 20px;
        left: 15px;
      }

      .small-item__header {
        color: $mainWhite;
        font-size: 22px;
        line-height: 24px;
      }

      .item__time {
        color: #FFFFFF;
        opacity: 0.5;
      }
    }
  }

  .special-topic {
    display: flex;
    justify-content: center;
    margin-top: 40px;
    margin-bottom: 50px;
    height: 300px;
    width: 100%;
    background-size: cover;
    background-position: center;
    overflow: hidden;
    box-sizing: border-box;
    position: relative;

    &:after {
      content: '';
      position: absolute;
      width: 100%;
      height: 100%;
      background: rgba(0, 0, 0, 0.65);
      z-index: 1;
    }

    &__content {
      position: absolute;
      z-index: 3;
      width: 100%;
      height: 100%;
      padding-left: 17px;
      padding-right: 20px;
      box-sizing: border-box;
      display: flex;
    }

    &__left {
      max-width: 450px;
    }

    &__right {
      display: flex;
      justify-content: flex-end;
      flex-grow: 1;
      padding: 20px 0;
    }

    &__list {
      max-height: 100%;
      overflow-y: auto;
      max-width: 370px;

      &::-webkit-scrollbar {
        width: 5px;
        background-color: rgba(255, 255, 255, 0.25);
      }

      &::-webkit-scrollbar-thumb {

        background-color: #ED3237;
      }

      .list__item {
        font-weight: 500;
        font-size: 20px;
        line-height: 24px;
        color: #FFFFFF;
        cursor: pointer;
        transition: all 0.3s;

        &:hover {
          color: gray;
        }

        .item__time {

          margin: 20px 0;
          color: $mainWhite;
          opacity: 0.5;
        }

        .item__line {
          width: 50px;
          height: 1px;
          background: #FFFFFF;
          opacity: 0.5;
          margin-bottom: 10px;
        }
      }
    }

    &__header {
      font-weight: 500;
      margin-top: 46px;
      font-size: 40px;
      line-height: 48px;
      text-transform: uppercase;
      color: #FFFFFF;
    }

    &__link {
      display: inline-block;
      margin-top: 60px;
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 14px;
      text-transform: uppercase;
      color: #FFFFFF;
      opacity: 0.5;
    }

  }

  .l-list {
    display: flex;
    justify-content: space-between;
    margin-bottom: 36px;
    box-sizing: border-box;

    &__item {
      min-height: 400px;
      box-sizing: border-box;
      margin-left: 5px;
      margin-right: 5px;
    }

    &__item-2, &__item-1 {
      width: 49%;
    }

    &__item-1 {
      display: flex;
      justify-content: space-between;
    }

    .l-card, .xl-card, .d-card {
      height: 100%;
      display: flex;
      flex-direction: column;
      box-sizing: border-box;
    }

    .l-card, .d-card {
      width: 49%;
      min-height: 400px;
    }

    .xl-card {
      width: 100%;
      position: relative;
    }

    .l-card {
      margin-bottom: 10px;

      &__preview {
        position: relative;
        overflow: hidden;

        .f__badge {
          position: absolute;
          bottom: 25px;
          left: 14px;
        }

        img {
          height: 260px;
          width: 300px;
        }
      }

      &__main {
        display: flex;
        flex-direction: column;
        flex-grow: 1;
        padding-bottom: 10px;
        border-bottom: 1px solid $mainWhite;
      }

      &__title {
        margin-top: 10px;
        margin-bottom: 15px;

        a {
          font-weight: 600;
          font-size: 20px;
          line-height: 22px;
          color: $mainBlack;
        }
      }

      &__time {
        margin-top: auto;
      }
    }

    .d-card {
      background: #060606;
      justify-content: space-between;
      padding: 26px 32px;
      align-items: center;
      margin-bottom: 10px;

      &__title {
        font-weight: bold;
        font-size: 14px;
        line-height: 14px;
        text-align: center;
        text-transform: uppercase;
        color: #FFFFFF;
      }

      &__main {
        display: flex;
        flex-direction: column;
        align-items: center;
        margin-top: 70px;
      }

      &__images {
        margin-bottom: 20px;

        img:first-child {
          margin-right: 4px;
        }
      }

      &__text {
        font-weight: bold;
        font-size: 20px;
        line-height: 22px;
        text-align: center;
        color: #FFFFFF;
      }

      &__author {
        margin-top: 55px;
        display: flex;
        flex-direction: column;
        align-items: center;

        &-name {
          margin-top: 5px;
          font-weight: 500;
          font-size: 14px;
          line-height: 18px;
          color: #FFFFFF;
        }
      }

    }

    .xl-card {
      position: relative;
      z-index: 4;
      overflow: hidden;
      padding: 40px 22px;
      align-items: flex-end;
      flex-direction: column;
      border: 2px solid #F4F4F4;

      &::after {
        content: "";
        position: absolute;
        bottom: 0;
        left: 0;
        width: 100%;
        background: $mainBlack;
        height: 136px;
        z-index: 1;
      }

      &::before {
        content: "";
        position: absolute;
        top: 100px;
        left: 0;
        width: 150px;
        background: $mainBlack;
        height: 300px;
        z-index: 1;
      }

      &__bg-image {
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 2;
      }

      &__title {
        font-weight: bold;
        font-size: 25px;
        line-height: 31px;
        max-width: 314px;
        color: #000000;
      }

      &__descr {
        margin-top: 32px;
        font-weight: normal;
        font-size: 18px;
        line-height: 23px;
        max-width: 314px;
        color: #000000;

      }

      &__author {
        align-self: flex-end;
        justify-self: flex-end;
        margin-top: auto;
        position: relative;
        z-index: 5;

        &-name {
          font-weight: bold;
          font-size: 16px;
          line-height: 20px;
          text-align: right;
          color: #FFFFFF;
        }

        &-work {
          margin-top: 6px;
          font-size: 14px;
          line-height: 18px;
          text-align: right;
          max-width: 170px;
          color: rgba(255, 255, 255, 0.75);
        }
      }
    }
  }

  .b-advertising {
    width: 100%;
    margin-top: 45px;
    margin-bottom: 40px;
    min-height: 116px;
    background: #ED3237;
    padding: 0 54px;
    box-sizing: border-box;
    display: flex;
    align-items: center;
    justify-content: space-between;
    overflow: hidden;

    .book__block {
      align-self: flex-end;
    }

    .book__btn {
      padding: 17px 50px;
      font-size: 20px;
      line-height: 14px;
      text-align: center;
      color: #FFFFFF;
      background: #000000;
    }

    .book__text {
      flex-grow: 1;
      font-size: 24px;
      line-height: 14px;
      margin-bottom: 5px;
      color: #FFFFFF;
      display: flex;
      flex-direction: column;
      align-items: center;

      span {
        margin-top: 10px;
        font-size: 16px;
        line-height: 116.6%;
        color: #FFFFFF;
      }
    }
  }

  .item__advertisment {
    border-bottom: none;
  }
  .a-block{
    margin-top: 40px;
    padding: 24px 150px;
    background: $mainGray;
    display: flex;
    justify-content: space-between;
    align-items: center;
    &__inner{
      background: #050A14;
      flex-grow: 1;
      display: flex;
      justify-content: space-around;
    }
  }

  .o--block {
    background: $mainGray;
    padding-top: 50px;
    padding-bottom: 50px;

    &__title {
      margin-bottom: 40px;
    }
  }

  .bg-option {
    height: fit-content;
    display: flex;
    justify-content: center;
  }

  .swiper-button-prev {
    left: 0;

    &:after {
      content: url("../assets/images/arrowRight.png");
      transform: rotateY(180deg);
    }
  }

  .swiper-button-next {
    right: 0;

    &:after {
      content: url("../assets/images/arrowRight.png");
    }
  }

  .u--block {
    &__title {
      margin-bottom: 26px;
    }

    .l-list__item-2 {
      background-image: url('../assets/images/ukraine/lviv.png');
      background-repeat: no-repeat;
      background-size: cover;
      position: relative;
    }

    .u-xl-card {
      padding: 20px 15px;

      .f__badge {
        position: absolute;
        top: 20px;
        left: 15px;
      }

      &__text {
        position: absolute;
        left: 15px;
        bottom: 70px;
        font-weight: bold;
        max-width: 420px;
        font-size: 24px;
        line-height: 30px;
        color: #FFFFFF;
      }
    }

  }

  .swiper-loop {
    margin-bottom: 50px;

    .swiper-slide {
      height: 400px;
      position: relative;
      display: flex;
      flex-direction: column;
      align-items: center;
      justify-content: center;

      img {
        position: absolute;
        top: 0;
        left: 0;
        bottom: 0;
        right: 0;
        width: 100%;
        height: fit-content;
      }

      .slide__text {
        position: relative;
        z-index: 5;
        font-weight: bold;
        font-size: 54px;
        line-height: 40px;
        color: #FFFFFF;
      }

      .slide__sub-text {
        margin-top: 20px;
        position: relative;
        z-index: 5;
        font-weight: 500;
        font-size: 24px;
        line-height: 24px;
        color: #FFFFFF;
      }
    }

    .swiper-button-prev {
      left: 35px;

      &:after {
        content: url("../assets/images/arrowRightLite.png");
      }
    }

    .swiper-button-next {
      right: 35px;

      &:after {
        content: url("../assets/images/arrowRightLite.png");
      }
    }
  }
}

@media screen and (max-width: 1200px) {
  main {
    .l-list {
      flex-direction: column;
      align-items: center;

      &__item {
        width: 100%;
      }

      &__item-1 {
        justify-content: space-around;
        flex-wrap: wrap;
      }

      .l-card, .d-card {
        width: 300px;
      }

      .xl-card {
        height: 350px;

        &__title {
          max-width: 400px;
        }

        &__descr {
          min-width: 300px;
          max-width: 400px;
        }
      }

      .xl-card:before {
        top: 0;
      }
    }

    .b-advertising {
      padding: 0 10px;

      .book__block {
        align-self: flex-end;
      }
    }

  }
}

@media screen and (max-width: 960px) {
  main {
    .news {
      justify-content: space-around;
    }

    .b-advertising {
      flex-direction: column-reverse;
      padding: 15px 0 0 0;

      .book__block {
        align-self: center;
        flex-grow: 1;
      }

      .book__btn {
        margin-bottom: 10px;
      }
    }
  }
}

@media screen and (max-width: 768px) {
  main {
    .slider__items-small-wrap {
      flex-wrap: wrap;
    }

    .slider__items-small {
      width: 48%;
      margin-bottom: 5px;
    }

    .special-topic {
      &__content {
        display: flex;
        flex-direction: column;
      }

      &__left {
        max-width: 100%;
      }

      &__right {
        width: 100%;
        justify-content: center;
      }

      &__list {
        align-self: flex-end;
        display: flex;
        max-width: 100%;
        justify-content: space-around;
        max-height: 100px;
        overflow-x: auto;

        &::-webkit-scrollbar {
          height: 5px;
          background-color: rgba(255, 255, 255, 0.25);
        }

        &::-webkit-scrollbar-thumb {
          background-color: #ED3237;
        }

        .list__item {
          font-weight: 500;
          min-height: 50px;
          font-size: 16px;
          line-height: 20px;
          display: flex;
          flex-direction: column;
          min-width: 50%;

          &:hover {
            font-size: 22px;
          }

          .item__time {
            margin-bottom: 10px;
            margin-top: auto;
          }
        }
      }

      &__header {
        margin-top: 20px;
        font-size: 20px;
        line-height: 35px;
      }

      &__link {
        display: inline-block;
        margin-top: 60px;
        font-style: normal;
        font-weight: 500;
        font-size: 16px;
        line-height: 14px;
        text-transform: uppercase;
        color: #FFFFFF;
        opacity: 0.5;
      }
    }

    .n-block {
      .l-list {
        .xl-card {
          padding: 10px;

          &__bg-image {
            width: 200px;
            height: 200px;
            bottom: -6px;
          }

          &:before {
            display: none;
          }
        }
      }
    }

    .swiper-loop {
      .swiper-slide {
        padding: 20px;

        .slide__text {
          margin-top: 35px;
          font-size: 35px;
        }

        .slide__sub-text {
          text-align: center;
          font-size: 20px;
        }
      }
    }
    .a-block{
      padding: 24px 50px;
    }
  }
}

@media screen and (max-width: 520px) {
  main {
    padding-top: 10px;

    .slider__items-small-wrap {
      flex-wrap: wrap;
    }

    .slider__items-small {
      width: 100%;
      margin-bottom: 5px;
    }

    .slider__items-big-wrap {
      margin-top: 5px;
    }

    .special-topic {
      margin-bottom: 20px;

      &__header {
        font-size: 18px;
        line-height: 20px;
      }
    }

    .n-block {
      .l-list {
        .l-list__item-1 {
          flex-direction: column;
          align-items: center;
        }

        .xl-card {
          &__bg-image {
            height: 180px;
            width: 180px;
          }

          &__title {
            max-width: 100%;
          }

          &__descr {
            max-width: 100%;
            margin-top: 15px;
          }
        }
      }
    }

    .b-advertising {
      position: relative;
      overflow: hidden;

      .book__block {
        position: absolute;
        bottom: -50px;
        left: 50%;
        transform: translateX(-50%);
        display: flex;
      }

      .book__btn {
        z-index: 5;
      }

      .book__text {
        z-index: 10;
        margin-bottom: 50px;
      }
    }

    .swiper-loop {
      .swiper-slide {
        padding: 20px;
        img{
          height: auto;
          width: auto;
        }

        .slide__text {
          margin-top: 60px;
          font-size: 21px;
        }

        .slide__sub-text {
          text-align: center;
          font-size: 16px;
        }
      }
    }

    .a-block{
      padding: 10px;
      &__inner{
        align-items: center;
        height: 100%;
       img{
         height: 50%;
         width: 50%;
       }
      }
    }
  }
}
</style>