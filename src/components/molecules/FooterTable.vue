<template>
  <div class="footer-table">
    <div class="resultados">
      <span>Monstrando resultados 1 até 50 entre 3331 pedidos</span>
    </div>
    <div class="paginacao">
      <div class="btns"><i class="fas fa-chevron-left"></i></div>
      <div class="btns"><span>1</span></div>
      <div class="btns"><span>2</span></div>
      <div class="btns"><span>3</span></div>
      <div class="btns"><i class="fas fa-chevron-right"></i></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
$grey5: #dddddd;
$grey3: #4a555d;
.footer-table {
  height: 10vh;

  padding: 0.1rem 1rem;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  -webkit-box-shadow: 2px -8px 13px -10px rgba(0, 0, 0, 0.8);
  box-shadow: 2px -8px 13px -10px rgba(0, 0, 0, 0.8);

  .resultados {
    span {
      font-size: 13px;
    }
  }

  .paginacao {
    display: flex;

    .btns {
      padding: 0.5rem 1rem;
      border: 1px solid $grey5;
      border-radius: 5px;
      cursor: pointer;

      &:hover {
        background: $grey3;
        color: white;
      }
    }
  }
}
</style>