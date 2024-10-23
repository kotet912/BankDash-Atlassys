<template>
  <div class="menu">
    <div class="menu__container">
      <div class="menu__box-img">
        <img src="../public/assets/images/Logo.png" alt="" />
      </div>
      <div class="menu__box-nav">
        <nav>
          <ul>
            <li v-for="item in menuItems" :key="item.id">
              <img :src="item.icon" alt="" class="menu-icon" />
              <router-link :to="item.link">{{ item.title }}</router-link>
            </li>
          </ul>
        </nav>
      </div>
    </div>
  </div>
</template>

<script setup>
const menuItems = [
  { id: 1, title: 'Dashboard', link: '/', icon: '/assets/icons/dashboard.svg' },
  {
    id: 2,
    title: 'Transactions',
    link: '/transactions',
    icon: '/assets/icons/transactions.svg'
  },
  { id: 3, title: 'Accounts', link: '/', icon: '/assets/icons/accounts.svg' },
  {
    id: 4,
    title: 'Investments',
    link: '/',
    icon: '/assets/icons/investments.svg'
  },
  {
    id: 5,
    title: 'Credit Cards',
    link: '/',
    icon: '/assets/icons/credit-cards.svg'
  },
  { id: 6, title: 'Loans', link: '/', icon: '/assets/icons/loans.svg' },
  { id: 7, title: 'Services', link: '/', icon: '/assets/icons/services.svg' },
  {
    id: 8,
    title: 'My Privileges',
    link: '/',
    icon: '/assets/icons/my-privileges.svg'
  },
  { id: 9, title: 'Setting', link: '/', icon: '/assets/icons/setting.svg' }
];
</script>

<style lang="scss" scoped>
.menu-icon {
  width: 24px;
  height: 24px;
  margin-right: 8px;
}
</style>
