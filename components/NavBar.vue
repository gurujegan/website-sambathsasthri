<template>
  <div>
    <nav
      id="navbar"
      class="
        h-36
        bg-amber-900
        flex
        justify-between
        items-center
        py-4
        px-6
        shadow-2xl
        navbar-expand-lg
        sticky
      "
    >
      <NuxtLink to="/home" class="logo ml-32 navbar-brand -mt-64">
        <img src="~/assets/images/ss-white.png" alt="logo" class="w-80 h-72" />
        <!-- <h1 class="text-white text-3xl">

          <span class="fname capitalize">SambathSastri</span>
          <span class="fist">&#x1F44A;</span>
        </h1> -->
      </NuxtLink>
      <span class="navbar-text shadow-2xl opacity-80">&#9742; +91 - 94435 03868 </span>
      <div class="collapse navbar-collapse" id="navbarSupportedContent">
        <ul
          class="
            fixed
            top-0
            justify-between
            items-center
            right-56
            font-extrabold
            text-yellow-900
            navbar-nav
            mr-auto
            text-2xl
          "
        >
          <li
            class="
              nav-item
              ml-8
              rounded-lg
              hover:bg-white
              bg-yellow-300
              rounded-2xl
            "
          >
            <NuxtLink
              to="/home"
              class="block hover:text-blue-400 nav-link"
              id="nav-link"
              >Home</NuxtLink
            >
          </li>
          <li
            class="
              nav-item
              ml-8
              rounded-lg
              hover:bg-white
              bg-yellow-300
              rounded-2xl
            "
          >
            <NuxtLink
              to="/about"
              class="block hover:text-blue-400 nav-link"
              id="nav-link"
              >About</NuxtLink
            >
          </li>
          <li
            class="
              nav-item
              ml-8
              rounded-lg
              hover:bg-white
              bg-yellow-300
              rounded-2xl
            "
          >
            <NuxtLink
              to="/services"
              class="block hover:text-blue-400 nav-link"
              id="nav-link"
              >Services</NuxtLink
            >
          </li>
          <li
            class="
              nav-item
              ml-8
              rounded-lg
              hover:bg-white
              bg-yellow-300
              rounded-2xl
            "
          >
            <NuxtLink
              to="/services"
              class="block hover:text-blue-400 nav-link"
              id="nav-link"
              >Contact</NuxtLink
            >
          </li>
        </ul>
      </div>
    </nav>
  </div>
</template>

<style>
.sticky {
  position: fixed;
  top: 0;
  width: 100%;
  z-index: 1;
}

/* .logo{
  background: url('~/assets/images/ss-black.png');
  width: 50px;
  height: 50px;
} */
/* @media all and (max-width: 1100px) {
  #navbar .nav-item {
    display: none;
  }

  #navbar .logo {
    margin: auto;
    margin-top: -3.5rem;
  }
} */

/* Style the active link (or home/logo) */
.active {
  background-color: #04aa6d;
  color: white;
}

.nav-item {
  height: 4.5rem;
  margin-top: 28px;
  width: 12rem;
  text-align: center;
  font-size: large;
  margin-left: 5rem;
  font-variant: small-caps;
}

.nav-link {
  padding-top: 13px !important;
}

.navbar-text {
  position: absolute;
  left: 38rem;
  color: blanchedalmond;
  font-size: large;
  font-weight: 400;
  margin-top: 3rem;
}
</style>

<script>
export default {
  mounted () {
    window.onscroll = function () {
      myFunction()
    }
    // Get the navbar
    const navbar = document.getElementById('navbar')
    // Get the offset position of the navbar
    const sticky = navbar.offsetTop

    // Add the sticky class to the navbar when you reach its scroll position. Remove "sticky" when you leave the scroll position
    function myFunction () {
      if (window.pageYOffset >= sticky) {
        navbar.classList.add('sticky')
      } else {
        navbar.classList.remove('sticky')
      }
    }
  },
  methods: {
    myFunction1 () {
      const x = document.getElementById('myLinks')
      if (x.style.display === 'block') {
        x.style.display = 'none'
      } else {
        x.style.display = 'block'
      }
    }
  }
}
</script>
