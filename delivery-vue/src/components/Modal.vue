<template>

  <div class="cart-modal_overlay" :class="{open: isOpen}" @click.self="closeModal()">
        <div class="cart-modal">
          <div class="cart-modal-header">
            <div class="cart-modal-header-title">Корзина</div>
            <span class="cart-modal-header-close" @click="closeModal()">
              <img src="../assets/img/icon/close.svg" alt="close">
            </span>
          </div>

          <div class="cart-modal-body">
            <div class="cart-item">
              <p class="cart-item-title">Ролл угорь стандарт</p>

              <div class="cart-item_controls">
                <div class="cart-item_controls-price">250 ₽</div>
                <button class="btn btn-outline"> - </button>
                <div class="cart-item_controls-count">1</div>
                <button class="btn btn-outline"> + </button>
              </div>
            </div>

            <div class="cart-item">
              <p class="cart-item-title">Ролл угорь стандарт</p>
              <div class="cart-item_controls">
                <div class="cart-item_controls-price">250 ₽</div>
                <button class="btn btn-outline"> - </button>
                <div class="cart-item_controls-count">1</div>
                <button class="btn btn-outline"> + </button>
              </div>
            </div>
          </div>

          <div class="cart-modal-footer">
            <div class="cart-modal-footer-price">1250 ₽</div>
            <div class="cart-modal-footer-controls">
              <button class="btn btn-primary">
                Оформить заказ
              </button>
              <button class="btn btn-outline">
                Отмена
              </button>
            </div>
          </div>
        </div>
      </div>

</template>


<script setup>
// #######################################################
// export default {
// }

const {isOpen} = defineProps({isOpen: Boolean})

const emit = defineEmits(['toggleModal'])
const closeModal = () => { emit('toggleModal') }



// #######################################################
</script>


<style scoped>

.cart-modal_overlay {
  display: none;
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  background: #000000ba;
  align-items: center;
  justify-content: center;
}

.cart-modal_overlay.open {
  display: flex;
}

.cart-modal {
  width: 100%;
  max-width: 780px;
  padding: 40px 45px;
  border-radius: 5px;
  background: #FFF;
}

.cart-modal-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  margin-bottom: 48px;
}

.cart-modal-header-title {
  color: #000;
  font-size: 36px;
  font-weight: 700;
  margin: 0;
}

.cart-modal-header-close {
  cursor: pointer;
}

.cart-modal-body {}

.cart-item {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
}

.cart-item:not(:last-child) {
  padding-bottom: 10px;
  margin-bottom: 10px;
  border-bottom: 1px solid #d9d9d9;
}

.cart-item-title {
  color: #000;
  font-size: 18px;
  font-weight: 400;
  line-height: 32px;
  margin: 0;
}

.cart-item_controls {
  display: flex;
  align-items: center;
}

.cart-item_controls button {
  border-radius: 2px;
  border: 1px solid #40A9FF;
  color: #40A9FF;
  background: #FFF;
}

.cart-item_controls-price {
  color: #000;
  font-size: 20px;
  font-weight: 700;
  line-height: 32px;
  margin-right: 47px;
}

.cart-item_controls-count {
  color: #000;
  text-align: center;
  font-size: 16px;
  font-weight: 400;
  line-height: 24px;
  margin: 0 15px;
}

.cart-modal-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;
  gap: 10px;
  margin-top: 50px;
}

.cart-modal-footer-price {
  border-radius: 5px;
  background: #262626;
  color: #FAFAFA;
  font-size: 20px;
  font-weight: 700; 
  padding: 15px 20px;
}

.cart-modal-footer-controls {
  display: flex;
  align-items: center;
  gap: 10px;
}

</style>

