<script lang="ts" setup>
// compiler macro
definePageMeta({
  layout: 'page',
})
const { t } = useLang()
useHead({
  title: `${t('pages.process_cost.cost')}| ${t('pages.process_cost.process')}`,
})
// 流程及費用
const serviceNavigation = [
  {
    anchorName: 'pages.process_cost.cost',
    anchorLink: '/process-and-cost#cost',
  },
  {
    anchorName: 'pages.process_cost.process',
    anchorLink: '/process-and-cost#processed',
  },
]
const isShowLanguageBool = ref(false)
const processBox = ref({
  offsetTop: 0,
})
onMounted(() => {
  scrollHeight()
  window.addEventListener('scroll', scrollHeight)
})
const scrollHeight = () => {
  if (window.scrollY >= processBox.value.offsetTop - 300) {
    isShowLanguageBool.value = true
  } else {
    isShowLanguageBool.value = false
  }
}
</script>

<template>
<div class="processAndCostPage">
  <div
    :class="['processAndCost']"
    :style="{
      'background-position': isShowLanguageBool === true ? '100% 100%' : '100% 0',
      'background-size': isShowLanguageBool === true ? 'auto 100%' : '100% auto'
    }"
  >
    <div>
      <div id="cost">
        <div class="content">
          <div class="titleBox">
            <h1 class="text-3xl font-normal">
              {{ $t('pages.process_cost.cont.cost_h1') }}
            </h1>
            <h2>PRICE LIST</h2>
            <h3>{{ $t('pages.process_cost.cont.cost_h3_1') }}</h3>
            <p>{{ $t('pages.process_cost.cont.cost_p1') }}</p>
          </div>

          <div class="costsTable py-10 px-8 mt-12 mb-40">
            <h3 class="text-2xl text-center font-bold mb-8">
              {{ $t('pages.process_cost.cont.cost_h3_2') }}
            </h3>
            <table class="table">
              <thead>
                <tr class="firstRow">
                  <td colspan="2"></td>
                  <td class="text-center text-xl">
                    {{ $t('pages.process_cost.cont.cost_tr1_td1') }}
                  </td>
                  <td class="text-center text-xl">
                    {{ $t('pages.process_cost.cont.cost_tr1_td2') }}
                  </td>
                </tr>
              </thead>
              <tbody>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr2_td1') }}
                  </td>
                  <td class="text-center">$450</td>
                  <td class="text-center">$750</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr3_td1') }}
                  </td>
                  <td class="text-center">$1000</td>
                  <td class="text-center">$1,800</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr4_td1') }}
                  </td>
                  <td class="text-center">$1000</td>
                  <td class="text-center">$1,800</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr5_td1') }}
                  </td>
                  <td class="text-center">$1,500</td>
                  <td class="text-center">$2,600</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr6_td1') }}
                  </td>
                  <td class="text-center">$400</td>
                  <td class="text-center">$800</td>
                </tr>
                <tr>
                  <td colspan="2">
                    光學生物測量儀
                  </td>
                  <td class="text-center">$400</td>
                  <td class="text-center">$650</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr7_td1') }}
                  </td>
                  <td class="text-center">$400</td>
                  <td class="text-center">$600</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr8_td1') }}
                  </td>
                  <td class="text-center">$620</td>
                  <td class="text-center">$960</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr9_td1') }}
                  </td>
                  <td class="text-center">$300</td>
                  <td class="text-center">$500</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr10_td1') }}
                  </td>
                  <td class="text-center">$400</td>
                  <td class="text-center">$800</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr11_td1') }}
                  </td>
                  <td class="text-center">$300</td>
                  <td class="text-center">$600</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr12_td1') }}
                  </td>
                  <td class="text-center">/</td>
                  <td class="text-center">$3,900</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr13_td1') }}
                  </td>
                  <td class="text-center">/</td>
                  <td class="text-center">$3,900</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr14_td1') }}
                  </td>
                  <td class="text-center">/</td>
                  <td class="text-center">$5,500</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr15_td1') }}
                  </td>
                  <td class="text-center">$500</td>
                  <td class="text-center">$1,000</td>
                </tr>
                <tr>
                  <td colspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr16_td1') }}
                  </td>
                  <td class="text-center">/</td>
                  <td class="text-center">$600/$800</td>
                </tr>
                <!-- <tr>
                  <td rowspan="2">
                    {{ $t('pages.process_cost.cont.cost_tr17_td1') }}
                  </td>
                  <td class="text-center text-left">
                    {{ $t('pages.process_cost.cont.cost_tr17_td2') }}
                  </td>
                  <td class="text-center">/</td>
                  <td class="text-center">$350</td>
                </tr>
                <tr>
                  <td class="text-center border-0 text-left">
                    {{ $t('pages.process_cost.cont.cost_tr18_td2') }}
                  </td>
                  <td class="text-center border-0">/</td>
                  <td class="text-center border-0">$750</td>
                </tr> -->
              </tbody>
            </table>
            <p class="text-center mt-20 mb-16 leading-10">
              {{ $t('pages.process_cost.cont.cost_p2')
              }}<span class="font-bold">{{
                $t('pages.process_cost.cont.cost_p2_1')
              }}</span
              >{{ $t('pages.process_cost.cont.cost_p2_2') }}<br />
              {{ $t('pages.process_cost.cont.cost_p3')
              }}<span class="font-bold">{{
                $t('pages.process_cost.cont.cost_p3_1')
              }}</span>
              {{ $t('pages.process_cost.cont.cost_p4') }} <br />
              {{ $t('pages.process_cost.cont.cost_p5') }}<br />
              {{ $t('pages.process_cost.cont.cost_p6')
              }}<span class="font-bold">HK$1,500-HK$6,000</span
              >{{ $t('pages.process_cost.cont.cost_p6_1') }}
              {{ $t('pages.process_cost.cont.cost_p7') }}<br />
              {{ $t('pages.process_cost.cont.cost_p8') }} <br />
              {{ $t('pages.process_cost.cont.cost_p9') }}
            </p>
          </div>
        </div>
      </div>
      <div id="processed" ref="processBox">
        <div
          class="processMain mainCon relative flex items-start justify-center"
        >
          <div class="content relative">
            <div class="titleBox">
              <h1 class="text-3xl font-normal">
                {{ $t('pages.process_cost.process_1.process_h1') }}
              </h1>
              <h2>Outpatient Services</h2>
            </div>
            <div class="py-10 px-8 mt-12 mb-40">
              <div class="processItem mb-20">
                <p>{{ $t('pages.process_cost.process_1.process_p1') }}</p>
              </div>
              <div class="processItem itemdes mb-14">
                <p>{{ $t('pages.process_cost.process_1.process_p2') }}</p>
                <div>
                  <h3 class="text-xl pb-3 mb-3">
                    {{ $t('pages.process_cost.process_1.process_h3_1') }}
                  </h3>
                  <p>
                    {{ $t('pages.process_cost.process_1.process_p3_1') }}<br />
                    {{ $t('pages.process_cost.process_1.process_p3_2') }}
                  </p>
                </div>
              </div>
              <div class="processItem itemdes mb-14">
                <p>{{ $t('pages.process_cost.process_1.process_p4') }}</p>
                <div>
                  <h3 class="text-xl pb-3 mb-3">
                    {{ $t('pages.process_cost.process_1.process_h3_2') }}
                  </h3>
                  <p>
                    {{ $t('pages.process_cost.process_1.process_p5_1') }}<br />
                    {{ $t('pages.process_cost.process_1.process_p5_2') }}<br />
                    {{ $t('pages.process_cost.process_1.process_p5_3') }}
                  </p>
                </div>
              </div>
              <div class="processItem mb-20">
                <p>{{ $t('pages.process_cost.process_1.process_p6') }}</p>
              </div>
              <div class="processItem processItem5 mb-20">
                <p>
                  {{ $t('pages.process_cost.process_1.process_p7_1') }} <br />
                  {{ $t('pages.process_cost.process_1.process_p7_2') }}
                </p>
              </div>
              <div class="processItem processItem6 itemdes mb-20">
                <p>{{ $t('pages.process_cost.process_1.process_p8') }}</p>
                <div>
                  <p>{{ $t('pages.process_cost.process_1.process_p9') }}</p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <PageInformation :service-navigation="serviceNavigation" />
    
  </div>
  <PageFooterMenu />
</div>
</template>
<style lang="scss" scoped>
.processAndCostPage{
  margin-bottom: 50px;
}
.processAndCost {
  transition: all 0.5s;
  background-repeat: no-repeat !important;
  background: url('https://static.cmereye.com/imgs/2023/06/414012d88e3154c7.jpg')no-repeat;
}

.processAndCost > div:nth-child(1) {
  max-width: 1080px;
  margin: auto;
}

.titleBox {
  padding-top: 100px;
  font-family: 'Noto Sans HK';

  h1 {
    font-size: 37.5px;
  }

  h2 {
    color: #8ad8dd;
    font-size: 21px;
    font-family: 'Metropolis';
    text-transform: uppercase;
    font-weight: 500;
    margin-bottom: 40px;
    letter-spacing: 5px;
  }

  h3 {
    font-size: 30px;
  }

  p {
    font-size: 20px;
  }
}

.costsTable {
  background-color: rgba(255, 255, 255, 0.75);

  table {
    width: 100%;
    thead {
      td {
        padding-bottom: 35px;
        position: relative;

        &::before {
          content: '';
          position: absolute;
          width: 100%;
          border-bottom: 1px dashed;
          bottom: 25%;
          left: 0;
        }
      }
    }

    tbody {
      tr {
        border-bottom: #dddddd solid 1.5px;
        width: 887.83px;

        &:nth-child(odd) {
          background-color: rgba(242, 242, 242, 0.75);
        }

        &:nth-child(even) {
          background-color: rgba(255, 255, 255, 0.55);
        }

        &:last-child {
          border: none;
        }

        td {
          padding: 15px;
          padding-left: 25px;
        }

        td:nth-child(1) {
          width: 620px;
          text-align: left;
        }
      }

      & > tr:nth-child(17) {
        & > td:nth-child(2) {
          text-align: left;
        }
      }

      position: relative;

      &::before {
        content: '';
        position: absolute;
        width: 100%;
        border-bottom: 1px dashed;
        bottom: -2%;
        left: 0;
      }
    }
  }
}

.anchor {
  bottom: 450px;
  position: fixed;
  right: 2.5%;
  z-index: 99;

  a {
    border: 0.5px solid #515151;
    margin: 5px 0;
    padding: 10px 40px 5px;
    font-size: 15px;
    background-color: #fff;
    text-align: center;
  }

  .anchorActive,
  .exactActive {
    border: 0.5px solid #8ad8dd;
    background: #8ad8dd;
    color: #fff;
    position: relative;

    &::after {
      content: '';
      position: absolute;
      width: 12%;
      height: 100%;
      right: 0;
      top: 0;
      background-color: #ffffff;
    }
  }
}

.processMain {
  .titleBox {
    h2 {
      color: #8ad8dd;
      font-size: 21px;
      font-family: 'Metropolis';
      text-transform: uppercase;
      font-weight: 500;
      margin-bottom: 40px;
      letter-spacing: 5px;
    }
  }

  .anchor {
    bottom: 20%;
    position: fixed;
    right: 2.5%;
    z-index: 99;
    bottom: 20%;

    a {
      border: 0.5px solid #515151;
      margin: 5px 0;
      padding: 10px 40px 5px;
      font-size: 15px;
      background-color: #fff;
      text-align: center;
    }

    .anchorActive,
    .exactActive {
      border: 0.5px solid #8ad8dd;
      background: #8ad8dd;
      color: #fff;
      position: relative;

      &::after {
        content: '';
        position: absolute;
        width: 12%;
        height: 100%;
        right: 0;
        top: 0;
        background-color: #ffffff;
      }
    }
  }

  .processItem {
    display: flex;
    align-items: flex-start;
    text-align: center;
    position: relative;

    &::before {
      content: '';
      color: #1b407a;
      position: absolute;
      top: 60px;
      font-size: 56px;
      left: 90px;
      background: url('https://static.cmereye.com/imgs/2023/06/66b6869226b542b5.png');
      background-size: 100% 100%;
      width: 25px;
      height: 55px;
    }

    & > p,
    & > div {
      padding: 10px 20px;
      background: #5376d0;
      display: inline-block;
      color: #fff;
    }

    & > p {
      margin-right: 100px;
      width: 200px;
    }

    & > div {
      width: 500px;
    }

    h3 {
      border-bottom: 1px solid #fff;
    }
  }

  .itemdes > p:after {
    position: absolute;
    content: '';
    left: 225px;
    top: 21px;
    margin: auto 0;
    width: 50px;
    height: 1px;
    border-bottom: 2px #5376d0 dotted;
  }

  .processItem5::before {
    top: 75px;
  }

  .processItem6::before {
    display: none;
  }
}
@media screen and (max-width: 768px) {
  .titleBox {
    width: max-content;
    color: #515151;
     h1 {
      font-size: 24px;
      padding-left: 30px;
      
    }

    h2 {
      padding-left: 30px;
      font-size: 18px;
      letter-spacing: -.05em;
    }

    h3 {
      font-size: 20px;
      padding-left: 30px;
    }

    p {
      font-size: 16px;
      padding-left: 30px;
    }
  }
  .costsTable {
    width: calc(100% - 60px);
    margin: 50px auto;
    padding: 30px 20px 1px;
    &>h3{
      font-size: 24px;
      margin-bottom: 15px;
    }
    table {
      thead {
        td {
          font-size: 16px;
          padding-bottom: 15px;
          &::before{
            border-bottom: 1px solid;
          }
        }
      }
      tbody {
        tr {
          td {
            font-size: 16px;
            padding: 10px 0 5px;
          }
          td:nth-child(1) {
            width: 140px;
            padding: 10px 10px 5px;
          }
        }
      }
    }
    &>p{
      font-size: 16px;
      line-height: 30px;
    }
  }
  .processMain{
    .titleBox {
      padding-top: 50px;
      h2 {
        font-size: 18px;
        letter-spacing: -.05em;
      }
    }
    .processItem {
      margin-bottom: 70px;
      &::before {
        top: 50px;
        left: 45px;
        width: 10px;
        height: 30px;
      }
      &:nth-of-type(5):before{
        top: 75px;
      }
      & > p,& > div {
        padding: 7px 0px 2px;
        br{
          display: none;
        }
      }
      &:not(:last-child){
        &>div{
          padding: 7px 10px 2px;
          p{
            text-align: left;
          }
        }
      }
      & > p {
        margin-right: 50px;
        width: 100px;
      }

      & > div {
        flex: 1;
      }
      h3{
        padding-top: 10px;
        padding-bottom: 0;
      }
    }
    &>div{
      width: 100%;
      &>div:last-child{
        margin-top: 0;
      }
    }
    .itemdes > p:after {
      left: 110px;
      top: 16px;
      margin: auto 0;
      width: 30px;
      height: 1px;
      border-bottom: 2px #5376d0 dotted;
    }
  }
  .processAndCost{
    background: url('https://static.cmereye.com/imgs/2023/07/c20c5728572d0992.jpg');
    background-position: top left !important;
    background-size: 100% auto !important;
  }
  #processed{
    background: url('https://static.cmereye.com/imgs/2023/07/2534e621e7024180.jpg')no-repeat;
  }
}

</style>
<style lang="scss" scoped>
@media screen and (min-width: 1920px) {
  .content {
    // padding-left: 160px;
  }
}
</style>
