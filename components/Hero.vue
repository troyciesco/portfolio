<template>
  <section
    class="grid items-center gap-8 max-w-7xl mx-auto grid-cols-1 px-6 mb-20 md:mb-0 xl:px-0 md:grid-cols-2 md:h-[88vh]">
    <div class="md:pr-4">
      <h1 class="mb-8 leading-tight text-4xl text-left md:text-[4rem] font-bold">
        Hello! <br /><span class="bg-primary-200">I'm Troy Ciesco.</span>
      </h1>
      <p class="max-w-prose md:text-xl">
        I'm a freelance software engineer dedicated to using code to
        <span class="underline decoration-double decoration-primary-200 underline-offset-4"
          >help the world solve important problems.</span
        >
      </p>
    </div>
    <figure>
      <!-- <div
          class="w-56 h-56 bg-white relative before:absolute before:w-full before:h-full before:-z-10 before:bg-gradient-to-r before:from-primary-500 before:to-secondary-500 before:left-0 before:top-0 before:blur-[5px]"></div> -->
      <div class="gradient-drop">
        <img
          class="rounded-xl"
          src="/images/headshot.jpg"
          alt="Troy Ciesco" />
      </div>
      <figcaption class="mt-4 flex text-sm text-primary-700">
        <span>I promise I'm better at coding than I am at growing a beard.</span>
      </figcaption>
    </figure>
  </section>
</template>
