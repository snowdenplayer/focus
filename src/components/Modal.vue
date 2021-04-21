<template>
  <div class="modal">
      <div class="modal-work">
        <a href="#" class="modal__logo">
          <img src="../assets/images/logo.png" alt="">
        </a>
        <button class="modal__close-btn btn" @click="$emit('closeModal')">
          <svg width="30" height="30" viewBox="0 0 30 30" xmlns="http://www.w3.org/2000/svg">
            <path d="M27.3481 0.00607115L0 27.3464L2.64803 29.9952L29.9961 2.65485L27.3481 0.00607115Z"></path>
            <path d="M2.65194 0.0042971L0.00390625 2.65308L27.352 29.9934L30 27.3447L2.65194 0.0042971Z"></path>
          </svg>
        </button>
        <form class="modal__form">
          <input type="text" class="modal__input" placeholder="Поиск">
          <button class="modal__search-btn btn">
            <svg width="26" height="26" viewBox="0 0 20 20" fill="#000" xmlns="http://www.w3.org/2000/svg">
              <path d="M19.7236 18.263L16.0223 14.5658C18.8541 11.0422 18.5809 5.83127 15.3516 2.63027C13.6624 0.942928 11.4019 0 8.99236 0C6.5828 0 4.34713 0.942928 2.63312 2.63027C0.943949 4.31762 0 6.57568 0 8.98263C0 11.3896 0.943949 13.6228 2.63312 15.335C4.32229 17.0223 6.5828 17.9653 8.99236 17.9653C11.0293 17.9653 13.0166 17.2705 14.6064 16.005L18.3076 19.7022C18.5064 19.9007 18.7548 20 19.0032 20C19.2764 20 19.5248 19.9007 19.6987 19.7022C20.0962 19.2804 20.0962 18.66 19.7236 18.263ZM15.9975 8.95782C15.9975 10.8189 15.2771 12.5806 13.9605 13.8958C12.644 15.2109 10.8803 15.9305 9.0172 15.9305C7.15414 15.9305 5.39045 15.2109 4.07389 13.8958C2.75733 12.5806 2.03694 10.8189 2.03694 8.95782C2.03694 7.09678 2.75733 5.33499 4.07389 4.01985C5.39045 2.70471 7.15414 1.98511 9.0172 1.98511C10.8803 1.98511 12.644 2.70471 13.9605 4.01985C15.2771 5.33499 15.9975 7.09678 15.9975 8.95782Z"></path>
            </svg>
          </button>
        </form>
      </div>
  </div>
</template>

<script>
export default {
  name: "Modal",
}
</script>

<style scoped lang="scss">
.modal{
  width: 100%;
  height: 100vh;
  background-color: rgba(244,244,245,.97);
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: center;
  z-index: 1000;
  &-work{
    width: 80%;
  }
  &__logo{
    position: absolute;
    left: 50%;
    top: 100px;
    transform: translateX(-50%);
  }
  &__close-btn{
    position: absolute;
    top: 100px;
  }
  &__form{
    width: 100%;
    position: relative;
  }
  &__input{
    width: 100%;
    font-size: 25px;
    font-weight: 500;
    padding: 20px 30px;
    box-sizing: border-box;
    border: none;
  }
  &__search-btn{
    position: absolute;
    top: 50%;
    right: 15px;
    color: gray;
    transform: translateY(-50%);
  }
}

</style>