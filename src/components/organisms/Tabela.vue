<template>
  <div>
    <div class="lista">
      <div class="conteudo-lista">
        <table>
          <thead>
            <tr>
              <th class="cell-cod"><input type="checkbox" name="" id="" /> <span>Cód</span></th>
              <th class="cell-produto p-hea"><div class="p-head">Produto  <img src="../../assets/img/selector.svg" alt=""></div></th>
              <th class="cell-custo"><div class="p-head">Custo  <img src="../../assets/img/selector.svg" alt=""></div></th>
              <th class="cell-frete"><div class="p-head">Frete  <img src="../../assets/img/selector.svg" alt=""></div></th>
              <th><div class="p-head">Margem  <img src="../../assets/img/selector.svg" alt=""></div></th>
              <th><div class="p-head">Preço final  <img src="../../assets/img/selector.svg" alt=""></div></th>
            </tr>
          </thead>
          <tbody>
            <tr class="body">
              <td class="cell-cod">
                <input type="checkbox" name="" id="" /> <span>ABCDEFGH</span>
              </td>
              <td class="cell-produto"><span class="title-table">10 Produtos de teste</span></td>
              <td class="cell-custo"><span class="title-table">R$200,00</span></td>
              <!-- <td class="cell-frete"><span class="title-table">R$192,00</span></td> -->
              <td class="cell-frete"><div class="title-table c-frete"> <span class="price">R$192,00</span><span class="price">R$192,00</span></div></td>
              <td class="cell-margem"><div class="c-margem"><span>R$200,00</span><span>50%</span></div></td>
              <td class="final-price">
                  <div class="teste">

                <span class="title-table">R$400,00</span>
                <button>Enviar preço</button>
                  </div>
              </td>
            </tr>
          </tbody>
        </table>
      </div>
      <div class="footer-lista">
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

.lista {
  height: 75vh;
  border: 1px solid transparent;
  max-width: 1450px;
  margin: 0 auto;
  position: relative;
  .conteudo-lista {
    margin-top: 50px;
    .cabecalho-lista {
      background: $grey4;
      height: 40px;

      display: flex;
      align-items: center;
      justify-content: space-between;
      color: white;
      font-weight: 200;

      & > div {
        width: 100%;
        margin: 0 0.5rem;
        border: 1px solid red;
      }
    }
    .itens {
      li {
        border: 1px solid red;
        list-style: none;
        border-bottom: 1px solid $grey5;
        padding: 1.5rem 0.5rem;
        display: flex;
        align-items: center;
        justify-content: space-between;
      }
    }

    table {
      width: 100%;
      border-collapse: collapse;
      display: block;
      table-layout: fixed;
      margin: 0;
      padding: 0;

      .cell-cod{
          width: 15rem;
          span{
           // padding-left: ;
            border: 1px solid;
          }
      }

      .cell-produto{
          width: 70rem;
      }
      .cell-frete, .cell-custo{
          width: 15rem;
      }
      .c-frete{
        display: flex;
        flex-direction: column;
      }
      .c-margem{
        border: 1px solid;
        max-width: 50%;
        display: flex;
        span{
          margin-right: .5rem;
          &:nth-child(2){
           // border: 1px solid red;
            // padding-left: .5rem;
          }
        }
      }
      .final-price{

          // .teste{
          //     display: flex;
          //     align-items: center;
          //     justify-content: space-evenly;
          // }
      }
     thead{
         .p-head{
           //  border: 1px solid red;
            display: flex;
             align-items: center;


             img{
                 width: 20px;
                 //border: 1px solid yellow;
                 margin-left: .2rem;
                 cursor: pointer;
             }
         }
     }
      tbody {
        display: block;
        overflow-y: scroll;
        height: 50vh;
        width: 100%;

        &::-webkit-scrollbar {
          width: 0;
        }
      }

      th {
        background: $grey4;
        color: white;
        padding: 0.5rem 0.5rem;
        font-weight: 200;
      }
      td {
        padding: 0.8rem 0.5rem;
        border-bottom: 1px solid $grey5;
        button {
          background: none;
          padding: 0.3rem;
          border-radius: 5px;
          border: 1px solid $grey2;
          font-family: "Poppins";
        }
        .title-table {
          font-size: 14px;
        }
      }

      td,
      th {
        text-align: left;
        width: 500px;
        min-width: 100px;
      }
    }
  }

  .footer-lista {
      padding: .1rem 1rem;
      bottom: 0;
     // border: 1px solid red;
    display: flex;
    align-items: center;
    justify-content: space-between;
    position: absolute;
    width: 100%;
    height: 8vh;
    -webkit-box-shadow: 2px -8px 13px -10px rgba(0, 0, 0, 0.8);
    box-shadow: 2px -8px 13px -10px rgba(0, 0, 0, 0.8);

    .resultados{
        span{
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
}
</style>