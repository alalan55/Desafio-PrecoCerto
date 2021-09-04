<template>
  <div>
    <div class="lista">
      <div class="conteudo-lista">
        <div class="table">
          <div class="head-table">
            <div class="h-codigo">
              <input type="checkbox" name="" id="" />
              <div class="content-h-codigo">
                <span>Cód</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>

            <div class="h-produto">
              <div class="content-h-produto">
                <span>Produto</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>

            <div class="h-custo">
              <div class="content-h-custo">
                <span>Custo</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>

            <div class="h-frete">
              <div class="content-h-frete">
                <span>Frete</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>

            <div class="h-margem">
              <div class="content-h-margem">
                <span>Margem</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>

            <div class="h-precoFinal">
              <div class="content-h-precoFinal">
                <span>Preço final</span>
                <img src="../../assets/img/selector.svg" alt="" />
              </div>
            </div>
          </div>

          <div class="body-table">
            <div class="cell-table" v-for="produto in produtos" :key="produto.id">
              <div class="b-codigo">
                <input type="checkbox" name="" id="" />
                <div class="content-b-codigo">
                  <span>{{produto.codigo}}</span>
                </div>
              </div>

              <div class="b-produto">
                <span>{{produto.produto}}</span>
              </div>

              <div class="b-custo">
                <span>{{produto.custo.toLocaleString("pt-BR", { minimumFractionDigits: 2 , style: 'currency', currency: 'BRL' })}}</span>
              </div>

              <div class="b-frete">
                <div class="content-b-frete">
                  <span v-for="(frete, index) in produto.frete" :key="index">{{frete.toLocaleString("pt-BR", { minimumFractionDigits: 2 , style: 'currency', currency: 'BRL' })}}</span>
                </div>
              </div>
              <div class="b-margem">
                <div class="content-b-margem">
                  <div class="valor-margem" v-for="(vmargem, index) in produto.margem" :key="index">
                   <span>{{vmargem.valor.toLocaleString("pt-BR", { minimumFractionDigits: 2 , style: 'currency', currency: 'BRL' })}}</span>
                   <span>{{vmargem.porcento}}%</span>
                  </div>
                  <!-- <div class="valor-margem">
                    <span>R$ 199,00</span>
                    <span>50%</span>
                  </div> -->
                </div>
              </div>
              <div class="b-precoFinal">
                <div class="content-b-precoFinal">
                  <span>{{produto.precoFinal.toLocaleString("pt-BR", { minimumFractionDigits: 2 , style: 'currency', currency: 'BRL' })}}</span>
                  <button class="btn-enviar">Enviar preço</button>
                </div>
              </div>
            </div>

           
          </div>

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
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props:['produtos']
};
</script>

<style lang="scss" scoped>
$grey1: #f2f2f2;
$grey2: #9d9d9d;
$grey3: #4a555d;
$grey4: #9faab2;
$grey5: #dddddd;
$greybtn: #f1f1f1;

.lista {
  height: 75vh;
  border: 1px solid transparent;
  max-width: 1450px;
  margin: 0 auto;
  position: relative;
  .conteudo-lista {
    margin-top: 50px;

    .table {
      .btn-enviar {
        background: none;
        padding: 0.3rem;
        border-radius: 5px;
        border: 3px solid $greybtn;
        font-family: "Poppins";
        font-size: 13px;

        &:hover {
          background: $greybtn;
        }
      }
      .head-table {
        width: 100%;
        padding: 0.2rem 0;
        display: grid;
        grid-template-columns: 145px 400px 150px 200px 250px 200px;

        font-weight: 200;
        background: $grey4;
        color: white;

        :nth-child(1) {
          padding: 0 0.6rem;
        }

        & > div {
          height: 5vh;
        }

        .h-codigo {
          display: flex;
          align-items: center;

          .content-h-codigo {
            display: flex;
            align-items: center;
          }
        }
        .h-produto {
          display: flex;
          align-items: center;

          .content-h-produto {
            display: flex;
            align-items: center;
          }
        }
        .h-custo {
          display: flex;
          align-items: center;

          .content-h-custo {
            display: flex;
            align-items: center;
          }
        }
        .h-frete {
          display: flex;
          align-items: center;

          .content-h-frete {
            display: flex;
            align-items: center;
          }
        }
        .h-margem {
          display: flex;
          align-items: center;

          .content-h-margem {
            display: flex;
            align-items: center;
          }
        }
        .h-precoFinal {
          display: flex;
          align-items: center;

          .content-h-precoFinal {
            display: flex;
            align-items: center;
          }
        }
      }

      .body-table {
        overflow-y: auto;
        height: 52vh;

        &::-webkit-scrollbar {
          width: 0;
        }

        .cell-table {
          width: 100%;
          display: grid;
          grid-template-columns: 150px 400px 150px 200px 250px 250px;
          gap: 0.1rem;
          border-bottom: 1px solid $grey5;

          & > div {
            padding: 0.6rem;
            text-align: left;
          }

          .b-codigo {
            display: flex;
            align-items: center;
            overflow-x: auto;

            .content-b-codigo {
              overflow-x: auto;
              margin: 0 1rem;
              display: flex;
              align-items: center;
            }
          }
          .b-produto {
            display: flex;
            align-items: center;
            overflow-x: auto;
          }
          .b-custo {
            display: flex;
            align-items: center;
          }
          .b-frete {
            .content-b-frete {
              display: flex;
              flex-direction: column;
            }
          }
          .b-margem {
            .content-b-margem {
              .valor-margem {
                display: flex;
                max-width: 60%;
                justify-content: space-between;
              }
            }
          }
          .b-precoFinal {
            display: flex;
            align-items: center;
            .content-b-precoFinal {
              width: 100%;
              display: flex;
              justify-content: space-between;
              align-items: center;
            }
          }
        }
      }

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
    }
  }
}
</style>