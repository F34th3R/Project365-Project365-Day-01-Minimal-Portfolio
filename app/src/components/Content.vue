<template>
  <main>
    <div class="container">
      <header>
        <img src="../assets/svg/circular-plus.svg">
      </header>
      <div class="content">
        <div class="pie">
          <div class="pie-center">
            <div class="pie-center-content">
              <h4>
                TOTAL VALUE
              </h4>
              <h3>
                $92,023.35
              </h3>
            </div>
          </div>
        </div>
        <div class="content-fotter">
          <PriceCard
            title="BITCOIN CASH"
            ammount="57,483.35"
            :progress="(129*0.8).toString()"
            actualPrice="+ 3220.21"
          />
          <PriceCard
            title="EHTEREUM"
            ammount="34540.00"
            :arrow="false"
            :progress="(129*0.2).toString()"
            background="#465566"
            actualPrice="- 3220.21"
          />
        </div>
      </div>
    </div>
  </main>
</template>

<script>
import PriceCard from './PriceCard'
export default {
  name: 'Content',
  components: {
    PriceCard
  }
}
</script>

<style lang="scss">
main {
  background: #FBFBFB;
  padding: 40px;
  width: 100%;
  height: 100vh;
  .container {
    margin: auto;
    height: 100%;
    position: relative;
    header {
      height: 40px;
      position: relative;
      img {
        cursor: pointer;
        position: absolute;
        top: 0;
        right: 0;
        height: 44px;
      }
    }
    .content {
      .pie {
        position: relative;
        margin: 50px auto;
        width: 425px;
        height: 425px;
        border-radius: 50%;
        background: #465566;
        background-image: linear-gradient(to right, transparent 50%, #1B9BB0 0);
        &::before {
          content: '';
          display: block;
          margin-left: 50%;
          height: 100%;
          border-radius: 0 100% 100% 0 / 50%;
          background: #1B9BB0;
          transform-origin: left;
          transform: rotate(-140deg); // 144deg .4turn
        }
        &-center {
          position: absolute;
          top: 60px;
          left: 60px;
          width: 305px;
          height: 305px;
          margin: 0 auto;
          border-radius: 50%;
          background: #FBFBFB;
          border: #E5E8E8 solid 20px;
          &-content {
            text-align: center;
            top: 40%;
            position: relative;
            h4 {
              color: #707070;
              font-size: 14;
              font-weight: 500;
              line-height: 19px;
              letter-spacing: 0.2px;
              margin-bottom: 5px;
            }
            h3 {
              color: #1B9BB0;
              font-size: 24px;
              line-height: 32px;
            }
          }
        }
      }
      &-fotter {
        margin-top: 89px;
        display: flex;
        justify-content: space-between;
        margin: auto;
        width: 35%;
        &-card {
          span {
            color: #1B9BB0;
            font-family: Raleway;
            font-size: 14px;
            line-height: 16px;
            letter-spacing: 1.9px;
          }
          h3 {
            color: #4A4A4A;
            font-size: 29px;
            line-height: 38px;
            letter-spacing: 0.74px;
          }
          .price {
            display: inline-flex;
            align-items: center;
            margin-top: 5px;
            .arrow {
              width: 16px;
              margin-right: 7px;
            }
            span {
              font-family: 'Segoe UI';
              color: #9B9B9B;
              font-size: 18px;
              line-height: 27px;
              letter-spacing: 1.5px;
            }
            &-progress {
              margin-top: 20px;
              width: 149.5px;
              height: 3px;
              background-color: #E4F1F3;
            }
            &-progress-actual {
              margin-top: 7px;
              height: 3px;
            }
          }
        }
      }
    }
  }
}
</style>
