<script lang="ts" setup>
definePageMeta({
  layout: 'page',
})
const { t } = useLang()
useHead(() => ({
  title: t('pages.ophthalmic_information.ophthalmic_publicity'),
}))
// 眼疾影片
const eyeDisease = [
  {
    img: 'https://static.cmereye.com/imgs/2023/05/040da0e4cbb6878a.png',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease1_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease1_text',
    link: 'https://youtu.be/0pN3E5ewLjE',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/05/195b3f6dc0ff23b9.png',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease2_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease2_text',
    link: 'https://youtu.be/fM2cCC5zxWw',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/06/1664b018cca2148a.webp',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease3_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease3_text',
    link: 'https://youtu.be/qNF78pbRx6c',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/06/53b1b85f90011cda.webp',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease4_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease4_text',
    link: 'https://youtu.be/oYTtMkqVK4w',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/06/c6cd62a4b837e9b1.webp',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease5_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease5_text',
    link: 'https://youtu.be/L9DHmvCTAZk',
  },
  {
    img: 'https://static.cmereye.com/imgs/2023/06/56e33eb0198fc5dc.webp',
    title:
      'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease6_title',
    text: 'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_eyeDisease.eye_disease6_text',
    link: 'https://youtu.be/9CnKIu04Nkk',
  },
]
</script>

<template>
  <div>
    <div class="publicity">
      <div>
        <div>
          <div>
            <img data-cfsrc="https://static.cmereye.com/imgs/2023/06/d14944870b7cfec7.png" 
            srcset="https://static.cmereye.com/imgs/2023/07/c77bfeb27c892e8e.jpg 768w, https://static.cmereye.com/imgs/2023/06/d14944870b7cfec7.png"  
            alt="護眼宣傳" 
            src="https://static.cmereye.com/imgs/2023/06/d14944870b7cfec7.png"/>
          </div>
        </div>
        <div>
          <div>
            <div>
              {{
                $t(
                  'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text1'
                )
              }}
            </div>
            <div>promotional video</div>
            <div>
            </div>
          </div>
          <div>
            {{
              $t(
                'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text2'
              )
            }}
          </div>
          <div>
            <div>
              {{
                $t(
                  'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text3'
                )
              }}
            </div>
            <div>
              {{
                $t(
                  'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text4'
                )
              }}
            </div>
          </div>
          <svg
              width="9"
              height="144"
              viewBox="0 0 9 144"
              fill="none"
              xmlns="http://www.w3.org/2000/svg"
              data-v-1d8b93bf=""
              data-v-a125a221=""
              data-v-4b343dd3=""
              data-v-ee7ab105=""
              data-v-040e870e=""
            >
              <path
                d="M1 1V143L7.5 130.5"
                stroke="#2958A3"
                stroke-width="2"
                stroke-linecap="round"
                stroke-linejoin="round"
                data-v-1d8b93bf=""
                data-v-a125a221=""
                data-v-4b343dd3=""
                data-v-ee7ab105=""
                data-v-040e870e=""
              ></path>
            </svg>
        </div>
      </div>
      <div class="publicity-content-swiper">
        <div>
          <div>
            {{
              $t(
                'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text5'
              )
            }}
          </div>
          <div class="videoBorder">
            <PageVideoSwiper :eye-disease="eyeDisease" />
          </div>
        </div>
        <!-- <div>
          <div>
            {{
              $t(
                'pages.ophthalmic_information.ophthalmic_publicity_text.publicity_text6'
              )
            }}
          </div>
          <div class="videoBorder household">
            <PageVideoSwiper :eye-disease="eyeDisease" />
          </div>
        </div> -->
      </div>
      <div class="publicity-content-mb">
        <div v-for="(item, index) in eyeDisease" :key="index">
          <div>
            <img :src="item.img" :alt="item.title" srcset="" />
          </div>
          <div>
            <div>{{ $t(item.title) }}</div>
            <div>
              {{ $t(item.text) }}
            </div>
            <div>
              <a :href="item.link" target="_blank" rel="noopener noreferrer">{{
                $t(
                  'pages.ophthalmic_information.ophthalmic_little_theatre_text.little_theatre_a1'
                )
              }}</a>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div>
      <PageInformation />
    </div>
    <div class="footerMenuPom">
      <PageFooterMenu />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.footerMenuPom{
  margin-bottom: 50px;
}
.publicity {
  position: relative;
  &::before{
    content: '';
    background: #f1f1f1;
    position: absolute;
    top: -146px;
    left: 0;
    width: calc((100vw - 1493px)/2 + 1427px);
    height: 706px;
  }
  & > div:nth-child(1) {
    margin: 179px auto 0;
    display: flex;
    position: relative;
    flex-direction: column;
    height: 706px;
    width: 100%;
    max-width: 1493px;
    & > div:nth-child(1) {
      position: absolute;
      width: 100%;
      img{
        width: 100%;
      }
    }
    & > div:nth-child(2) {
      position: absolute;
      bottom: -50px;
      left: 50%;
      transform: translateX(-50%);
      display: flex;
      flex-direction: column;
      align-items: center;
      z-index: 5;
      & > div:nth-child(1) {
        font-family: 'Noto Sans HK';
        font-style: normal;
        font-weight: 400;
        font-size: 49.14px;
        line-height: 46px;
        text-align: center;
        letter-spacing: 0.2em;
        color: #ffffff;
        & > div:nth-child(2) {
          font-family: 'Metropolis';
          font-style: normal;
          font-weight: 500;
          font-size: 20px;
          line-height: 44px;
          letter-spacing: 0.1em;
          text-transform: uppercase;
          color: #8ad8dd;
        }
      }
      & > div:nth-child(2) {
        margin-top: 34px;
        font-family: 'Noto Sans HK';
        font-style: normal;
        font-weight: 700;
        font-size: 30px;
        line-height: 60px;
        text-align: right;
        letter-spacing: 0.3em;
        color: #ffffff;
      }
      & > div:nth-child(3) {
        font-family: 'Noto Sans HK';
        font-style: normal;
        font-weight: 400;
        font-size: 20px;
        line-height: 30px;
        text-align: center;
        letter-spacing: 0.3em;
        color: #ffffff;
      }
      &>svg{
        margin-top: 100px;
      }
    }
    & > div:nth-child(1) {
      & > img {
        position: relative;
        z-index: 5;
      }
    }
  }
  & > div:nth-child(2) {
    margin-top: 108px;
    margin-bottom: 277px;
    & > div {
      & > div:nth-child(1) {
        font-family: 'Noto Sans HK';
        font-style: normal;
        font-weight: 400;
        font-size: 35px;
        line-height: 35px;
        letter-spacing: 0.05em;
        color: #515151;
        width: 100%;
        max-width: 1190px;
        margin: 0 auto;
      }
    }
  }
  &-content-mb{
    display: none;
  }
}
.videoBorder {
  width: 1190px;
  border-top: 1.75771px solid #8ad8dd;
  padding-top: 73px;
  padding-bottom: 63px;
  margin: 25px auto 0;
}
:deep(.swiper-wrapper) {
  & > div:nth-child(n) {
    & > div:nth-child(1) {
      margin: 0 75px;
    }
  }
}
.household {
  border-bottom: 1.75771px solid #8ad8dd;
}
@media screen and (max-width: 768px) {
  .publicity {
    &::before{
      width: calc(100% - 50px);
      top: 0;
      left: 50px;
      height: 300px;
    }
    & > div:nth-child(1) {
      margin: 78px auto 0;
      height: 290px;
      & > div:nth-child(2) {
        bottom: -90px;
        & > div:nth-child(1) {
          font-size: 28px;
          line-height: 1.6;
          & > div:nth-child(2) {
            font-size: 12px;
            line-height: 1.2;
          }
        }
        & > div:nth-child(2) {
          font-size: 18px;
          line-height: 1.6;
          margin-top: 20px;
        }
        & > div:nth-child(3) {
          font-size: 14px;
          line-height: 1.6;
          letter-spacing: 0em;
        }
        &>svg{
          margin-top: -25px;
          transform: scale(.5);
        }
      }
    }
    &-content-swiper {
      display: none;
    }
    &-content-mb{
      width: calc(100% - 60px);
      max-width: 1080px;
      margin: 120px auto 0;
      min-height: 900px;
      display: block;
      & > div {
        display: flex;
        flex-direction: column-reverse;
        margin-bottom: 80px;
        & > div:nth-child(1) {
          margin-right: 72px;
          width: 100%;
          height: auto;
          background: #f2f2f2;
          display: flex;
          justify-content: center;
          align-items: center;
        }
        & > div:nth-child(2) {
          width: 100%;
          position: relative;
          margin-bottom: 90px;
          & > div:nth-child(1) {
            font-family: 'Noto Sans HK';
            font-style: normal;
            font-weight: 400;
            font-size: 20px;
            letter-spacing: 0.05em;
            padding-bottom: 5px;
            color: #515151;
            position: relative;
          }
          & > div:nth-child(1)::after {
            content: '';
            width: 65.04px;
            border-bottom: 1.75771px solid #8ad8dd;
            display: inline-block;
            position: absolute;
            left: 0;
            bottom: 0;
          }
          & > div:nth-child(2) {
            margin-top: 25px;
            font-family: 'Noto Sans HK';
            font-style: normal;
            font-weight: 350;
            font-size: 13.1828px;
            line-height: 26px;
            text-align: justify;
            letter-spacing: 0.1em;
            text-indent: 30px;
            text-transform: uppercase;
            color: #232323;
            & > div:nth-child(1) {
              margin-bottom: 20px;
            }
          }
          & > div:nth-child(3) {
            position: absolute;
            bottom: -60px;
            left: 50%;
            transform: translateX(-50%);
            width: 95px;
            height: 37.27px;
            background: #8ad8dd;
            font-family: 'Noto Sans HK';
            font-style: normal;
            font-weight: 500;
            font-size: 13.1538px;
            line-height: 26px;
            text-align: center;
            letter-spacing: 0.1em;
            color: #ffffff;
            display: flex;
            align-items: center;
            justify-content: center;
          }
        }
      }
    }
  }
}
</style>
