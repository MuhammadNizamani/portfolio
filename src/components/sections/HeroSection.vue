<template>
  <section id="hero" class="relative pt-32 pb-20 lg:pt-48 lg:pb-32 overflow-hidden flex items-center min-h-[90vh]">
    <!-- Background Decoration -->
    <div class="absolute inset-0 z-0">
      <div class="absolute inset-0 bg-gradient-to-br from-indigo-50 to-white dark:from-gray-900 dark:to-gray-800 opacity-90 transition-colors duration-300"></div>
      <div class="absolute top-0 right-0 -mr-20 -mt-20 w-96 h-96 rounded-full bg-indigo-200 dark:bg-indigo-900 opacity-20 blur-3xl animate-blob"></div>
      <div class="absolute bottom-0 left-0 -ml-20 -mb-20 w-80 h-80 rounded-full bg-purple-200 dark:bg-purple-900 opacity-20 blur-3xl animate-blob animation-delay-2000"></div>
    </div>

    <div class="relative z-10 max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 w-full">
      <div class="text-center md:text-left flex flex-col md:flex-row items-center justify-between">
        
        <div class="md:w-3/5 mb-10 md:mb-0">
          <h1 class="text-4xl tracking-tight font-extrabold text-gray-900 dark:text-white sm:text-5xl md:text-6xl">
            <span class="block mb-2">Hi, I'm</span>
            <span class="block text-indigo-600 dark:text-indigo-400">Muhammad Ishaque</span>
          </h1>
          <h2 class="mt-3 text-xl sm:text-2xl text-gray-600 dark:text-gray-300 font-medium">
            Backend & Machine Learning Engineer
          </h2>
          <p class="mt-5 text-base text-gray-500 dark:text-gray-400 sm:text-lg sm:max-w-xl md:text-xl">
            Passionate about building robust, secure backends, integrating AI/ML technologies, and optimizing databases for high-performance applications.
          </p>
          <div class="mt-8 sm:flex sm:justify-center md:justify-start gap-4">
            <div class="rounded-md shadow">
              <a href="#contact" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-indigo-600 hover:bg-indigo-700 dark:bg-indigo-500 dark:hover:bg-indigo-600 transition-colors md:py-4 md:text-lg md:px-10">
                Get in touch
              </a>
            </div>
            <div class="mt-3 sm:mt-0 rounded-md shadow">
              <a href="#projects" class="w-full flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-indigo-600 bg-white hover:bg-gray-50 dark:text-white dark:bg-gray-800 dark:hover:bg-gray-700 transition-colors md:py-4 md:text-lg md:px-10">
                View Work
              </a>
            </div>
          </div>
        </div>

        <div class="md:w-2/5 flex justify-center">
          <div class="relative group">
            <div class="absolute -inset-1 bg-gradient-to-r from-indigo-600 to-purple-600 rounded-full blur opacity-25 group-hover:opacity-50 transition duration-1000 group-hover:duration-200"></div>
            <img class="relative rounded-full h-64 w-64 object-cover border-4 border-white dark:border-gray-800 shadow-2xl" src="/src/assets/muhammadishaque.png" alt="Muhammad Ishaque" />
          </div>
        </div>
        
      </div>
    </div>
  </section>
</template>
