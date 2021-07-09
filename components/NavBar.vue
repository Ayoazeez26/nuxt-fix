<template>
  <!-- <header>
    <div>
      <nav>
        <ul class="bg-black">
          <li><NuxtLink to="/">Home</NuxtLink></li>
          <li><NuxtLink to="/">Blog</NuxtLink></li>
          <li><NuxtLink to="about">About</NuxtLink></li>
        </ul>
      </nav>
    </div>
  </header> -->
  <header
    id="header"
    class="
      ivisible
      sticky
      bg-pr-milk bg-opacity-90
      w-full
      flex
      items-center
      top-0
      left-0
      z-50
      h-20
      text-lg text-pr-nav
    "
  >
    <div class="flex items-center justify-between w-11/12 mx-auto">
      <div class="brand-logo w-12">
        <img src="~/assets/paritie-logo.png" alt="Paritie Logo">
      </div>
      <ul class="nav-tabs hidden md:flex items-center justify-between">
        <li class="active relative mr-8">
          <NuxtLink to="/">
            Home
          </NuxtLink>
        </li>
        <p class="big-num absolute -top-5 -right-5" />
        <li class="mr-8">
          <NuxtLink to="/services">
            Services
          </NuxtLink>
        </li>
        <li class="mr-8">
          <NuxtLink to="/projects">
            Projects
          </NuxtLink>
        </li>
        <li class="mr-8">
          <NuxtLink to="/innovation">
            Innovation
          </NuxtLink>
        </li>
        <li class="mr-8">
          <NuxtLink to="/coworking">
            Coworking Space
          </NuxtLink>
        </li>
        <li>
          <NuxtLink to="/blog">
            Blog
          </NuxtLink>
        </li>
      </ul>

      <div class="nav-links items-center justify-between flex">
        <a
          href="#"
          class="
            text-pr-sec
            border border-pr-sec
            hidden
            md:block
            rounded-lg
            bg-transparent
            outline-none
            text-sm
            py-3
            px-5
          "
        >Start a Project</a>
        <div
          class="
            hamburger
            sm-menu-btn
            relative
            z-50
            justify-self-end
            ml-20
            flex flex-col
          "
        >
          <span class="ham-up inline-flex w-5 h-1 bg-pr-pri" />
          <span class="ham-down inline-flex w-5 h-1 bg-pr-pri mt-1" />
        </div>
      </div>
      <div
        class="
          sm-screen-menu
          fixed
          top-0
          left-0
          h-screen
          w-screen
          lg:w-full
          bg-pr-pri
          hidden
        "
      >
        <div class="flex h-full relative w-10/12 mx-auto">
          <div
            class="
              hamburger
              absolute
              top-5
              right-0
              sm-menu-btn
              z-50
              justify-self-end
              ml-20
              flex flex-col
            "
          >
            <div class="relative">
              <span
                class="ham-up transform rotate-45 inline-flex w-8 h-px bg-white"
              />
              <span
                class="
                  ham-down
                  absolute
                  mt-1.5
                  top-3
                  left-0
                  transform
                  -rotate-45
                  inline-flex
                  w-8
                  h-px
                  bg-white
                "
              />
            </div>
          </div>
          <div class="hidden md:flex justify-between w-2/5">
            <div class="flex pt-10 flex-col">
              <div
                class="
                  text-lg
                  justify-between
                  flex flex-col
                  mx-auto
                  font-normal
                  py-20
                  text-white
                "
              >
                <div class="text-pr-milk text-base md:text-xl mb-5">
                  <h6 class="text-xs opacity-50 uppercase">
                    office
                  </h6>
                  <p>Suite C1, Peniel Albarka Plaza, Opp.</p>
                  <p>Federal Highcourt, Minna.</p>
                  <p>Niger State.</p>
                </div>
                <div class="font-medium text-base md:text-xl mb-5">
                  <h6 class="text-xs opacity-50 uppercase">
                    email us
                  </h6>
                  <p>info@paritie.com</p>
                </div>
                <div class="font-medium text-base md:text-xl mb-5">
                  <h6 class="text-xs opacity-50 uppercase">
                    call us
                  </h6>
                  <p>08234534534</p>
                </div>
                <div
                  class="socials text-base md:text-lg uppercase mt-8 md:w-auto"
                >
                  <h6 class="text-xs opacity-50 uppercase">
                    Follow Us
                  </h6>
                  <p class="mb-6 md:mt-2">
                    instagram
                  </p>
                  <p class="mb-6">
                    facebook
                  </p>
                  <p class="mb-6">
                    youtube
                  </p>
                  <p>twitter</p>
                </div>
              </div>
            </div>
            <div class="line h-full w-px" />
          </div>
          <div
            class="
              text-white
              pt-20
              flex
              justify-center
              md:justify-end
              font-semibold
              p-5
              mt-10
              w-3/5
            "
          >
            <div class="flex flex-col w-3/5">
              <a href="index.html" class="text-pr-sec text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-1">01.</span>Home</a>
              <a href="services.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">02.</span>Services</a>
              <a href="projects.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">03.</span>Projects</a>
              <a href="innovation.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">04.</span>Innovation</a>
              <a href="coworking.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">05.</span>Coworking</a>
              <a href="resources.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">06.</span>Resources</a>
              <a href="blog.html" class="text-3xl mb-3 p-2"><span class="text-xl mr-2 opacity-25">07.</span>Blog</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>
