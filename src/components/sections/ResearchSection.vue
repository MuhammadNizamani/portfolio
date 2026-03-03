<template>
  <section id="research" class="py-20 bg-gray-50 dark:bg-gray-800/50 transition-colors duration-300">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-16">
        <h5 class="text-sm font-bold text-indigo-600 dark:text-indigo-400 uppercase tracking-widest mb-2">My Focus</h5>
        <h2 class="text-3xl font-extrabold text-gray-900 dark:text-white sm:text-4xl lg:text-5xl">
          Research Interests
        </h2>
        <div class="mt-6 flex justify-center">
          <div class="w-24 h-1 bg-indigo-600 dark:bg-indigo-500 rounded"></div>
        </div>
      </div>

      <div class="grid grid-cols-1 md:grid-cols-2 gap-8">
        <div v-for="(item, index) in researchInterests" :key="index" class="bg-white dark:bg-gray-900 rounded-2xl shadow-lg border border-gray-100 dark:border-gray-700 p-8 hover:shadow-2xl transition-all duration-300 group flex flex-col h-full hover:-translate-y-1">
          <div class="flex items-center mb-6">
            <div class="p-3 bg-indigo-100 dark:bg-indigo-900/50 rounded-xl text-indigo-600 dark:text-indigo-400 mr-4 group-hover:bg-indigo-600 group-hover:text-white transition-colors duration-300">
              <span v-html="item.icon" class="w-8 h-8 flex items-center justify-center"></span>
            </div>
            <h3 class="text-2xl font-bold text-gray-900 dark:text-white group-hover:text-indigo-600 dark:group-hover:text-indigo-400 transition-colors">
              {{ item.title }}
            </h3>
          </div>
          
          <p class="text-gray-600 dark:text-gray-400 text-lg mb-6 leading-relaxed flex-grow">
            {{ item.description }}
          </p>

          <div class="space-y-4 border-t border-gray-100 dark:border-gray-800 pt-6">
            <div v-for="(highlight, hIndex) in item.highlights" :key="hIndex" class="bg-gray-50 dark:bg-gray-800/80 rounded-lg p-4 transition-colors">
              <h4 class="text-sm font-bold text-indigo-600 dark:text-indigo-400 uppercase tracking-wider mb-1">
                {{ highlight.label }}
              </h4>
              <p class="text-gray-700 dark:text-gray-300 text-sm">
                {{ highlight.text }}
              </p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const researchInterests = [
  {
    title: 'AI & Mechanistic Interpretability',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M14.25 9.75L16.5 12l-2.25 2.25m-4.5 0L7.5 12l2.25-2.25M6 20.25h12A2.25 2.25 0 0020.25 18V6A2.25 2.25 0 0018 3.75H6A2.25 2.25 0 003.75 6v12A2.25 2.25 0 006 20.25z" /></svg>',
    description: 'My primary research focus lies in peering into the "black box" of Large Language Models (LLMs). I am specifically interested in understanding how circuit-level behaviors emerge as model depth increases.',
    highlights: [
      { label: 'Current Focus', text: 'Investigating functional differences between 2-layer, 3-layer, and 4-layer attention-only models.' },
      { label: 'Key Question', text: 'Identifying emergent properties (like induction heads) that only manifest at 3L+ architectures and how they contribute to in-context learning.' }
    ]
  },
  {
    title: 'Visual Speech Recognition & Low-Resource Languages',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M12 18v-5.25m0 0a6.01 6.01 0 001.5-.189m-1.5.189a6.01 6.01 0 01-1.5-.189m3.75 7.478a12.06 12.06 0 01-4.5 0m3.75 2.383a14.406 14.406 0 01-3 0M14.25 18v-.192c0-.983.658-1.829 1.58-1.936a4.5 4.5 0 00-4.5-8.436L12 9" /></svg>',
    description: 'I am dedicated to applying Deep Learning to preserve and enhance accessibility for regional languages, particularly focusing on my roots in Pakistan.',
    highlights: [
      { label: 'Thesis Work', text: 'Developing a robust Visual Speech Recognition (VSR) system for the Sindhi language.' },
      { label: 'Methodology', text: 'Designing and curating specialized datasets for Sindhi lip-reading and training models to bridge the gap in Urdu/Sindhi-centric speech technologies.' }
    ]
  },
  {
    title: 'Computer Vision & Automated Systems',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M2.036 12.322a1.012 1.012 0 010-.639C3.423 7.51 7.36 4.5 12 4.5c4.638 0 8.573 3.007 9.963 7.178.07.207.07.431 0 .639C20.577 16.49 16.64 19.5 12 19.5c-4.638 0-8.573-3.007-9.963-7.178z" /><path stroke-linecap="round" stroke-linejoin="round" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" /></svg>',
    description: 'Beyond linguistics, I am interested in how computer vision can be integrated into real-world management systems to solve logistical challenges.',
    highlights: [
      { label: 'Applications', text: 'Utilizing image and video processing for automated health monitoring and identification within livestock management platforms.' }
    ]
  },
  {
    title: 'Full-Stack AI Integration',
    icon: '<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" d="M9.594 3.94c.09-.542.56-.94 1.11-.94h2.593c.55 0 1.02.398 1.11.94l.213 1.281c.063.374.313.686.645.87.074.04.147.083.22.127.324.196.72.257 1.075.124l1.217-.456a1.125 1.125 0 011.37.49l1.296 2.247a1.125 1.125 0 01-.26 1.431l-1.003.827c-.293.24-.438.613-.431.992a6.759 6.759 0 010 .255c-.007.378.138.75.43.99l1.005.828c.424.35.534.954.26 1.43l-1.298 2.247a1.125 1.125 0 01-1.369.491l-1.217-.456c-.355-.133-.75-.072-1.076.124a6.57 6.57 0 01-.22.128c-.331.183-.581.495-.644.869l-.213 1.28c-.09.543-.56.941-1.11.941h-2.594c-.55 0-1.02-.398-1.11-.94l-.213-1.281c-.062-.374-.312-.686-.644-.87a6.52 6.52 0 01-.22-.127c-.325-.196-.72-.257-1.076-.124l-1.217.456a1.125 1.125 0 01-1.369-.49l-1.297-2.247a1.125 1.125 0 01.26-1.431l1.004-.827c.292-.24.437-.613.43-.992a6.932 6.932 0 010-.255c.007-.378-.138-.75-.43-.99l-1.004-.828a1.125 1.125 0 01-.26-1.43l1.297-2.247a1.125 1.125 0 011.37-.491l1.216.456c.356.133.751.072 1.076-.124.072-.044.146-.087.22-.128.332-.183.582-.495.644-.869l.214-1.28zM12 15a3 3 0 100-6 3 3 0 000 6z" /></svg>',
    description: 'Exploring the intersection of modern web architectures and AI deployment to create seamless, data-driven user experiences.',
    highlights: [
      { label: 'Tech Stack', text: 'Developing end-to-end solutions using Python (FastAPI/Flask), Vue.js, and Firebase, with a focus on efficient model serving and state management.' }
    ]
  }
];
</script>
