<template>
  <div
    class="min-h-screen bg-gradient-to-br from-[#FFF5F1] via-[#F5E6FF] to-[#E5F4FF] font-sans"
  >
    <nav
      :class="[
        'fixed top-0 w-full z-40 transition-all duration-300',
        scrolled
          ? 'bg-white/90 backdrop-blur-lg shadow-sm py-4'
          : 'bg-transparent py-6',
      ]"
    >
      <div class="max-w-6xl mx-auto px-6 flex items-center justify-between">
        <a href="#" class="text-2xl font-bold text-[#1E293B]">RGavit</a>

        <div class="hidden md:flex items-center gap-8">
          <button
            v-for="s in sections"
            :key="s"
            @click="scrollTo(s)"
            class="text-sm font-medium text-gray-600 hover:text-[#FF6B35] transition-colors capitalize"
          >
            {{ s }}
          </button>
        </div>

        <div
          class="hidden md:flex items-center gap-5 bg-white py-2 px-4 rounded-2xl shadow-sm"
        >
          <a
            href="https://github.com/Rahul-Gavit"
            target="_blank"
            rel="noopener noreferrer"
            class="text-[#1E293B] hover:text-[#FF6B35] hover:scale-110 transition-all duration-300"
            aria-label="GitHub"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="28"
              height="28"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M12 0c-6.626 0-12 5.373-12 12 0 5.302 3.438 9.8 8.207 11.387.599.111.793-.261.793-.577v-2.234c-3.338.726-4.033-1.416-4.033-1.416-.546-1.387-1.333-1.756-1.333-1.756-1.089-.745.083-.729.083-.729 1.205.084 1.839 1.237 1.839 1.237 1.07 1.834 2.807 1.304 3.492.997.107-.775.418-1.305.762-1.604-2.665-.305-5.467-1.334-5.467-5.931 0-1.311.469-2.381 1.236-3.221-.124-.303-.535-1.524.117-3.176 0 0 1.008-.322 3.301 1.23.957-.266 1.983-.399 3.003-.404 1.02.005 2.047.138 3.006.404 2.291-1.552 3.297-1.23 3.297-1.23.653 1.653.242 2.874.118 3.176.77.84 1.235 1.911 1.235 3.221 0 4.609-2.807 5.624-5.479 5.921.43.372.823 1.102.823 2.222v3.293c0 .319.192.694.801.576 4.765-1.589 8.199-6.086 8.199-11.386 0-6.627-5.373-12-12-12z"
              />
            </svg>
          </a>

          <a
            href="https://www.linkedin.com/in/rahulgavit"
            target="_blank"
            rel="noopener noreferrer"
            class="text-[#1E293B] hover:text-[#FF6B35] hover:scale-110 transition-all duration-300"
            aria-label="LinkedIn"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="28"
              height="28"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M19 0h-14c-2.761 0-5 2.239-5 5v14c0 2.761 2.239 5 5 5h14c2.762 0 5-2.239 5-5v-14c0-2.761-2.238-5-5-5zm-11 19h-3v-11h3v11zm-1.5-12.268c-.966 0-1.75-.79-1.75-1.764s.784-1.764 1.75-1.764 1.75.79 1.75 1.764-.783 1.764-1.75 1.764zm13.5 12.268h-3v-5.604c0-3.368-4-3.113-4 0v5.604h-3v-11h3v1.765c1.396-2.586 7-2.777 7 2.476v6.759z"
              />
            </svg>
          </a>

          <a
            href="https://leetcode.com/u/Its_Me_Rahul/"
            target="_blank"
            rel="noopener noreferrer"
            class="text-[#1E293B] hover:text-[#FF6B35] hover:scale-110 transition-all duration-300"
            aria-label="LeetCode"
          >
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="28"
              height="28"
              viewBox="0 0 24 24"
              fill="currentColor"
            >
              <path
                d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.665 2.665 0 0 1 .614-1.164L9.36 9.614l2.76-2.536a1.374 1.374 0 0 1-.038-1.936l1.63-1.666a1.374 1.374 0 0 1 1.935-.038L15.9 8.358a1.374 1.374 0 0 1 .038 1.936l-3.921 4.006h4.536a1.374 1.374 0 0 1 1.374 1.374v1.658a1.374 1.374 0 0 1-1.374 1.374H6.84a1.374 1.374 0 0 1-1.374-1.374v-1.658a1.374 1.374 0 0 1 1.374-1.374h2.128l3.666-3.746-2.738-2.798-2.76 2.536a3.021 3.021 0 0 0-.693 1.314 3.021 3.021 0 0 0-.075.592c-.024.9.296 1.73.948 2.37l4.276 4.193.02.019a1.644 1.644 0 0 0 2.292-.02l2.396-2.392a1.378 1.378 0 0 1 1.951.003c.537.541.537 1.415-.003 1.955l-2.396 2.392c-2.211 2.207-5.815 2.239-8.063.074l-.039-.038-4.277-4.193a4.563 4.563 0 0 1-1.271-1.818 4.453 4.453 0 0 1-.349-1.017 4.15 4.15 0 0 1-.062-2.362c.04-.173.082-.345.125-.513A3.89 3.89 0 0 1 3.262 10.352l3.854-4.126 5.406-5.35a1.374 1.374 0 0 1 1.936.038l.458.468a1.374 1.374 0 0 1-.038 1.936l-1.395 1.425z"
              />
            </svg>
          </a>
        </div>
        <button
          @click="isMobileMenuOpen = true"
          class="md:hidden text-3xl text-[#1E293B] focus:outline-none"
        >
          ☰
        </button>
      </div>
    </nav>

    <div
      v-show="isMobileMenuOpen"
      class="fixed inset-0 bg-white/95 backdrop-blur-md z-50 flex flex-col items-center justify-center transition-opacity duration-300"
    >
      <button
        @click="isMobileMenuOpen = false"
        class="absolute top-6 right-6 text-4xl text-[#1E293B] hover:text-[#FF6B35]"
      >
        &times;
      </button>
      <div class="flex flex-col gap-6 items-center">
        <button
          v-for="s in sections"
          :key="'mobile-' + s"
          @click="scrollTo(s)"
          class="text-2xl font-bold text-[#1E293B] hover:text-[#FF6B35] transition-colors capitalize"
        >
          {{ s }}
        </button>
        <a
          href="/Rahul_Awesome_Resume.pdf"
          download
          class="mt-6 px-8 py-3 bg-[#FF6B35] text-white rounded-full font-semibold hover:bg-[#FF5722] transition-all shadow-lg shadow-orange-200"
        >
          Download CV
        </a>
      </div>
    </div>

    <main class="max-w-6xl mx-auto px-6 pt-32 pb-20">
      <section id="home" class="min-h-[90vh] flex items-center reveal-up">
        <div class="grid md:grid-cols-2 gap-12 items-center w-full">
          <div class="space-y-6">
            <h1
              class="text-5xl md:text-6xl font-bold text-[#1E293B] leading-tight"
            >
              Hy! I Am<br />
              <span class="text-[#1E293B]">Rahul Gavit</span>
            </h1>

            <p class="text-gray-600 text-lg leading-relaxed max-w-md">
              Software Engineer & Full-Stack Developer. I build high-performance
              web applications, bridging the gap between pixel-perfect
              interfaces and scalable backend systems.
            </p>

            <button
              class="px-8 py-3 bg-[#FF6B35] text-white rounded-full font-semibold hover:bg-[#FF5722] hover:scale-105 transition-all shadow-lg shadow-orange-200"
            >
              Hire Me
            </button>

            <div class="pt-6">
              <p class="text-sm text-gray-500 font-medium mb-4">
                Work For All This Brand & Client
              </p>
              <div class="flex items-center gap-4 flex-wrap">
                <div
                  class="w-8 h-8 bg-white rounded-lg shadow-sm flex items-center justify-center text-xl"
                >
                  💼
                </div>
                <div
                  class="w-8 h-8 bg-white rounded-lg shadow-sm flex items-center justify-center text-xl"
                >
                  🏢
                </div>
                <div
                  class="w-8 h-8 bg-white rounded-lg shadow-sm flex items-center justify-center text-xl"
                >
                  🚀
                </div>
                <div
                  class="w-8 h-8 bg-white rounded-lg shadow-sm flex items-center justify-center text-xl"
                >
                  💡
                </div>
                <div
                  class="w-8 h-8 bg-white rounded-lg shadow-sm flex items-center justify-center text-xl"
                >
                  ⚡
                </div>
              </div>
            </div>
          </div>

          <div class="relative">
            <div
              class="absolute -top-4 -right-4 w-3 h-3 bg-red-400 rounded-full"
            ></div>
            <div
              class="absolute top-20 -left-8 w-3 h-3 bg-blue-400 rounded-full"
            ></div>
            <div
              class="absolute bottom-32 -right-8 w-3 h-3 bg-green-400 rounded-full"
            ></div>
            <div
              class="absolute bottom-12 left-12 w-3 h-3 bg-purple-400 rounded-full"
            ></div>

            <div
              class="relative bg-gradient-to-br from-purple-100 to-pink-100 rounded-3xl p-8 mx-auto max-w-md"
            >
              <img
                src="/RahulPic.jpg"
                alt="Rahul Gavit"
                class="w-full h-auto rounded-2xl"
              />

              <div
                class="absolute -top-6 -right-6 bg-white rounded-2xl shadow-xl p-3 flex items-center gap-2 animate-float"
              >
                <div
                  class="w-10 h-10 bg-yellow-100 rounded-xl flex items-center justify-center text-xl"
                >
                  🏆
                </div>
                <div class="text-left">
                  <p class="text-xs font-bold text-gray-800">GATE 2026</p>
                  <p class="text-xs text-gray-500">Qualified</p>
                </div>
              </div>

              <div
                class="absolute bottom-20 -left-8 bg-white rounded-2xl shadow-xl p-3 animate-float-delayed"
              >
                <div class="flex items-center gap-2 mb-1">
                  <div
                    class="w-8 h-8 bg-orange-100 rounded-lg flex items-center justify-center text-lg"
                  >
                    🎨
                  </div>
                  <p class="text-xs font-bold text-gray-800">UI/UX Dev</p>
                </div>
                <p class="text-xs text-gray-500">
                  Vue 3, Nuxt.js,<br />Tailwind CSS
                </p>
              </div>

              <div
                class="absolute -bottom-6 -right-6 bg-white rounded-2xl shadow-xl p-4 w-24 h-24 flex flex-col items-center justify-center animate-float"
              >
                <div
                  class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center text-xl mb-1"
                >
                  ⚙️
                </div>
                <div class="w-16 h-1 bg-gray-200 rounded-full mb-1"></div>
                <div class="w-12 h-1 bg-gray-200 rounded-full mb-1"></div>
                <div class="w-14 h-1 bg-gray-200 rounded-full"></div>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="services" class="py-20 reveal-up">
        <div class="grid md:grid-cols-2 gap-12 items-start">
          <div class="space-y-4">
            <div
              v-for="(service, idx) in services"
              :key="service.name"
              :class="[
                'bg-white rounded-3xl p-6 shadow-lg hover:shadow-xl transition-all cursor-pointer border-2',
                idx === 0
                  ? 'border-gradient-to-r from-pink-300 to-purple-300'
                  : 'border-transparent',
              ]"
              :style="
                idx === 0
                  ? 'background: linear-gradient(white, white) padding-box, linear-gradient(135deg, #FFB6C1, #DDA0DD) border-box;'
                  : ''
              "
            >
              <div class="flex items-start gap-4">
                <div
                  class="w-14 h-14 bg-gradient-to-br from-pink-100 to-purple-100 rounded-2xl flex items-center justify-center text-2xl flex-shrink-0"
                >
                  {{ service.icon }}
                </div>
                <div>
                  <h3 class="text-xl font-bold text-[#1E293B] mb-2">
                    {{ service.name }}
                  </h3>
                  <p class="text-gray-500 text-sm leading-relaxed">
                    {{ service.desc }}
                  </p>
                </div>
              </div>
            </div>

            <div class="flex justify-center pt-4">
              <div
                class="w-10 h-10 bg-black rounded-full flex items-center justify-center text-white cursor-pointer hover:scale-110 transition-transform"
              >
                ↓
              </div>
            </div>
          </div>

          <div class="space-y-6 md:pt-8">
            <h2
              class="text-4xl md:text-5xl font-bold text-[#1E293B] leading-tight"
            >
              My Awesome<br />
              <span class="text-[#FF6B35]">Expertise</span>
            </h2>

            <p class="text-gray-600 leading-relaxed">
              With a strong foundation in Computer Engineering, I specialize in
              architecting scalable SaaS platforms, responsive UI dashboards,
              and robust backend ecosystems.
            </p>

            <p class="text-gray-600 leading-relaxed">
              My industry experience spans across tools like Next.js, Node.js,
              Prisma, and MongoDB. Whether it's reducing HTML report sizes by
              30% or refactoring architecture for 20+ application screens, I
              focus on delivering optimized, high-quality code.
            </p>

            <a
              href="/Rahul_Awesome_Resume.pdf"
              download
              class="inline-block px-8 py-3 bg-[#FF6B35] text-white rounded-full font-semibold hover:bg-[#FF5722] hover:scale-105 transition-all shadow-lg shadow-orange-200 mt-4"
            >
              Download CV
            </a>
          </div>
        </div>
      </section>

      <section class="py-20 reveal-up">
        <div class="grid md:grid-cols-2 gap-12 items-center">
          <div class="space-y-6">
            <h2
              class="text-4xl md:text-5xl font-bold text-[#1E293B] leading-tight"
            >
              Bridging The Gap Between<br />
              Design &<br />
              Performance
            </h2>

            <p class="text-gray-600 leading-relaxed">
              I am dedicated to crafting digital experiences that are not only
              visually appealing but structurally sound and highly optimized for
              user engagement.
            </p>

            <div class="bg-orange-50 rounded-2xl p-6 space-y-3">
              <div class="flex items-start gap-3">
                <span class="text-[#FF6B35] font-bold">1.</span>
                <p class="text-gray-700 font-medium">
                  Scalable Web Applications
                </p>
              </div>
              <div class="flex items-start gap-3">
                <span class="text-[#FF6B35] font-bold">2.</span>
                <p class="text-gray-700 font-medium">
                  Seamless API Integrations
                </p>
              </div>
              <div class="flex items-start gap-3">
                <span class="text-[#FF6B35] font-bold">3.</span>
                <p class="text-gray-700 font-medium">
                  Responsive & Accessible UI
                </p>
              </div>
            </div>
          </div>

          <div class="relative">
            <div
              class="absolute -top-4 -left-4 w-3 h-3 bg-blue-400 rounded-full"
            ></div>
            <div
              class="absolute top-12 -right-8 w-3 h-3 bg-red-400 rounded-full"
            ></div>
            <div
              class="absolute bottom-20 -left-8 w-3 h-3 bg-purple-400 rounded-full"
            ></div>

            <div
              class="relative bg-gradient-to-br from-blue-100 to-purple-100 rounded-3xl p-8"
            >
              <img
                src="/RahulPic.jpg"
                alt="Rahul"
                class="w-full h-auto rounded-2xl"
              />

              <div
                class="absolute -top-6 -right-6 bg-white rounded-2xl shadow-xl p-4 w-20 h-20 flex items-center justify-center animate-float"
              >
                <div
                  class="w-12 h-12 bg-green-100 rounded-full flex items-center justify-center text-2xl"
                >
                  ✓
                </div>
              </div>

              <div
                class="absolute -bottom-6 left-8 bg-white rounded-2xl shadow-xl p-3 animate-float-delayed"
              >
                <div class="flex items-center gap-2 mb-1">
                  <div
                    class="w-8 h-8 bg-orange-100 rounded-full flex items-center justify-center text-lg"
                  >
                    💡
                  </div>
                  <p class="text-xs font-bold text-gray-800">Problem Solver</p>
                </div>
                <p class="text-xs text-gray-500">
                  Committed to clean<br />& efficient code
                </p>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="projects" class="py-20 reveal-up">
        <h2
          class="text-4xl md:text-5xl font-bold text-[#1E293B] text-center mb-12"
        >
          Recent Projects
        </h2>

        <div class="grid md:grid-cols-3 gap-6">
          <div
            v-for="(proj, i) in projects"
            :key="i"
            class="group relative bg-gradient-to-br from-blue-600 to-blue-800 rounded-3xl overflow-hidden shadow-xl hover:shadow-2xl transition-all hover:-translate-y-2 flex flex-col h-full"
          >
            <div
              class="relative bg-gradient-to-br from-blue-400 to-purple-600 p-8 flex flex-col items-center justify-center min-h-[200px]"
            >
              <div class="text-6xl mb-4">{{ proj.emoji }}</div>
              <h3
                class="text-2xl font-bold text-white text-center leading-tight"
              >
                {{ proj.name }}
              </h3>
            </div>

            <div class="bg-white p-6 flex flex-col flex-grow">
              <p class="text-gray-600 text-sm mb-4 leading-relaxed flex-grow">
                {{ proj.description }}
              </p>

              <div class="flex flex-wrap gap-2 mb-6">
                <span
                  v-for="tech in proj.tech"
                  :key="tech"
                  class="px-2 py-1 bg-blue-50 text-blue-600 text-xs font-semibold rounded-md"
                >
                  {{ tech }}
                </span>
              </div>

              <div class="flex gap-3 mt-auto">
                <a
                  v-if="proj.liveLink"
                  :href="proj.liveLink"
                  target="_blank"
                  class="flex-1 text-center py-2 bg-[#FF6B35] text-white text-sm font-semibold rounded-lg hover:bg-[#FF5722] transition-colors shadow-md"
                >
                  Live Demo
                </a>
                <a
                  v-if="proj.githubLink"
                  :href="proj.githubLink"
                  target="_blank"
                  class="flex-1 text-center py-2 bg-gray-900 text-white text-sm font-semibold rounded-lg hover:bg-gray-800 transition-colors shadow-md"
                >
                  GitHub
                </a>
              </div>
            </div>
          </div>
        </div>
      </section>

      <section id="education" class="py-20 reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-[#1E293B] mb-12">
          Education
        </h2>
        <div class="grid md:grid-cols-2 gap-8">
          <div
            v-for="edu in education"
            :key="edu.degree"
            class="bg-white rounded-3xl p-8 shadow-lg hover:shadow-xl transition-all"
          >
            <p
              class="text-sm font-semibold text-gray-500 uppercase tracking-wide mb-4"
            >
              {{ edu.year }}
            </p>
            <h3 class="text-2xl font-bold text-[#1E293B] mb-3">
              {{ edu.degree }}
            </h3>
            <p class="text-gray-600 mb-4">{{ edu.college }}</p>
            <div
              v-if="edu.cgpa"
              class="inline-block px-4 py-2 bg-orange-50 text-[#FF6B35] rounded-lg font-semibold text-sm"
            >
              CGPA / {{ edu.cgpa }}
            </div>
          </div>
        </div>
      </section>

      <section id="experience" class="py-20 reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-[#1E293B] mb-12">
          Work Experience
        </h2>

        <div class="space-y-6">
          <div
            v-for="(exp, i) in experiences"
            :key="i"
            class="bg-white rounded-3xl p-8 shadow-lg hover:shadow-xl transition-all"
          >
            <div class="flex flex-wrap items-center gap-4 mb-4">
              <h3 class="text-2xl font-bold text-[#1E293B]">{{ exp.role }}</h3>
              <span class="text-gray-400 hidden md:inline">—</span>
              <span class="text-lg text-gray-600">{{ exp.company }}</span>
              <span
                class="px-4 py-1 bg-orange-50 text-[#FF6B35] rounded-full text-sm font-semibold"
              >
                {{ exp.period }}
              </span>
            </div>

            <ul class="space-y-2 text-gray-600">
              <li
                v-for="pt in exp.points"
                :key="pt"
                class="flex items-start gap-3"
              >
                <span class="text-[#FF6B35] mt-1">•</span>
                <span>{{ pt }}</span>
              </li>
            </ul>
          </div>
        </div>
      </section>

      <section id="skills" class="py-20 reveal-up">
        <h2 class="text-4xl md:text-5xl font-bold text-[#1E293B] mb-12">
          Technical Skills
        </h2>

        <div class="grid md:grid-cols-4 gap-6">
          <div
            v-for="cat in skillCategories"
            :key="cat.name"
            class="bg-white rounded-3xl p-6 shadow-lg hover:shadow-xl transition-all group"
          >
            <div
              class="text-4xl mb-4 group-hover:scale-110 transition-transform"
            >
              {{ cat.icon }}
            </div>
            <h3 class="text-xl font-bold text-[#1E293B] mb-3">
              {{ cat.name }}
            </h3>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="s in cat.skills"
                :key="s"
                class="text-sm px-2 py-1 bg-gray-50 text-gray-600 rounded-md border border-gray-100"
              >
                {{ s }}
              </span>
            </div>
          </div>
        </div>

        <div
          class="mt-8 bg-gradient-to-r from-[#FF6B35] to-[#FF8A5B] rounded-3xl p-8 text-white flex items-center justify-between shadow-xl"
        >
          <div>
            <h3 class="text-3xl font-bold mb-2">GATE CSE 2026 Qualified</h3>
            <p class="text-white/90">Computer Science & Engineering</p>
          </div>
          <div class="text-5xl">🎯</div>
        </div>
      </section>

      <section id="coding-stats" class="py-20 reveal-up">
        <h2
          class="text-4xl md:text-5xl font-bold text-[#1E293B] mb-12 text-center"
        >
          Coding <span class="text-[#FF6B35]">Stats</span>
        </h2>

        <div
          class="bg-white rounded-3xl p-8 md:p-12 shadow-xl border-t-4 border-[#FFA116] max-w-4xl mx-auto group hover:shadow-2xl transition-all duration-300"
        >
          <div class="flex flex-col md:flex-row items-center gap-12">
            <div class="flex-shrink-0 text-center md:text-left">
              <div
                class="inline-flex items-center justify-center w-40 h-40 rounded-full border-[12px] border-gray-50 shadow-inner mb-4 relative group-hover:scale-105 transition-transform duration-500"
              >
                <svg
                  class="absolute inset-0 w-full h-full -rotate-90"
                  viewBox="0 0 100 100"
                >
                  <circle
                    cx="50"
                    cy="50"
                    r="44"
                    fill="none"
                    stroke="#FFA116"
                    stroke-width="12"
                    :stroke-dasharray="276.46"
                    :stroke-dashoffset="
                      loadingStats
                        ? 276.46
                        : 276.46 -
                          276.46 *
                            (leetcodeData.totalSolved /
                              leetcodeData.totalQuestions)
                    "
                    class="transition-all duration-1500 ease-out"
                    stroke-linecap="round"
                  />
                </svg>
                <div
                  class="absolute inset-0 flex flex-col items-center justify-center"
                >
                  <span
                    class="text-4xl font-black text-[#1E293B]"
                    v-if="!loadingStats"
                    >{{ leetcodeData.totalSolved }}</span
                  >
                  <span class="text-xl animate-pulse text-gray-400" v-else
                    >...</span
                  >
                </div>
              </div>
              <h3 class="text-xl font-bold text-gray-800 text-center">
                Problems Solved
              </h3>
              <a
                href="https://leetcode.com/u/rahulgavit/"
                target="_blank"
                class="text-[#FFA116] hover:text-orange-600 font-medium text-sm flex items-center justify-center gap-2 mt-2 transition-colors"
              >
                <svg
                  xmlns="http://www.w3.org/2000/svg"
                  width="16"
                  height="16"
                  viewBox="0 0 24 24"
                  fill="currentColor"
                >
                  <path
                    d="M13.483 0a1.374 1.374 0 0 0-.961.438L7.116 6.226l-3.854 4.126a5.266 5.266 0 0 0-1.209 2.104 5.35 5.35 0 0 0-.125.513 5.527 5.527 0 0 0 .062 2.362 5.83 5.83 0 0 0 .349 1.017 5.938 5.938 0 0 0 1.271 1.818l4.277 4.193.039.038c2.248 2.165 5.852 2.133 8.063-.074l2.396-2.392c.54-.54.54-1.414.003-1.955a1.378 1.378 0 0 0-1.951-.003l-2.396 2.392a3.021 3.021 0 0 1-4.205.038l-.02-.019-4.276-4.193c-.652-.64-.972-1.469-.948-2.263a2.68 2.68 0 0 1 .066-.523 2.665 2.665 0 0 1 .614-1.164L9.36 9.614l2.76-2.536a1.374 1.374 0 0 1-.038-1.936l1.63-1.666a1.374 1.374 0 0 1 1.935-.038L15.9 8.358a1.374 1.374 0 0 1 .038 1.936l-3.921 4.006h4.536a1.374 1.374 0 0 1 1.374 1.374v1.658a1.374 1.374 0 0 1-1.374 1.374H6.84a1.374 1.374 0 0 1-1.374-1.374v-1.658a1.374 1.374 0 0 1 1.374-1.374h2.128l3.666-3.746-2.738-2.798-2.76 2.536a3.021 3.021 0 0 0-.693 1.314 3.021 3.021 0 0 0-.075.592c-.024.9.296 1.73.948 2.37l4.276 4.193.02.019a1.644 1.644 0 0 0 2.292-.02l2.396-2.392a1.378 1.378 0 0 1 1.951.003c.537.541.537 1.415-.003 1.955l-2.396 2.392c-2.211 2.207-5.815 2.239-8.063.074l-.039-.038-4.277-4.193a4.563 4.563 0 0 1-1.271-1.818 4.453 4.453 0 0 1-.349-1.017 4.15 4.15 0 0 1-.062-2.362c.04-.173.082-.345.125-.513A3.89 3.89 0 0 1 3.262 10.352l3.854-4.126 5.406-5.35a1.374 1.374 0 0 1 1.936.038l.458.468a1.374 1.374 0 0 1-.038 1.936l-1.395 1.425z"
                  />
                </svg>
                <span>@rahulgavit</span>
              </a>
            </div>

            <div class="flex-grow w-full space-y-6">
              <div>
                <div class="flex justify-between text-sm font-bold mb-2">
                  <span class="text-[#00b8a3]">Easy</span>
                  <span class="text-gray-700" v-if="!loadingStats"
                    >{{ leetcodeData.easySolved }}
                    <span class="text-gray-400 font-medium"
                      >/ {{ leetcodeData.totalEasy }}</span
                    ></span
                  >
                </div>
                <div
                  class="w-full bg-gray-100 rounded-full h-3 overflow-hidden"
                >
                  <div
                    class="bg-[#00b8a3] h-full rounded-full transition-all duration-1000 ease-out"
                    :style="{
                      width: loadingStats
                        ? '0%'
                        : (leetcodeData.easySolved / leetcodeData.totalEasy) *
                            100 +
                          '%',
                    }"
                  ></div>
                </div>
              </div>

              <div>
                <div class="flex justify-between text-sm font-bold mb-2">
                  <span class="text-[#ffc01e]">Medium</span>
                  <span class="text-gray-700" v-if="!loadingStats"
                    >{{ leetcodeData.mediumSolved }}
                    <span class="text-gray-400 font-medium"
                      >/ {{ leetcodeData.totalMedium }}</span
                    ></span
                  >
                </div>
                <div
                  class="w-full bg-gray-100 rounded-full h-3 overflow-hidden"
                >
                  <div
                    class="bg-[#ffc01e] h-full rounded-full transition-all duration-1000 ease-out"
                    :style="{
                      width: loadingStats
                        ? '0%'
                        : (leetcodeData.mediumSolved /
                            leetcodeData.totalMedium) *
                            100 +
                          '%',
                    }"
                  ></div>
                </div>
              </div>

              <div>
                <div class="flex justify-between text-sm font-bold mb-2">
                  <span class="text-[#ef4743]">Hard</span>
                  <span class="text-gray-700" v-if="!loadingStats"
                    >{{ leetcodeData.hardSolved }}
                    <span class="text-gray-400 font-medium"
                      >/ {{ leetcodeData.totalHard }}</span
                    ></span
                  >
                </div>
                <div
                  class="w-full bg-gray-100 rounded-full h-3 overflow-hidden"
                >
                  <div
                    class="bg-[#ef4743] h-full rounded-full transition-all duration-1000 ease-out"
                    :style="{
                      width: loadingStats
                        ? '0%'
                        : (leetcodeData.hardSolved / leetcodeData.totalHard) *
                            100 +
                          '%',
                    }"
                  ></div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </main>

    <footer class="bg-white border-t border-gray-100 py-8">
      <div
        class="max-w-6xl mx-auto px-6 flex flex-col sm:flex-row items-center justify-between gap-4"
      >
        <p class="text-gray-600 font-semibold">RGavit</p>

        <div class="flex items-center gap-8">
          <a
            href="#home"
            class="text-[#FF6B35] font-semibold hover:text-[#FF5722] transition-colors"
            >Home</a
          >
          <a
            href="#services"
            class="text-gray-600 font-semibold hover:text-[#FF6B35] transition-colors"
            >Expertise</a
          >
          <a
            href="#projects"
            class="text-gray-600 font-semibold hover:text-[#FF6B35] transition-colors"
            >Projects</a
          >
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const scrolled = ref(false);
const isMobileMenuOpen = ref(false);

const sections = [
  "home",
  "services",
  "projects",
  "experience",
  "education",
  "skills",
];

const services = [
  {
    name: "Frontend Development",
    icon: "🎨",
    desc: "Building highly scalable, responsive UI with Vue 3, Nuxt.js, Next.js, and Tailwind CSS.",
  },
  {
    name: "Backend Engineering",
    icon: "⚙️",
    desc: "Developing secure RESTful APIs and background jobs using Node.js, Express.js, Prisma ORM, and PostgreSQL.",
  },
  {
    name: "Full-Stack Integration",
    icon: "🚀",
    desc: "Seamlessly connecting front-end interfaces with back-end architectures for robust SaaS platforms.",
  },
];

const skillCategories = [
  {
    name: "Languages",
    icon: "💻",
    skills: ["C", "Java", "JavaScript", "TypeScript", "SQL"],
  },
  {
    name: "Frontend",
    icon: "🎨",
    skills: ["Vue 3", "Nuxt.js", "React.js", "Next.js", "Tailwind CSS"],
  },
  {
    name: "Backend",
    icon: "⚙️",
    skills: ["Node.js", "Express.js", "MySQL", "MongoDB", "Prisma"],
  },
  {
    name: "Architecture & Tools",
    icon: "🏗️",
    skills: ["Git", "Redux", "Zustand", "Pinia", "Postman", "DSA"],
  },
];

const experiences = [
  {
    role: "Software Developer Intern",
    company: "WaveNxt Technology",
    period: "March 2025",
    type: "Remote",
    points: [
      "Developed back-end systems using Node.js, MongoDB, and EJS to generate optimized offline HTML reports.",
      "Integrated Plotly.js for interactive data visualization.",
      "Optimized report generation, reducing HTML report size by 30%, improving performance and accessibility.",
    ],
  },
  {
    role: "Software Engineer Intern",
    company: "Ascenwork Technologies",
    period: "Feb 2024 – July 2024",
    type: "Mumbai",
    points: [
      "Developed and optimized scalable, responsive UI for the Easy HR SaaS platform using Vue 3, Nuxt.js, Tailwind CSS, and Pinia.",
      "Built and integrated core HR modules including Leave Management and Attendance System.",
      "Refactored frontend architecture, improving UI consistency across 20+ application screens.",
    ],
  },
  {
    role: "Backend Developer Intern",
    company: "TCR Innovation",
    period: "Jun 2023 – Aug 2023",
    type: "Navi Mumbai",
    points: [
      "Developed backend using Node.js and Express.js, implementing CRUD operations & RESTful APIs.",
      "Identified and resolved bugs in back-end services through API testing using Postman.",
    ],
  },
];

const projects = [
  {
    name: "AI Finance Management",
    emoji: "💰",
    description:
      "A full-stack SaaS platform featuring real-time income/expense tracking, recurring transactions via Inngest, and automated receipt scanning using Google Gemini AI.",
    tech: ["Next.js 15", "Prisma", "PostgreSQL", "Gemini AI", "Tailwind"],
    liveLink: "https://wealth-dun.vercel.app/", // Replace with your actual Live Link
    githubLink: "https://github.com/Rahul-Gavit/Wealth", // Replace with your actual GitHub Link
  },
  {
    name: "E-Store Platform",
    emoji: "🛒",
    description:
      "A comprehensive e-commerce site featuring secure user authentication, dynamic product pages, cart management with Zustand, and an intuitive admin panel.",
    tech: ["React.js", "Next.js", "Material UI", "Zustand", "NextAuth"],
    liveLink: "https://e-store-007.vercel.app/", // Replace with your actual Live Link
    githubLink: "https://github.com/Rahul-Gavit/e-store", // Replace with your actual GitHub Link
  },
  {
    name: "Easy HR SaaS",
    emoji: "🏢",
    description:
      "Scalable frontend architecture for an HR management platform handling Leave & Attendance modules across 20+ application screens.",
    tech: ["Vue 3", "Nuxt.js", "Pinia", "Tailwind CSS"],
    liveLink: null,
    githubLink: null,
  },
];

const education = [
  {
    degree: "B.E. in Computer Engineering",
    college: "Bharati Vidyapeeth College Of Engineering, Navi Mumbai",
    year: "Sep 2019 – July 2023",
    cgpa: "8.41",
  },
  {
    degree: "12th, Science",
    college: "Karmaveer Bhaurao Patil College, Navi Mumbai",
    year: "2019",
    cgpa: null,
  },
];

// --- LeetCode Stats Logic ---
const loadingStats = ref(true);
const leetcodeData = ref({
  totalSolved: 0,
  totalQuestions: 1, // Prevent division by zero initially
  easySolved: 0,
  mediumSolved: 0,
  hardSolved: 0,
  totalEasy: 1,
  totalMedium: 1,
  totalHard: 1,
});

const fetchLeetCodeStats = async () => {
  try {
    // Swapped to a much more stable Vercel-hosted API
    const response = await fetch(
      "https://leetcode-api-faisalshohag.vercel.app/Its_Me_Rahul",
    );
    const data = await response.json();

    // The Vercel API doesn't use the 'status: success' wrapper,
    // so we just check if totalSolved exists
    if (data && data.totalSolved !== undefined) {
      leetcodeData.value = {
        totalSolved: data.totalSolved,
        totalQuestions: data.totalQuestions,
        easySolved: data.easySolved,
        mediumSolved: data.mediumSolved,
        hardSolved: data.hardSolved,
        totalEasy: data.totalEasy,
        totalMedium: data.totalMedium,
        totalHard: data.totalHard,
      };
    }
  } catch (error) {
    console.error("Error fetching LeetCode stats:", error);
  } finally {
    loadingStats.value = false;
  }
};
// -----------------------------

const scrollTo = (id) => {
  isMobileMenuOpen.value = false;
  document.getElementById(id)?.scrollIntoView({ behavior: "smooth" });
};

const handleScroll = () => {
  scrolled.value = window.scrollY > 50;
};

let observer;

onMounted(() => {
  fetchLeetCodeStats(); // <--- Add this line here
  window.addEventListener("scroll", handleScroll);

  observer = new IntersectionObserver(
    (entries) => {
      entries.forEach((entry) => {
        if (entry.isIntersecting) {
          entry.target.classList.add("active");
        }
      });
    },
    { threshold: 0.1, rootMargin: "0px 0px -50px 0px" },
  );

  document.querySelectorAll(".reveal-up").forEach((el) => observer.observe(el));
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
  if (observer) observer.disconnect();
});
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700;800;900&display=swap");

* {
  font-family: "Inter", sans-serif;
}

/* Animations */
@keyframes float {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-10px);
  }
}

@keyframes float-delayed {
  0%,
  100% {
    transform: translateY(0px);
  }
  50% {
    transform: translateY(-15px);
  }
}

.animate-float {
  animation: float 3s ease-in-out infinite;
}

.animate-float-delayed {
  animation: float-delayed 3s ease-in-out infinite;
  animation-delay: 1.5s;
}

/* Reveal Animation */
.reveal-up {
  opacity: 0;
  transform: translateY(30px);
  transition:
    opacity 0.8s cubic-bezier(0.16, 1, 0.3, 1),
    transform 0.8s cubic-bezier(0.16, 1, 0.3, 1);
}

.reveal-up.active {
  opacity: 1;
  transform: translateY(0);
}

/* Smooth Scrolling */
html {
  scroll-behavior: smooth;
}
</style>
