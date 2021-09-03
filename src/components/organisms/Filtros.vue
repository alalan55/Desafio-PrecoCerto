<template>
  <div class="filtros">
    <div class="bloco-1">
      <div class="title">
        <span>Formação de Preços</span>
      </div>

      <button class="btn-sincronizar">SINCRONIZAR PRODUTOS</button>
    </div>

    <div class="bloco-2">
      <div class="filtros-bloco-2">
        <div class="input-pedido">
          <input type="text" placeholder="Buscar pedido" />
          <i class="fas fa-search"></i>
        </div>

        <select id="estado" name="estado" class="select">
          <option disabled value="">Estado</option>
          <option value="0">Estado</option>
        </select>

        <select id="fornecedor" class="select">
          <option disabled value="">Fornecedor</option>
          <option value="0">Fornecedor</option>
        </select>

        <div class="produto-prejuizo">
          <input type="checkbox" name="teste" id="" /><span
            >Produtos com prejuizo</span
          >
        </div>

        <div class="btn-filtrar">
          <button><i class="fas fa-filter"></i> FILTRAR</button>
        </div>
      </div>

      <div class="informacoes-pis-bloco2">
        <div class="texto-pis">
          <span><b class="title-pis">PIS:</b> 2%</span>
          <span><b class="title-pis">CONFINS:</b> 2%</span>
          <span><b class="title-pis">COMISSÃO:</b> 2%</span>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="scss" scoped>
$grey1: #f2f2f2;
$grey2: #9d9d9d;
$grey3: #4a555d;
$grey4: #9faab2;
$grey5: #dddddd;
$grey6: #CACACA;

.filtros {
  padding-top: 5rem;
  height: calc(25vh - 80px);
  max-width: 1450px;
  margin: 0 auto;
  display: flex;
  align-items: flex-end;
  justify-content: space-between;

  .bloco-1 {
    .title {
      margin-bottom: 0.6rem;
      span {
        font-size: 2rem;
        font-weight: 300;
      }
    }
    .btn-sincronizar {
      width: auto;
      background: none;
      padding: 0.5rem 1.5rem;
      border: 3px solid $grey1;
      border-radius: 5px;
      font-weight: 700;
      font-family: "Poppins", sans-serif;
      cursor: pointer;
    }
  }
  .bloco-2 {
    // border: 1px solid red;
    display: flex;
    flex-direction: column;
    position: relative;

    .filtros-bloco-2 {
      display: flex;

      &:not(:nth-child(4)){
         align-items: flex-end;
      }

      .input-pedido {
        position: relative;
        input {
          position: relative;
          border-top: none;
          border-left: none;
          border-right: none;
          padding: 0.3rem 2rem;
          border-bottom: 3px solid $grey6;
          font-family: "Poppins";
          color: $grey2;

          &:focus {
            outline: none;
          }
        }
        i {
          position: absolute;
          left: 0;
          bottom: 10px;
          color: $grey2;
        }
      }
      .select {
        border: 3px solid $grey1;
        border-radius: 10px;
        padding: 0.5rem 5rem 0.5rem 0.5rem;
        color: grey;
        margin: 0 0.4rem;
        font-family: 'Poppins';
      }
      .produto-prejuizo {
        margin: 0 .5rem;
        display: flex;
        align-items: center;
        justify-content: center;
        height:40px;

        input {
          display: block;
          margin: 0 0.3rem;
        }

        span {
          color: $grey2;
          font-size: 14px;
        }
      }
      .btn-filtrar {
        display: flex;
        align-items: center;
        justify-content: center;
        button {
          cursor: pointer;
          padding: 0.7rem 1rem;
          background: $grey1;
          border-radius: 10px;
          border: none;
          font-weight: 800;
          color: $grey3;

          i {
            color: $grey2;
          }
        }
      }
    }

    .informacoes-pis-bloco2 {
      // border: 1px solid red;
      //  text-align: right;
      position: absolute;
      bottom: -40px;
      right: 0;

      .texto-pis {
        span {
          display: inline-block;
          margin: 0 .6rem;
          font-weight: 600;
          font-size: 14px;
          .title-pis {
            color: #0047BB;
          }
        }
      }
    }
  }
}
</style>