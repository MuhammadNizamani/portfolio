<template>
  <section id="experience" class="py-20 bg-gray-50 dark:bg-gray-800/50 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h2 class="text-3xl font-extrabold text-gray-900 dark:text-white sm:text-4xl">
          Professional Experience
        </h2>
        <div class="mt-4 flex justify-center">
          <div class="w-24 h-1 bg-indigo-600 dark:bg-indigo-500 rounded"></div>
        </div>
      </div>

      <div class="relative">
        <!-- Vertical Timeline Line -->
        <div class="hidden md:block absolute left-1/2 transform -translate-x-1/2 w-0.5 h-full bg-gray-200 dark:bg-gray-700"></div>

        <div class="space-y-12">
          <!-- Experience 1 -->
          <div v-for="(job, index) in experiences" :key="index" class="relative flex flex-col md:flex-row justify-between items-center w-full">
            
            <!-- Timeline Dot -->
            <div class="hidden md:flex absolute left-1/2 transform -translate-x-1/2 w-8 h-8 rounded-full bg-indigo-600 dark:bg-indigo-500 items-center justify-center ring-4 ring-white dark:ring-gray-900 z-10 transition-colors shadow">
              <span class="w-3 h-3 bg-white rounded-full"></span>
            </div>

            <!-- Content Container -->
            <div :class="['w-full md:w-5/12', index % 2 === 0 ? 'md:pr-12 md:text-right' : 'md:pl-12 md:ml-auto']">
              <div class="bg-white dark:bg-gray-900 p-6 rounded-lg shadow-lg hover:shadow-xl transition-shadow border border-gray-100 dark:border-gray-800 relative z-10 group">
                <div class="flex flex-col md:flex-row justify-between items-start md:items-center mb-4" :class="index % 2 === 0 ? 'md:flex-row-reverse' : ''">
                  <div>
                    <h3 class="text-xl font-bold text-gray-900 dark:text-white group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors">{{ job.role }}</h3>
                    <div class="text-lg font-medium text-indigo-600 dark:text-indigo-400 mt-1">{{ job.company }} <span class="text-gray-500 text-sm font-normal">| {{ job.location }}</span></div>
                  </div>
                  <span class="mt-2 md:mt-0 px-3 py-1 bg-indigo-50 dark:bg-indigo-900/30 text-indigo-600 dark:text-indigo-300 text-sm font-semibold rounded-full border border-indigo-100 dark:border-indigo-800">
                    {{ job.duration }}
                  </span>
                </div>
                
                <ul class="text-gray-600 dark:text-gray-400 space-y-2 text-sm text-left list-disc pl-5 mt-4">
                  <li v-for="(detail, i) in job.details" :key="i">
                    {{ detail }}
                  </li>
                </ul>
              </div>
            </div>

          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const experiences = [
  {
    role: 'Backend & Machine Learning Engineer',
    company: 'AIFIST',
    location: 'Hyderabad, Pakistan',
    duration: 'April 2024 to Date',
    details: [
      'Built robust, secure backends with Python, PostgreSQL, and Firebase, implementing authentication and optimized database schemas.',
      'Integrated Google Gemini via LangChain with RAG pipelines and vector-based PostgreSQL retrieval for real-time educational insights.',
      'Developed responsive, high-speed web applications using Vue.js and Pinia, optimizing state management.',
      'Implemented cloud-based deployment strategies, Firebase Storage, DDoS mitigation, rate-limiting, and strict security protocols.',
      'Led code reviews, resolved critical issues, and enforced rigorous testing and maintenance standards.'
    ]
  },
  {
    role: 'Backend Developer',
    company: 'Quantum Leap',
    location: 'London, UK (Remote)',
    duration: 'Sep 2023 to Feb 2024',
    details: [
      'Designed robust database structures to support complex engineering design data, ensuring high data integrity.',
      'Engineered high-performance backend systems using Django to integrate AI-powered design tools.',
      'Orchestrated deployment and maintenance of the platform on Render, ensuring stable operations.'
    ]
  },
  {
    role: 'Machine Learning Engineer',
    company: 'IVY',
    location: 'London, UK (Remote)',
    duration: 'May 2023 to April 2024',
    details: [
      'Actively contributed code, bug fixes, and features to the Ivy open-source repository.',
      'Collaborated effectively within community through code reviews and discussions.',
      'Engaged in design discussions and addressed user-reported issues on community forums.',
      'Promoted Ivy through blog posts, tutorials, and conference presentations.'
    ]
  },
  {
    role: 'Backend Developer',
    company: 'Erxa',
    location: 'Kuwait City (Remote)',
    duration: 'May 2022 to April 2023',
    details: [
      'Architected a healthcare communication platform connecting doctors and pharmacies to streamline prescriptions.',
      'Developed secure RESTful APIs using Django and Flask for scalable backend services in sensitive environments.',
      'Engineered optimized MySQL databases and deployed full-stack solutions on Heroku for 24/7 accessibility.'
    ]
  },
  {
    role: 'Machine Learning Engineer',
    company: 'AIME',
    location: 'London, UK (Remote)',
    duration: 'May 2021 to April 2022',
    details: [
      'Engineered a Python-based FAQ chatbot with tailored NLP models, automating company support.',
      'Built proprietary datasets from scratch for Japanese-language accuracy and model reliability.',
      'Developed high-precision OCR models for automated extraction of financial invoice data.',
      'Designed scalable RESTful APIs to integrate AI-driven NLP and OCR processes into business operations.',
      'Streamlined end-to-end document pipelines, automating form filling and reducing operational overhead.'
    ]
  }
]
</script>
