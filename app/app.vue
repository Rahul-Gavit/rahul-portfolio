<template>
  <div
    class="min-h-screen bg-[#050505] text-neutral-200 font-sans selection:bg-white selection:text-black antialiased"
  >
    <nav
      :class="[
        'fixed top-0 w-full z-50 transition-all duration-500 border-b',
        scrolled
          ? 'bg-[#050505]/80 backdrop-blur-xl border-neutral-800 py-4'
          : 'bg-transparent border-transparent py-6',
      ]"
    >
      <div
        class="max-w-7xl mx-auto px-6 md:px-12 flex items-center justify-between"
      >
        <a
          href="#"
          class="text-xl font-bold tracking-tighter text-white uppercase flex items-center gap-2"
        >
          <div class="w-2 h-2 bg-white rounded-full animate-pulse"></div>
          RG.
        </a>

        <div class="hidden md:flex items-center gap-8">
          <button
            v-for="s in sections"
            :key="s"
            @click="scrollTo(s)"
            class="text-sm font-medium uppercase tracking-widest text-neutral-400 hover:text-white transition-colors relative group"
          >
            {{ s }}
            <span
              class="absolute -bottom-2 left-0 w-0 h-[1px] bg-white transition-all duration-300 group-hover:w-full"
            ></span>
          </button>
        </div>

        <a
          href="/Rahul_Awesome_Resume.pdf"
          download
          class="hidden sm:inline-flex items-center justify-center px-6 py-2.5 text-sm font-bold uppercase tracking-wider bg-white text-black rounded-full hover:bg-neutral-200 hover:scale-105 transition-all"
        >
          Download CV
        </a>
      </div>
    </nav>

    <main class="max-w-7xl mx-auto px-6 md:px-12 pt-32 pb-24 space-y-32">
      <!-- <section
        id="hero"
        class="min-h-[80vh] flex flex-col justify-center reveal-up"
      >
        <div
          class="inline-flex items-center gap-3 px-4 py-2 rounded-full border border-neutral-800 bg-neutral-900/50 backdrop-blur-sm w-fit mb-8"
        >
          <span class="relative flex h-2 w-2">
            <span
              class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75"
            ></span>
            <span
              class="relative inline-flex rounded-full h-2 w-2 bg-green-500"
            ></span>
          </span>
          <span
            class="text-xs font-semibold uppercase tracking-widest text-neutral-300"
            >Available for Opportunities</span
          >
        </div>

        <h1
          class="text-[12vw] sm:text-[8vw] md:text-8xl lg:text-[110px] font-black uppercase leading-[0.9] tracking-tighter text-white mb-8"
        >
          Rahul <br />
          <span class="text-neutral-500">Gavit_</span>
        </h1>

        <div
          class="flex flex-col md:flex-row md:items-end justify-between gap-8 mt-4 border-t border-neutral-800 pt-8"
        >
          <p
            class="max-w-xl text-lg md:text-xl text-neutral-400 font-light leading-relaxed"
          >
            I am a
            <strong class="text-white font-medium"
              >Software Engineer & Full-Stack Developer</strong
            >. I build high-performance web applications, bridging the gap
            between pixel-perfect interfaces and scalable backend systems.
          </p>

          <div class="flex gap-4">
            <a
              href="https://github.com/Rahul-Gavit"
              target="_blank"
              class="w-12 h-12 rounded-full border border-neutral-800 flex items-center justify-center text-neutral-400 hover:text-white hover:border-white hover:bg-white/5 transition-all"
            >
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.155-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0 1 12 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.741 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"
                />
              </svg>
            </a>
            <a
              href="mailto:itsmerahulgavit@gmail.com"
              class="w-12 h-12 rounded-full border border-neutral-800 flex items-center justify-center text-neutral-400 hover:text-white hover:border-white hover:bg-white/5 transition-all"
            >
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <rect
                  x="2"
                  y="4"
                  width="20"
                  height="16"
                  rx="2"
                  stroke-width="1.5"
                />
                <polyline points="2,4 12,13 22,4" stroke-width="1.5" />
              </svg>
            </a>
          </div>
        </div>
      </section> -->

      <section
        id="hero"
        class="min-h-[80vh] flex flex-col justify-center reveal-up"
      >
        <div
          class="inline-flex items-center gap-3 px-4 py-2 rounded-full border border-neutral-800 bg-neutral-900/50 backdrop-blur-sm w-fit mb-8"
        >
          <span class="relative flex h-2 w-2">
            <span
              class="animate-ping absolute inline-flex h-full w-full rounded-full bg-green-400 opacity-75"
            ></span>
            <span
              class="relative inline-flex rounded-full h-2 w-2 bg-green-500"
            ></span>
          </span>
          <span
            class="text-xs font-semibold uppercase tracking-widest text-neutral-300"
            >Available for Opportunities</span
          >
        </div>

        <div
          class="flex flex-col justify-around md:flex-row md:items-center gap-8 lg:gap-16 mb-8"
        >
          <h1
            class="text-[12vw] sm:text-[8vw] md:text-8xl lg:text-[110px] font-black uppercase leading-[0.9] tracking-tighter text-white shrink-0"
          >
            Rahul <br />
            <span class="text-neutral-500">Gavit_</span>
          </h1>

          <div
            class="max-md:hidden w-48 h-48 md:w-56 md:h-56 lg:w-72 lg:h-72 rounded-full overflow-hidden border border-neutral-800 bg-neutral-900 shrink-0 grayscale hover:grayscale-0 transition-all duration-500"
          >
            <img
              src="/RahulPic.jpg"
              alt="Rahul Gavit"
              class="w-full h-full object-cover"
            />
          </div>
        </div>

        <div
          class="flex flex-col md:flex-row md:items-end justify-between gap-8 mt-4 border-t border-neutral-800 pt-8"
        >
          <p
            class="max-w-xl text-lg md:text-xl text-neutral-400 font-light leading-relaxed"
          >
            I am a
            <strong class="text-white font-medium"
              >Software Engineer & Full-Stack Developer</strong
            >. I build high-performance web applications, bridging the gap
            between pixel-perfect interfaces and scalable backend systems.
          </p>

          <div class="flex gap-4">
            <a
              href="https://github.com/Rahul-Gavit"
              target="_blank"
              class="w-12 h-12 rounded-full border border-neutral-800 flex items-center justify-center text-neutral-400 hover:text-white hover:border-white hover:bg-white/5 transition-all"
            >
              <svg class="w-5 h-5" fill="currentColor" viewBox="0 0 24 24">
                <path
                  d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.155-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0 1 12 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.741 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"
                />
              </svg>
            </a>
            <a
              href="mailto:itsmerahulgavit@gmail.com"
              class="w-12 h-12 rounded-full border border-neutral-800 flex items-center justify-center text-neutral-400 hover:text-white hover:border-white hover:bg-white/5 transition-all"
            >
              <svg
                class="w-5 h-5"
                fill="none"
                stroke="currentColor"
                viewBox="0 0 24 24"
              >
                <rect
                  x="2"
                  y="4"
                  width="20"
                  height="16"
                  rx="2"
                  stroke-width="1.5"
                />
                <polyline points="2,4 12,13 22,4" stroke-width="1.5" />
              </svg>
            </a>
          </div>
        </div>
      </section>

      <section id="skills" class="reveal-up">
        <div
          class="flex flex-col md:flex-row justify-between md:items-end gap-6 mb-12 border-b border-neutral-800 pb-8"
        >
          <h2
            class="text-4xl md:text-5xl font-black uppercase tracking-tighter text-white"
          >
            Expertise
          </h2>
          <p
            class="text-neutral-500 uppercase tracking-widest text-sm font-semibold"
          >
            Technical Arsenal
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-4">
          <div
            v-for="(cat, idx) in skillCategories"
            :key="cat.name"
            class="p-8 border border-neutral-800 bg-neutral-950 hover:bg-neutral-900 transition-colors group"
          >
            <div
              class="text-3xl text-neutral-600 group-hover:text-white transition-colors mb-8 font-light"
            >
              {{ cat.icon }}
            </div>
            <h3
              class="text-lg font-bold text-white uppercase tracking-wider mb-4"
            >
              {{ cat.name }}
            </h3>
            <div class="flex flex-wrap gap-2">
              <span
                v-for="s in cat.skills"
                :key="s"
                class="text-sm text-neutral-400"
              >
                {{ s }}<span class="text-neutral-700 ml-2">/</span>
              </span>
            </div>
          </div>
        </div>

        <div
          class="mt-4 p-8 border border-neutral-800 bg-white text-black flex flex-col sm:flex-row items-start sm:items-center justify-between gap-6 hover:-translate-y-1 transition-transform"
        >
          <div>
            <h4 class="text-2xl font-black uppercase tracking-tighter">
              GATE CSE 2026 Qualified
            </h4>
            <p
              class="text-sm font-medium text-neutral-600 mt-1 uppercase tracking-widest"
            >
              Computer Science & Engineering
            </p>
          </div>
          <div class="text-3xl">🎯</div>
        </div>
      </section>

      <section id="experience" class="reveal-up">
        <div
          class="flex flex-col md:flex-row justify-between md:items-end gap-6 mb-12 border-b border-neutral-800 pb-8"
        >
          <h2
            class="text-4xl md:text-5xl font-black uppercase tracking-tighter text-white"
          >
            Experience
          </h2>
          <p
            class="text-neutral-500 uppercase tracking-widest text-sm font-semibold"
          >
            Career Timeline
          </p>
        </div>

        <div class="flex flex-col">
          <div
            v-for="(exp, i) in experiences"
            :key="i"
            class="group border-b border-neutral-800/50 py-10 flex flex-col md:flex-row gap-6 md:gap-12 hover:bg-neutral-900/30 transition-colors px-4 -mx-4 rounded-xl"
          >
            <div class="md:w-1/4 shrink-0">
              <span
                class="text-sm font-bold uppercase tracking-widest text-neutral-500"
                >{{ exp.period }}</span
              >
            </div>

            <div class="md:w-3/4">
              <div class="flex flex-col sm:flex-row sm:items-center gap-4 mb-4">
                <h3
                  class="text-2xl font-bold text-white uppercase tracking-tight"
                >
                  {{ exp.role }}
                </h3>
                <span class="hidden sm:block text-neutral-700">—</span>
                <span class="text-lg text-neutral-400 font-medium">{{
                  exp.company
                }}</span>
                <span
                  class="text-xs px-3 py-1 border border-neutral-800 rounded-full text-neutral-500 uppercase tracking-widest"
                  >{{ exp.type }}</span
                >
              </div>

              <ul
                class="space-y-3 text-neutral-400 font-light leading-relaxed list-none pl-0"
              >
                <li
                  v-for="pt in exp.points"
                  :key="pt"
                  class="relative pl-6 before:content-[''] before:absolute before:left-0 before:top-2.5 before:w-1.5 before:h-1.5 before:bg-neutral-600 before:rounded-full"
                >
                  {{ pt }}
                </li>
              </ul>
            </div>
          </div>
        </div>
      </section>

      <section id="projects" class="reveal-up">
        <div
          class="flex flex-col md:flex-row justify-between md:items-end gap-6 mb-12 border-b border-neutral-800 pb-8"
        >
          <h2
            class="text-4xl md:text-5xl font-black uppercase tracking-tighter text-white"
          >
            Selected Work
          </h2>
          <p
            class="text-neutral-500 uppercase tracking-widest text-sm font-semibold"
          >
            Featured Projects
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
          <div
            v-for="(proj, i) in projects"
            :key="i"
            class="group relative flex flex-col p-8 border border-neutral-800 bg-[#0a0a0a] hover:border-neutral-500 transition-colors min-h-[400px]"
          >
            <div class="flex justify-between items-start mb-12">
              <div
                class="text-6xl font-black text-neutral-800 group-hover:text-white transition-colors duration-500"
              >
                {{ String(i + 1).padStart(2, "0") }}
              </div>
              <div class="flex gap-3">
                <a
                  :href="proj.github"
                  target="_blank"
                  class="w-10 h-10 rounded-full bg-neutral-900 border border-neutral-800 flex items-center justify-center text-neutral-400 hover:text-white hover:bg-neutral-800 transition-all z-10"
                >
                  <svg class="w-4 h-4" fill="currentColor" viewBox="0 0 24 24">
                    <path
                      d="M12 2C6.477 2 2 6.477 2 12c0 4.418 2.865 8.166 6.839 9.489.5.092.682-.217.682-.482 0-.237-.009-.868-.013-1.703-2.782.604-3.369-1.34-3.369-1.34-.454-1.155-1.11-1.463-1.11-1.463-.908-.62.069-.608.069-.608 1.003.07 1.531 1.03 1.531 1.03.892 1.529 2.341 1.087 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.11-4.555-4.943 0-1.091.39-1.984 1.029-2.683-.103-.253-.446-1.27.098-2.647 0 0 .84-.269 2.75 1.025A9.578 9.578 0 0 1 12 6.836c.85.004 1.705.114 2.504.336 1.909-1.294 2.747-1.025 2.747-1.025.546 1.377.202 2.394.1 2.647.64.699 1.028 1.592 1.028 2.683 0 3.842-2.339 4.687-4.566 4.935.359.309.678.919.678 1.852 0 1.336-.012 2.415-.012 2.741 0 .267.18.578.688.48C19.138 20.163 22 16.418 22 12c0-5.523-4.477-10-10-10z"
                    />
                  </svg>
                </a>
                <a
                  :href="proj.live"
                  target="_blank"
                  class="w-10 h-10 rounded-full bg-white flex items-center justify-center text-black hover:scale-110 transition-all z-10"
                >
                  <svg
                    class="w-4 h-4"
                    fill="none"
                    stroke="currentColor"
                    viewBox="0 0 24 24"
                  >
                    <path
                      stroke-linecap="round"
                      stroke-linejoin="round"
                      stroke-width="2"
                      d="M14 5l7 7m0 0l-7 7m7-7H3"
                    ></path>
                  </svg>
                </a>
              </div>
            </div>

            <div class="mt-auto">
              <h3
                class="text-2xl font-bold text-white uppercase tracking-tight mb-4"
              >
                {{ proj.name }}
              </h3>
              <p class="text-neutral-400 font-light mb-6">{{ proj.desc }}</p>

              <div class="flex flex-wrap gap-2">
                <span
                  v-for="t in proj.stack"
                  :key="t"
                  class="px-3 py-1 text-xs font-bold uppercase tracking-widest border border-neutral-800 text-neutral-300"
                >
                  {{ t }}
                </span>
              </div>
            </div>

            <div
              class="absolute inset-0 bg-white/[0.02] opacity-0 group-hover:opacity-100 transition-opacity pointer-events-none"
            ></div>
          </div>
        </div>
      </section>

      <section id="education" class="reveal-up">
        <div
          class="flex flex-col md:flex-row justify-between md:items-end gap-6 mb-12 border-b border-neutral-800 pb-8"
        >
          <h2
            class="text-4xl md:text-5xl font-black uppercase tracking-tighter text-white"
          >
            Academics
          </h2>
          <p
            class="text-neutral-500 uppercase tracking-widest text-sm font-semibold"
          >
            Education History
          </p>
        </div>

        <div class="grid grid-cols-1 md:grid-cols-2 gap-4">
          <div
            v-for="edu in education"
            :key="edu.degree"
            class="p-8 border border-neutral-800 bg-[#0a0a0a]"
          >
            <span
              class="text-sm font-bold uppercase tracking-widest text-neutral-500 block mb-4"
              >{{ edu.year }}</span
            >
            <h3
              class="text-xl font-bold text-white uppercase tracking-tight mb-2"
            >
              {{ edu.degree }}
            </h3>
            <p class="text-neutral-400 font-light mb-6">{{ edu.college }}</p>
            <span
              v-if="edu.cgpa"
              class="inline-block px-4 py-1.5 border border-neutral-700 bg-neutral-900 text-white text-sm font-bold uppercase tracking-widest"
            >
              CGPA / {{ edu.cgpa }}
            </span>
          </div>
        </div>
      </section>
    </main>

    <footer
      id="contact"
      class="border-t border-neutral-800 bg-[#050505] reveal-up"
    >
      <div class="max-w-7xl mx-auto px-6 md:px-12 py-32 text-center">
        <h2
          class="text-5xl md:text-8xl font-black uppercase tracking-tighter text-white mb-8"
        >
          Let's work <br />
          together.
        </h2>

        <div class="flex flex-wrap items-center justify-center gap-4 mb-20">
          <a
            href="mailto:itsmerahulgavit@gmail.com"
            class="px-8 py-4 bg-white text-black font-bold uppercase tracking-widest text-sm hover:bg-neutral-200 transition-colors"
          >
            Get in touch
          </a>
          <a
            href="/Rahul_Awesome_Resume.pdf"
            download
            class="px-8 py-4 border border-neutral-800 text-white font-bold uppercase tracking-widest text-sm hover:border-neutral-500 transition-colors"
          >
            Download Resume
          </a>
        </div>

        <div
          class="flex flex-col md:flex-row items-center justify-between gap-6 pt-12 border-t border-neutral-800 text-sm font-bold uppercase tracking-widest text-neutral-600"
        >
          <p>© {{ new Date().getFullYear() }} Rahul Gavit</p>
          <div class="flex gap-6">
            <a
              href="https://github.com/Rahul-Gavit"
              target="_blank"
              class="hover:text-white transition-colors"
              >Github</a
            >
            <a
              href="https://rahul-gavit-portfolio.netlify.app"
              target="_blank"
              class="hover:text-white transition-colors"
              >Portfolio</a
            >
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from "vue";

const scrolled = ref(false);
const sections = ["skills", "experience", "projects", "education"];

// --- Data ---
const skillCategories = [
  {
    name: "Languages",
    icon: "</>",
    skills: ["JavaScript", "TypeScript", "Java", "C", "SQL"],
  },
  {
    name: "Frontend",
    icon: "◈",
    skills: ["Vue 3", "Nuxt.js", "React.js", "Next.js", "Tailwind"],
  },
  {
    name: "Backend",
    icon: "◄",
    skills: ["Node.js", "Express.js", "MySQL", "MongoDB", "Prisma"],
  },
  {
    name: "Architecture",
    icon: "⊞",
    skills: ["Git", "Redux", "Zustand", "Pinia", "DSA"],
  },
];

const experiences = [
  {
    role: "Software Developer Intern",
    company: "WaveNxt Technology",
    period: "Mar 2025",
    type: "Remote",
    points: [
      "Engineered robust backend systems leveraging Node.js and MongoDB.",
      "Designed offline HTML reports utilizing Plotly.js for interactive data visualization.",
      "Reduced HTML report size by 30%, optimizing overall performance.",
    ],
  },
  {
    role: "Software Engineer Intern",
    company: "Ascenwork Technologies",
    period: "Feb 2024 – Jul 2024",
    type: "Mumbai",
    points: [
      "Developed a scalable UI for the Easy HR SaaS platform using Vue 3 and Nuxt.js.",
      "Architected core HR modules: Leave Management and Attendance Systems with REST API integration.",
      "Refactored frontend components across 20+ screens, ensuring strict UI consistency.",
    ],
  },
  {
    role: "Backend Developer Intern",
    company: "TCR Innovation",
    period: "Jun 2023 – Aug 2023",
    type: "Navi Mumbai",
    points: [
      "Built scalable RESTful APIs enabling seamless client-server communication.",
      "Executed complex CRUD operations and optimized database queries.",
    ],
  },
];

const projects = [
  {
    name: "AI Finance Manager",
    desc: "Full-stack SaaS with real-time income/expense tracking. Integrated Google Gemini AI for automated receipt scanning and insights.",
    stack: ["Next.js 15", "Prisma", "PostgreSQL", "Gemini AI"],
    live: "https://wealth-dun.vercel.app/",
    github: "https://github.com/Rahul-Gavit/Wealth",
  },
  {
    name: "E-Store Platform",
    desc: "Comprehensive e-commerce ecosystem featuring secure NextAuth authentication, dynamic product routing, and a streamlined admin panel.",
    stack: ["React.js", "Tailwind", "NextAuth", "Zustand"],
    live: "https://e-store-007.vercel.app/",
    github: "https://github.com/Rahul-Gavit/e-store",
  },
];

const education = [
  {
    degree: "B.E. in Computer Engineering",
    college: "Bharati Vidyapeeth College Of Engineering, Navi Mumbai",
    year: "2019 – 2023",
    cgpa: "8.41",
  },
  {
    degree: "Higher Secondary (Science)",
    college: "Karmaveer Bhaurao Patil College, Navi Mumbai",
    year: "2019",
    cgpa: null,
  },
];

// --- Logic & Animations ---

const scrollTo = (id) => {
  document.getElementById(id)?.scrollIntoView({ behavior: "smooth" });
};

const handleScroll = () => {
  scrolled.value = window.scrollY > 50;
};

let observer;

onMounted(() => {
  window.addEventListener("scroll", handleScroll);

  // Scroll Reveal Observer
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
/* Base Typography override for the Brutalist style */
@import url("https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;700;900&display=swap");

html {
  scroll-behavior: smooth;
  font-family: "Inter", sans-serif;
  background-color: #050505;
}

/* Scroll Reveal Animations */
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
</style>
