<template>
  <section id="projects" class="py-20 bg-white dark:bg-gray-900 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-extrabold text-gray-900 dark:text-white sm:text-4xl">
          Projects & Open Source
        </h2>
        <div class="mt-4 flex justify-center">
          <div class="w-24 h-1 bg-indigo-600 dark:bg-indigo-500 rounded"></div>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Project 1 -->
        <div v-for="(project, index) in projects" :key="index" class="bg-gray-50 dark:bg-gray-800 rounded-2xl shadow-lg hover:shadow-2xl transition-all duration-300 overflow-hidden group border border-gray-100 dark:border-gray-700 flex flex-col h-full transform hover:-translate-y-2">
          
          <div class="p-8 flex-grow">
            <div class="flex items-center justify-between mb-4">
              <div class="p-3 bg-indigo-100 dark:bg-indigo-900/50 rounded-lg text-indigo-600 dark:text-indigo-400">
                <svg v-if="project.type === 'Open Source'" xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 20l4-16m4 4l4 4-4 4M6 16l-4-4 4-4" />
                </svg>
                <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-8 w-8" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                  <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" />
                </svg>
              </div>
              <span class="px-3 py-1 text-xs font-semibold rounded-full" :class="project.type === 'Open Source' ? 'bg-green-100 text-green-800 dark:bg-green-900/30 dark:text-green-400' : 'bg-blue-100 text-blue-800 dark:bg-blue-900/30 dark:text-blue-400'">
                {{ project.type }}
              </span>
            </div>
            
            <h3 class="text-xl font-bold text-gray-900 dark:text-white mb-3 group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors">
              {{ project.title }}
            </h3>
            
            <p class="text-gray-600 dark:text-gray-400 text-sm mb-6 leading-relaxed">
              {{ project.description }}
            </p>

            <div class="flex flex-wrap gap-2 mt-auto">
              <span v-for="(tech, i) in project.techStack" :key="i" class="px-2.5 py-0.5 rounded text-xs font-medium bg-gray-200 text-gray-800 dark:bg-gray-700 dark:text-gray-300">
                {{ tech }}
              </span>
            </div>
          </div>

          <div class="px-8 pb-8 pt-4 border-t border-gray-200 dark:border-gray-700 mt-auto">
            <a v-if="project.link" :href="project.link" target="_blank" class="inline-flex items-center text-indigo-600 dark:text-indigo-400 hover:text-indigo-800 dark:hover:text-indigo-300 font-medium transition-colors">
              <span v-if="project.link.includes('github')">View on GitHub</span>
              <span v-else>Visit Website</span>
              <svg v-if="project.link.includes('github')" xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
              <svg v-else xmlns="http://www.w3.org/2000/svg" class="h-4 w-4 ml-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M10 6H6a2 2 0 00-2 2v10a2 2 0 002 2h10a2 2 0 002-2v-4M14 4h6m0 0v6m0-6L10 14" />
              </svg>
            </a>
          </div>
          
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const projects = [
  {
    title: 'Activist Contributor',
    type: 'Open Source',
    description: 'Proactively identified technical debt and bugs in the open-source repository. Implemented fixes and automated tests, and deciphered complex codebases to resolve critical backend issues, ensuring stable operation.',
    techStack: ['Analysis', 'Testing', 'Backend Architecture', 'Debugging'],
    link: 'https://github.com/activist-org/activist'
  },
  {
    title: 'SchnellTools.de',
    type: 'Client Project',
    description: 'Developed a comprehensive suite of online tools for a German client. Implemented robust SEO strategies to successfully rank the website on Google and secure AdSense approval.',
    techStack: ['Full Stack', 'SEO', 'Performance Optimization'],
    link: 'https://schnelltools.de/'
  },
  {
    title: 'Weddle Unlimited (NFL)',
    type: 'Client Project',
    description: 'Created a popular web-based NFL guessing game (Weddle) for a US client. Architected both the frontend interaction and the backend game logic.',
    techStack: ['Web Development', 'Game Logic', 'Frontend Architecture'],
    link: 'https://weddleunlimited.net/'
  },
  {
    title: 'Anime Plot Creator',
    type: 'Project',
    description: 'Collected data from gogoanime for anime plots, cleaned and trained a decoder transformer model like GPT, achieving impressive 1.5 cross-validation scores.',
    techStack: ['Python', 'Transformers', 'GPT', 'Data Mining'],
    link: 'https://github.com/MuhammadNizamani/AnimePlot/tree/master'
  },
  {
    title: 'Social Media Clone API',
    type: 'Project',
    description: 'Developed a fully functional social media API. Handled the database securely with PostgreSQL, utilizing SQLAlchemy for ORM and Alembic for migrations, deployed directly on Heroku.',
    techStack: ['FastAPI', 'Python', 'PostgreSQL', 'SQLAlchemy', 'Alembic', 'Heroku'],
    link: 'https://github.com/MuhammadNizamani/backend'
  }
]
</script>
