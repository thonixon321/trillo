<template>
  <div
    id="app"
    class="container"
  >
    <Header />
    <div class='content'>
      <SideBar />

      <main class='hotel-view'>

        <div class='gallery'>
          <figure class='gallery__item'>
            <img
              src='./assets/img/hotel-1.jpg'
              alt='Photo of hotel 1'
              class='gallery__photo'
            >
          </figure>
          <figure class='gallery__item'>
            <img
              src='./assets/img/hotel-2.jpg'
              alt='Photo of hotel 2'
              class='gallery__photo'
            >
          </figure>
          <figure class='gallery__item'>
            <img
              src='./assets/img/hotel-3.jpg'
              alt='Photo of hotel 3'
              class='gallery__photo'
            >
          </figure>
        </div>

        <div class='overview'>
          <h1 class='overview__heading'>
            Hotel Las Palmas
          </h1>
          <div class='overview__stars'>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-star"></use>
            </svg>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-star"></use>
            </svg>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-star"></use>
            </svg>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-star"></use>
            </svg>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-star"></use>
            </svg>
          </div>
          <div class='overview__location'>
            <svg class='overview__icon-star'>
              <use xlink:href="./assets/img/sprite.svg#icon-location-pin"></use>
            </svg>
            <button class='btn-inline'>Albufeira, Portugal</button>
          </div>
          <div class='overview__rating'>
            <div class='overview__rating-average'>8.6</div>
            <div class='overview__rating-count'>429 votes</div>
          </div>
        </div>

        <div class='detail'>
          <div class='description'>
            <p class='paragraph'>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Animi nisi dignissimos debitis ratione sapiente saepe. Accusantium cumque, quas, ut corporis incidunt deserunt quae architecto voluptate.
            </p>
            <p class='paragraph'>
              Accusantium cumque, quas, ut corporis incidunt deserunt quae architecto voluptate delectus, inventore iure aliquid aliquam.
            </p>
            <ul class='list'>
              <li class='list__item'>Close to the beach</li>
              <li class='list__item'>Breakfast included</li>
              <li class='list__item'>Free airport shuttle</li>
              <li class='list__item'>Free wifi in all rooms</li>
              <li class='list__item'>Air conditioning and heating</li>
              <li class='list__item'>Pets allowed</li>
              <li class='list__item'>We speak all languages</li>
              <li class='list__item'>Perfect for families</li>
            </ul>
            <div class='recommend'>
              <p class='recommend__count'>
                Lucy and 3 other friends recommend this hotel.
              </p>
              <div class='recommend__friends'>
                <img
                  src='./assets/img/user-3.jpg'
                  alt='Friend 1'
                  class="recommend__photo"
                >
                <img
                  src='./assets/img/user-4.jpg'
                  alt='Friend 1'
                  class="recommend__photo"
                >
                <img
                  src='./assets/img/user-5.jpg'
                  alt='Friend 1'
                  class="recommend__photo"
                >
                <img
                  src='./assets/img/user-6.jpg'
                  alt='Friend 1'
                  class="recommend__photo"
                >
              </div>
            </div>
          </div>

          <div class='user-reviews'>
            <figure class='review'>
              <blockquote class="review__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga doloremque architecto dicta animi, totam, itaque officia ex.</blockquote>
              <figcaption class="review__user">
                <img
                  src='./assets/img/user-1.jpg'
                  alt='User 1'
                  class='review__photo'
                >
                <div class='review__user-box'>
                  <p class='review__user-name'>Nick Smith</p>
                  <p class='review__user-date'>Feb 23rd, 2020</p>
                </div>
                <div class='review__rating'>7.8</div>
              </figcaption>
            </figure>
            <figure class='review'>
              <blockquote class="review__text">Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fuga doloremque architecto dicta animi.</blockquote>
              <figcaption class="review__user">
                <img
                  src='./assets/img/user-2.jpg'
                  alt='User 1'
                  class='review__photo'
                >
                <div class='review__user-box'>
                  <p class='review__user-name'>Mary Thomas</p>
                  <p class='review__user-date'>Sept 13th, 2020</p>
                </div>
                <div class='review__rating'>9.3</div>
              </figcaption>
            </figure>
            <button class='btn-inline'>Show all <span>&rarr;</span></button>
          </div>
        </div>
        <div class='cta'>
          <h2 class='cta__book-now'>
            Good news! We have 4 free rooms for your selected dates!
          </h2>
          <button class='btn'>
            <span class='btn__visible'>Book now</span>
            <span class='btn__invisible'>Only 4 rooms left</span>
          </button>
        </div>
      </main>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header";
import SideBar from "./components/Sidebar";
export default {
  name: "App",
  components: {
    Header,
    SideBar
  }
};
</script>

<style lang="scss">
@import "./styles/global.scss";

//////////////////////////////////////
// LIST
.list {
  list-style: none;
  margin: 3rem 0;
  padding: 3rem 0;
  border-top: var(--line);
  border-bottom: var(--line);

  display: flex;
  flex-wrap: wrap;

  &__item {
    flex: 0 0 50%;
    margin-bottom: 0.7rem;
  }

  &__item::before {
    content: "";
    display: inline-block;
    height: 1rem;
    width: 1rem;
    margin-right: 0.7rem;

    //older browsers
    // background-image: url(./assets/img/chevron-thin-right.svg);
    // background-size: cover;

    //newer browser - masks
    background-color: var(--color-primary);
    mask-image: url(./assets/img/chevron-thin-right.svg);
    mask-size: cover;
  }
}
</style>
