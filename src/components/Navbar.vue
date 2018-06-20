<template>
  <div>
    <b-navbar variant="dark" type="dark" class="ao_navbar">
        <b-navbar-brand tag="h1" class="ao_brand p-0">Shoptime</b-navbar-brand>
        <ul class="d-flex m-0 p-0 ao_tabs h-100" left>
            <router-link :to="{ name: tab.href }"
                class="d-flex" v-for="(tab, index) in tabs"
                v-bind:key="index">
                <li class="d-flex align-items-center justify-content-center"
                    :class="{active: activeTab === index}"
                    @click="activeTab = index">
                    <span>{{ tab.name }}</span>
                </li>
            </router-link>
        </ul>
        <b-nav-text class="ml-auto ao_user">ADMIN</b-nav-text>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: 'Navbar',
  data() {
    return {
      activeTab: 0,
      tabs: [
        {
          name: 'HOME',
          href: 'Overview',
        },
        {
          name: 'ORDERS',
          href: 'HelloWorld',
        },
        {
          name: 'PRODUCT',
          href: 'Overview',
        },
      ],
    };
  },
};
</script>
