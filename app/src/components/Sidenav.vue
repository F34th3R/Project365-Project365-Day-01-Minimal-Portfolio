<template>
  <nav>
      <div class="brand">
        <img class="brand-logo" src="@/assets/svg/brand-logo.svg">
        <div class="brand-name">
          <h3>Exodus</h3>
          <span>v1.41.0</span>
        </div>
      </div>
      <div class="menu">
        <MenuItem
          :active="true"
          title="Portfolio">
          <img slot="ico" src="@/assets/svg/portfolio.svg">
        </MenuItem>
        <MenuItem
          :active="false"
          title="Wallet">
          <img slot="ico" src="@/assets/svg/wallet.svg">
        </MenuItem>
        <MenuItem
          :active="false"
          title="Exchange">
          <img slot="ico" src="@/assets/svg/exchange.svg">
        </MenuItem>
        <MenuItem
          :active="false"
          title="Backup">
          <img slot="ico" src="@/assets/svg/backup.svg">
        </MenuItem>
        <MenuItem
          :active="false"
          title="Support">
          <img slot="ico" src="@/assets/svg/support.svg">
        </MenuItem>
        <MenuItem
          :active="false"
          title="Settings">
          <img slot="ico" src="@/assets/svg/settings.svg">
        </MenuItem>
        <div class="menu-item-fotter">
          <div class="content-fotter">
            <span>
              YOUR HOLDINGS:
            </span>
            <p>
              $92,023.35
            </p>
          </div>
          <img src="../assets/svg/refresh.svg">
        </div>
      </div>
    </nav>
</template>

<script>
import MenuItem from '@/components/MenuItem'
export default {
  name: 'Sidenav',
  components: {
    MenuItem
  }
}
</script>

<style lang="scss">
$primary-color: #1B9BB0;
$general-padding-l: 50px;
nav {
  height: 100vh;
  display: block;
  background: white !important;
  .brand {
    width: 100%;
    height: 140px;
    padding-left: $general-padding-l;
    align-items: center;
    display: flex;
    &-logo {
      cursor: pointer;
      width: 81px;
    }
    &-name {
      padding-left: 16px;
      h3 {
        font-weight: 400;
        font-size: 26px;
        line-height: 35px;
        letter-spacing: -0.15px;
      }
      span {
        color: #A6A6A6;
        font-weight: 300;
        font-size: 14px;
        line-height: 17px;
        letter-spacing: -0.15px;
      }
    }
  }
  .menu {
    &-item {
      position: relative;
      width: 100%;
      height: 78px;
      display: flex;
      align-items: center;
      cursor: pointer;
      img {
        height: 100%;
        padding-left: $general-padding-l;
      }
      h4 {
        font-weight: 400;
        padding-left: 30px;
      }
      &-ico-container {
        width: 80px;
        height: 20px;
      }
      &-active {
        width: 10px;
        height: 100%;
        position: absolute;
        right: 0;
        bottom: 0;
        background: $primary-color;
      }
      &-fotter {
        bottom: 0;
        left: 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 130px 57px 30px $general-padding-l;
        cursor: pointer;
        img {
          height: 44px;
        }
        .content-fotter {
          span {
            font-size: 14px;
            font-weight: 400;
            line-height: 17px;
            letter-spacing: 2px;
            color: $primary-color;
          }
          p {
            font-size: 20px;
            font-weight: 700;
            line-height: 26px;
            letter-spacing: 3px;
          }
        }
      }
    }
    .active {
      background: #FBFBFB;
      color: $primary-color;
      h4 {
        font-weight: 500 !important;
      }
    }
  }
}
</style>
