<template>
  <footer class="bg-white dark:bg-gray-900 border-t border-gray-200 dark:border-gray-800 pt-12 pb-8 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex flex-col md:flex-row justify-between items-center text-center md:text-left">
        
        <div class="mb-6 md:mb-0">
          <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-2">Muhammad Ishaque Nizamani</h3>
          <p class="text-gray-500 dark:text-gray-400 text-sm max-w-sm">
            Backend & Machine Learning Engineer specializing in robust backends, AI integration, and scalable databases.
          </p>
        </div>
        
        <div class="flex flex-col space-y-2 text-sm text-gray-500 dark:text-gray-400">
              <span>📍 Pakistan</span>
              <span>✉️ <a href="mailto:ishaque.niz786@gmail.com" class="hover:text-indigo-500 transition-colors">ishaque.niz786@gmail.com</a></span>
              <span>📞 +92-346-4897524</span>
        </div>
      </div>
      
      <div class="mt-8 border-t border-gray-200 dark:border-gray-800 pt-8 flex flex-col md:flex-row justify-between items-center">
        <p class="text-sm text-gray-500 dark:text-gray-400">
          &copy; {{ new Date().getFullYear() }} Muhammad Ishaque Nizamani. All rights reserved.
        </p>
        
        <div class="flex space-x-6 mt-4 md:mt-0">
          <a href="https://github.com/MuhammadNizamani" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-gray-900 dark:hover:text-white transition-colors">
            <span class="sr-only">GitHub</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path fill-rule="evenodd" d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z" clip-rule="evenodd" />
            </svg>
          </a>
          
          <a href="https://www.linkedin.com/in/muhammad-ishaque-nizamani-109a13194/" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-600 dark:hover:text-blue-400 transition-colors">
             <span class="sr-only">LinkedIn</span>
             <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
               <path d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"/>
             </svg>
          </a>

          <a href="https://x.com/NizamaniIshaque" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-black dark:hover:text-white transition-colors">
             <span class="sr-only">X (Twitter)</span>
             <svg class="h-5 w-5 mt-0.5" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
               <path d="M18.244 2.25h3.308l-7.227 8.26 8.502 11.24H16.17l-5.214-6.817L4.99 21.75H1.68l7.73-8.835L1.254 2.25H8.08l4.713 6.231zm-1.161 17.52h1.833L7.084 4.126H5.117z"/>
             </svg>
          </a>

          <a href="https://www.kaggle.com/muhammadishaque" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-blue-500 dark:hover:text-blue-400 transition-colors">
             <span class="sr-only">Kaggle</span>
             <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
               <path d="M18.825 23.859c-.022.092-.117.141-.281.141h-3.139c-.187 0-.351-.082-.492-.248l-5.178-6.009-1.448 1.474v4.341c0 .298-.12.441-.362.441h-2.923c-.244 0-.363-.143-.363-.441v-23.12c0-.295.119-.441.363-.441h2.923c.243 0 .362.146.362.441v14.453l5.59-5.694c.143-.162.308-.242.492-.242h3.295c.189 0 .285.074.285.207.009.057 0 .106-.021.157L11.534 10.37l7.29 13.489z"/>
             </svg>
          </a>

          <a href="https://dev.to/muhammadnizamani" target="_blank" rel="noopener noreferrer" class="text-gray-400 hover:text-black dark:hover:text-white transition-colors">
            <span class="sr-only">Dev.to</span>
            <svg class="h-6 w-6" fill="currentColor" viewBox="0 0 24 24" aria-hidden="true">
              <path d="M7.42 10.05c-.18-.16-.46-.23-.84-.23H6l.02 2.44.04 2.45.56-.02c.41 0 .63-.07.83-.26.24-.24.26-.36.26-2.2 0-1.91-.02-1.96-.29-2.18zM0 4.94v14.12h24V4.94H0zM8.56 15.3c-.44.58-1.06.77-2.53.77H4.71V8.53h1.4c1.67 0 2.16.18 2.6.9.27.43.29.6.32 2.57.05 2.23-.02 2.73-.47 3.3zm5.09-5.47h-2.47v1.77h1.52v1.28l-1.52.02v1.8h2.52l.02 1.3H8.84V8.54h4.81l.02 1.29zm8.15 4.31c-.13.73-.62 1.34-1.32 1.63-.3.12-.56.14-1.28.14-.98 0-1.12-.01-1.46-.2-.68-.37-1.1-1.07-1.1-1.83v-.35l1.52-.02v.2c0 .54.21.94.57 1.1.28.12.92.05 1.15-.12.29-.21.41-.53.41-.99V14c0-.95-.12-1.29-.44-1.61-.31-.3-.69-.42-1.26-.42h-.37L18 10.74h.47c.69 0 1.05-.13 1.34-.48.2-.24.27-.47.27-1.05 0-.58-.08-.85-.3-1.06-.28-.27-.58-.33-1.3-.33-.67 0-1.06.13-1.26.43-.18.27-.22.46-.24 1.21l-1.5-.02v-.39c0-.79.06-.99.3-1.4.37-.65 1.05-1.02 1.95-1.02.72 0 1.23.16 1.6.5.34.33.48.65.52 1.23.04.6-.08 1.02-.37 1.31-.22.2-.44.31-.83.42.5.11.83.33 1.05.7.2.33.25.68.25 1.48 0 .84-.04 1-.21 1.36h-.01z"/>
            </svg>
          </a>
        </div>
      </div>
    </div>
  </footer>
</template>
