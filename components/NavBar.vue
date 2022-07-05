<template>
  <div>
    <nav id="navbar" class="h-20 bg-yellow-900 flex justify-between items-center py-4 px-6 shadow-2xl">
     <NuxtLink to="/home" class="logo ml-32 -mt-3">
               <img src="~/assets/images/ss-white.png" alt="logo" class="w-48 h-40"/>
        <!-- <h1 class="text-white text-3xl">

          <span class="fname capitalize">SambathSastri</span>
          <span class="fist">&#x1F44A;</span>
        </h1> -->
      </NuxtLink>
      <ul class="fixed flex justify-between items-center right-44 font-bold text-yellow-900">
        <li class="nav-item h-10 ml-8 rounded-lg hover:bg-white  bg-yellow-300 text-center pt-2 w-32">
         <NuxtLink to="/home" class="block hover:text-blue-400" id="nav-link">Home</NuxtLink>
        </li>
        <li class="nav-item h-10 ml-8 rounded-lg hover:bg-white  bg-yellow-300 text-center pt-2 w-32">
          <NuxtLink to="/about" class="block hover:text-blue-400" id="nav-link">About</NuxtLink>
        </li>
        <li class="nav-item h-10 ml-8 rounded-lg hover:bg-yellow-400 bg-yellow-300 text-center pt-2 w-32">
          <NuxtLink to="/services" class="m-4" id="nav-link">Services</NuxtLink>
        </li>
        <li class="nav-item h-10 ml-8 rounded-lg hover:bg-yellow-400 bg-yellow-300 text-center pt-2 w-32">
          <a href="#sub" class="m-4" id="nav-link">Subscribe</a>
        </li>
      </ul>
      <div class="hamburger" id="hamburger">
        <span class="bar"></span>
        <span class="bar"></span>
        <span class="bar"></span>
      </div>
          <div class="block self-end absolute left-0 bottom-0 border-b-4 w-full"></div>
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
  }
}
</script>
