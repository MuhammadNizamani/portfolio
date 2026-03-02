<template>
  <section id="skills" class="py-20 bg-gray-50 dark:bg-gray-800/50 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-extrabold text-gray-900 dark:text-white sm:text-4xl">
          Technical Skills
        </h2>
        <div class="mt-4 flex justify-center">
          <div class="w-24 h-1 bg-indigo-600 dark:bg-indigo-500 rounded"></div>
        </div>
      </div>

      <!-- Skill Logos Marquee -->
      <div class="mb-16 overflow-hidden relative w-full flex items-center bg-white dark:bg-gray-800 py-8 rounded-xl shadow-sm border border-gray-100 dark:border-gray-700">
        <!-- Fade masks for smooth entry/exit edges -->
        <div class="absolute inset-y-0 left-0 w-24 bg-gradient-to-r from-white dark:from-gray-800 to-transparent z-10 pointer-events-none"></div>
        <div class="absolute inset-y-0 right-0 w-24 bg-gradient-to-l from-white dark:from-gray-800 to-transparent z-10 pointer-events-none"></div>
        
        <div class="marquee-content flex items-center gap-16 px-8">
          <img v-for="(logo, i) in duplicatedLogos" :key="i" :src="logo" class="h-16 w-auto max-w-[120px] object-contain transition-transform duration-300 hover:scale-110" alt="Skill Logo" />
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        
        <div v-for="(category, index) in skillCategories" :key="index" class="bg-white dark:bg-gray-900 rounded-xl shadow p-8 border border-gray-100 dark:border-gray-800 hover:border-indigo-500 dark:hover:border-indigo-500 transition-colors group">
          <div class="flex items-center mb-6">
            <div class="p-2 bg-indigo-100 dark:bg-indigo-900/50 rounded-lg text-indigo-600 dark:text-indigo-400 mr-4">
               <!-- Dynamic icon mapping if desired, using a placeholder for now -->
               <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M5 13l4 4L19 7" />
               </svg>
            </div>
            <h3 class="text-xl font-bold text-gray-900 dark:text-white group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors">
              {{ category.name }}
            </h3>
          </div>
          
          <div class="flex flex-wrap gap-2">
            <span v-for="(skill, i) in category.skills" :key="i" class="px-3 py-1.5 bg-gray-100 dark:bg-gray-800 text-gray-700 dark:text-gray-300 rounded-md text-sm font-medium hover:bg-indigo-50 hover:text-indigo-700 dark:hover:bg-indigo-900/80 dark:hover:text-white transition-colors cursor-default">
              {{ skill }}
            </span>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const getImageUrl = (name) => {
  return new URL(`../../assets/skillsLogo/${name}`, import.meta.url).href
}
const logoFiles = [
  'flutter.webp', 'firebase.webp', 'docker.webp', 'rest.webp', 'bootstrap.webp', 'mysql.webp',
  'html.webp', 'Pandas_logo.svg.webp', 'fast.webp', 'dj.webp', 'css.webp', 'tesnor.webp',
  'np.webp', 'git.webp', 'hk.webp', 'gcp.webp', 'md.webp', 'graphql.webp', 'kb.webp',
  'linux.webp', 'pytorch.webp', 'opencv.webp'
]
const skillLogos = logoFiles.map(getImageUrl)
const duplicatedLogos = [...skillLogos, ...skillLogos]

const skillCategories = [
  {
    name: 'Backend',
    skills: ['Django', 'Flask', 'FastAPI', 'Hasura', 'GraphQL', 'Heroku']
  },
  {
    name: 'Machine Learning & Data',
    skills: ['scikit-learn', 'TensorFlow', 'Keras', 'Pandas', 'NumPy', 'Matplotlib']
  },
  {
    name: 'Frontend',
    skills: ['Vue.js', 'Nuxt.js', 'Flutter', 'HTML', 'Tailwind CSS']
  },
  {
    name: 'Tools & DevOps',
    skills: ['Git', 'Docker', 'Linux', 'Bash', 'SQL Server', 'NVM', 'LangChain']
  },
  {
    name: 'Data Science',
    skills: ['Data Processing', 'Visualization', 'Statistical Analysis', 'Computer Vision', 'Predictive Modeling']
  },
  {
    name: 'Cloud Services',
    skills: ['Google Cloud Platform (GCP)', 'Amazon Web Services (AWS)', 'Azure']
  }
]
</script>

<style scoped>
.marquee-content {
  display: inline-flex;
  animation: marquee 40s linear infinite;
  min-width: max-content;
}
.marquee-content:hover {
  animation-play-state: paused;
}
@keyframes marquee {
  0% { transform: translateX(0); }
  100% { transform: translateX(calc(-50% - 2rem)); } 
}
</style>
