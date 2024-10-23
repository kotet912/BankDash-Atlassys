<template>
  <div class="menu">
    <div class="menu__container">
      <div class="menu__box-img">
        <img src="../public/assets/images/Logo.png" alt="" />
      </div>
      <div class="menu__box-nav">
        <nav class="menu__nav">
          <ul class="menu__ul">
            <li class="menu__li" v-for="item in menuItems" :key="item.id">
              <div v-if="item.title === 'Setting'" class="active-line"></div>
              <component
                :is="item.icon"
                class="menu-icon"
                :class="{ active: item.title === 'Setting' }"
              />
              <router-link
                :to="item.link"
                :class="{ active: item.title === 'Setting' }"
              >
                {{ item.title }}
              </router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script setup>
import DashboardIcon from '../public/assets/icons/dashboard.svg';
import TransactionsIcon from '../public/assets/icons/transactions.svg';
import AccountsIcon from '../public/assets/icons/accounts.svg';
import InvestmentsIcon from '../public/assets/icons/investments.svg';
import CreditCardsIcon from '../public/assets/icons/credit-cards.svg';
import LoansIcon from '../public/assets/icons/loans.svg';
import ServicesIcon from '../public/assets/icons/services.svg';
import MyPrivilegesIcon from '../public/assets/icons/my-privileges.svg';
import SettingIcon from '../public/assets/icons/setting.svg';

const menuItems = [
  {
    id: 1,
    title: 'Dashboard',
    link: '/',
    icon: DashboardIcon
  },
  {
    id: 2,
    title: 'Transactions',
    link: '/transactions',
    icon: TransactionsIcon
  },
  {
    id: 3,
    title: 'Accounts',
    link: '/',
    icon: AccountsIcon
  },
  {
    id: 4,
    title: 'Investments',
    link: '/',
    icon: InvestmentsIcon
  },
  {
    id: 5,
    title: 'Credit Cards',
    link: '/',
    icon: CreditCardsIcon
  },
  { id: 6, title: 'Loans', link: '/', icon: LoansIcon },
  { id: 7, title: 'Services', link: '/', icon: ServicesIcon },
  {
    id: 8,
    title: 'My Privileges',
    link: '/',
    icon: MyPrivilegesIcon
  },
  { id: 9, title: 'Setting', link: '/', icon: SettingIcon }
];
</script>

<style lang="scss" scoped>
.menu {
}
.menu__container {
  padding-top: 33px;
}
.menu__box-img {
  padding-left: 44px;
}
.menu__box-nav {
  padding-top: 58px;
}
.menu__nav {
}
.menu__ul {
  margin: 0;
  padding: 0;
  gap: 39px;
  display: flex;
  flex-direction: column;
}
.menu__li {
  padding: 0;
  margin: 0;
  display: flex;
  align-items: center;
  gap: 26px;
  position: relative;
  padding-left: 44px;

  a {
    text-decoration: none;
    color: rgb(177, 177, 177);
    font-family: Inter;
    font-size: 18px;
    font-weight: 500;
    line-height: 22px;
    letter-spacing: 0%;
    text-align: left;
  }
  .active {
    color: rgb(24, 20, 243);
    padding-left: 4px;
  }
}
.menu-icon {
  &.active {
    margin-left: -7px;
    path {
      fill: rgb(24, 20, 243);
    }
  }
}
.active-line {
  position: absolute;
  width: 6px;
  height: 60px;
  border-radius: 0px 10px 10px 0px;
  background: rgb(24, 20, 243);
  top: 50%;
  transform: translateY(-50%);
  left: 0;
  z-index: 1;
}
</style>
