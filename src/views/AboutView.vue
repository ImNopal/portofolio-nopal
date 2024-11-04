<template>
  <!-- Bagian About Me -->
  <div class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="about">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          About Me &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>
      <section class="text-sm md:text-lg text-justify flex flex-col gap-4 md:flex-row md:gap-8 md:justify-left md:items-center">
        <div class="flex justify-center">
          <img class="w-9/12 rounded-full mb-3 fadein-up" src="https://i1.sndcdn.com/avatars-000214125831-5q6tdw-t500x500.jpg" alt="Foto">
        </div>
        <div class="md:w-7/12">
          <p class="mb-3 md:mb-7 fadein-left fadeins-1">
            &nbsp; &nbsp; &nbsp; Hi everyone! My name is Naufal Danisha Amri. I am a web developer from Sidoarjo, East Java. I have 1 year of experience in front-end web development. 
            I really enjoy what I do now, in my opinion, creating programs is not just a job, but also art that has aesthetic value.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; My job is to build your website to be functional and user-friendly yet still attractive.
            In addition, I provide a personal touch to your product and ensure that the website catches attention and is
            easy to use.
            My goal is to convey your message and identity in the most creative way. If you are interested in hiring me,
            please contact the listed contact.
          </p>
        </div>
      </section>
    </article>
  </div>

  <!-- Bagian Education -->
  <div class="bg-[#2c2c2d] px-5 py-5 md:px-12 md:py-10 text-left border border-[#555555] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="education">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          Education &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>
      <section>
        <p class="text-lg font-semibold">SMA NEGERI 1 WONOAYU</p>
        <p class="text-sm text-gray-400">2021 - 2024</p>
      </section>
    </article>
  </div>

  <!-- Bagian Skills -->
  <div class="px-5 py-5 md:px-12 md:py-10 text-left text-amber-50 mx-3">
    <article data-page="skills">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          <div class="h-[1px] w-10 bg-amber-200 md:w-20 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
          &nbsp; Skills
        </div>
      </header>
      <section>
        <ul class="flex flex-wrap text-sm font-medium text-center text-gray-500 dark:text-gray-400 mb-5">
          <li class="mr-2">
            <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
              :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 1 }" @click="activeTab = 1">Tech Stack</button>
          </li>
          <li class="mr-2">
            <button class="inline-block px-4 py-3 rounded-lg hover:text-white"
              :class="{ 'text-amber-200 bg-amber-200 bg-opacity-10': activeTab === 2 }" @click="activeTab = 2">Tools</button>
          </li>
        </ul>
        <div v-show="activeTab === 1">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tech" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3 zoom-in">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="HTML" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0">{{ item.name }}</div>
                  <div class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
        <div v-show="activeTab === 2">
          <div class="grid grid-cols-2 gap-4 pb-32 md:grid-cols-3 md:gap-8 xl:grid-cols-4 xl:gap-10 2xl:gap-12">
            <div v-for="item in tools" :key="item.id">
              <div
                class="item-tech flex cursor-pointer items-center gap-2 rounded border border-amber-200 px-2 py-2 hover:bg-amber-200 hover:bg-opacity-10 md:gap-3 lg:px-3">
                <div class="flex h-12 w-12 items-center justify-center p-0 lg:h-16 lg:w-16 lg:p-2 zoom-in">
                  <img alt="Tool" loading="lazy" width="32" height="32" decoding="async" data-nimg="1"
                    class="img-tech drop-shadow-xl transition-all duration-300 h-[65%] w-[65%] lg:h-[85%] lg:w-[85%]"
                    :src="item.imageUrl" style="color: transparent;">
                </div>
                <div class="flex items-center text-sm md:text-base lg:text-lg">
                  <div class="tech font-medium text-secondary transition-all duration-300 translate-y-0">{{ item.name }}</div>
                  <div class="status-tech opacity-0 absolute mt-5 text-[10px] text-amber-200 transition-all duration-300 md:text-xs lg:text-sm">
                    {{ item.status }}</div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
    </article>
  </div>

  <!-- Bagian Certificates -->
  <div class="bg-[#1e1e1f] px-5 py-5 md:px-12 md:py-10 text-left border border-[#383838] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="certificates">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          Certificates &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>
      <section class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-4">
        <div v-for="cert in certificates" :key="cert.id" class="certificate-card bg-[#2c2c2d] p-4 rounded-xl text-center text-amber-50">
          <img :src="cert.imageUrl" :alt="cert.title" class="w-full h-48 object-cover rounded mb-3" />
          <h3 class="text-lg font-semibold">{{ cert.title }}</h3>
          <p class="text-sm">{{ cert.provider }}</p>
          <small class="text-gray-400">{{ cert.date }}</small>
        </div>
      </section>
    </article>
  </div>
</template>

<script>
export default {
  data() {
    return {
      activeTab: 1,
      tech: [
        {
          id: 1,
          name: 'HTML',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/1051/1051277.png',
          status: 'Advanced'
        },
        {
          id: 2,
          name: 'CSS',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/732/732190.png',
          status: 'Advanced'
        },
        {
          id: 3,
          name: 'PHP',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-php-2038871-1720084.png',
          status: 'Advanced'
        },
        {
          id: 4,
          name: 'Javascript',
          imageUrl: 'https://cdn.icon-icons.com/icons2/2415/PNG/512/javascript_original_logo_icon_146455.png',
          status: 'Advance'
        },
        {
          id: 5,
          name: 'Laravel',
          imageUrl: 'https://cdn.worldvectorlogo.com/logos/laravel-2.svg',
          status: 'Advance'
        },
        {
          id: 6,
          name: 'Codeigniter',
          imageUrl: 'https://codeigniter.com/assets/icons/44521256.png',
          status: 'Intermediate'
        },
        {
          id: 7,
          name: 'VueJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-vue-282497.png?f=webp',
          status: 'Intermediate'
        },
        {
          id: 8,
          name: 'AlpineJS',
          imageUrl: 'https://avatars.githubusercontent.com/u/59030169?s=200&v=4',
          status: 'Beginner'
        },
        {
          id: 9,
          name: 'NodeJS',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-node-js-1174925.png',
          status: 'Beginner'
        },
        {
          id: 10,
          name: 'Tailwind',
          imageUrl: 'https://upload.wikimedia.org/wikipedia/commons/d/d5/Tailwind_CSS_Logo.svg',
          status: 'Advance'
        },
        {
          id: 11,
          name: 'Bootstrap',
          imageUrl: 'https://getbootstrap.com/docs/5.2/assets/brand/bootstrap-logo-shadow.png',
          status: 'Intermediate'
        },
        {
          id: 12,
          name: 'ReactJS',
          imageUrl: 'https://cdn4.iconfinder.com/data/icons/logos-3/600/React.js_logo-512.png',
          status: 'Beginner'
        }
        // data tech lainnya
      ],
      tools: [
      {
          id: 1,
          name: 'Git',
          imageUrl: 'https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png',
          status: 'Version Control'
        },
        {
          id: 2,
          name: 'GitHub',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/25/25231.png',
          status: 'Git Hosting'
        },
        {
          id: 3,
          name: 'NPM',
          imageUrl: 'https://cdn.iconscout.com/icon/free/png-256/free-npm-3-1175132.png',
          status: 'Package Manager'
        },
        {
          id: 4,
          name: 'MySQL',
          imageUrl: 'https://cdn-icons-png.flaticon.com/512/5968/5968313.png',
          status: 'Database'
        },
        // data tools lainnya
      ],
      certificates: [
        {
          id: 1,
          name: 'Front-End Web Developer',
          imageUrl: '/img/certificate1.jpg',
          issuer: 'Dicoding',
          date: 'November 2024'
        },
        {
          id: 2,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate11.jpg',
          issuer: 'Udemy',
          date: 'August 2024'
        },
        {
          id: 3,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate10.jpg',
          issuer: 'Udemy',
          date: 'August 2024'
        },
        {
          id: 4,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate2.jpg',
          issuer: 'Udemy',
          date: 'June 2024'
        },
        {
          id: 5,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate12.jpg',
          issuer: 'Udemy',
          date: 'April 2024'
        },
        {
          id: 6,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate9.jpg',
          issuer: 'Udemy',
          date: 'January 2024'
        },
        {
          id: 7,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate3.jpg',
          issuer: 'Udemy',
          date: 'July 2023'
        },
        {
          id: 8,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate4.jpg',
          issuer: 'Udemy',
          date: 'July 2023'
        },
        {
          id: 9,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate5.jpg',
          issuer: 'Udemy',
          date: 'July 2023'
        },
        {
          id: 10,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate6.jpg',
          issuer: 'Udemy',
          date: 'October 2022'
        },
        {
          id: 11,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate7.jpg',
          issuer: 'Udemy',
          date: 'July 2022'
        },
        {
          id: 12,
          name: 'Back-End Development with PHP',
          imageUrl: '/img/certificate8.jpg',
          issuer: 'Udemy',
          date: 'June 2022'
        },
        // tambahkan data sertifikat lainnya di sini
      ]
    };
  }
}
</script>

<style>
.certificate-card {
  padding: 10px; /* Ruang tambahan di sekitar gambar */
  border: 1px solid #383838; /* Warna border */
  border-radius: 12px; /* Bentuk border bulat */
  overflow: hidden; /* Agar gambar tidak keluar dari kartu */
  transition: transform 0.3s ease;
}

.certificate-card:hover {
  transform: scale(1.05); /* Animasi zoom saat hover */
}

.certificate-card img {
  width: 100%; /* Gambar memenuhi lebar container */
  height: 90%; /* Gambar memenuhi tinggi container */
  object-fit: contain; /* Memastikan gambar tidak terpotong */
  padding: 5px; /* Ruang tambahan di sekitar gambar */
  border-radius: 8px; /* Bentuk bulat di sudut gambar */
  box-sizing: border-box;
}

.certificate-card:hover img {
  transform: scale(1.05); /* Sedikit zoom pada gambar saat hover */
}

/* Animasi fade-in dari kiri */
.fadein-left {
  opacity: 0;
  animation: fadeInLeft 0.5s ease-out forwards;
}

@keyframes fadeInLeft {
  0% {
    opacity: 0;
    transform: translateX(100%);
  }

  100% {
    opacity: 1;
    transform: translateX(0);
  }
}

.fadeins-1 {
  animation-delay: 500ms;
}

.fadeins-2 {
  animation-delay: 800ms;
}

.img-tech,
.tech {
  transition: transform 0.3s ease;
}

.item-tech:hover .img-tech {
  transform: scale(1.3);
}

.item-tech:hover .tech {
  transform: translateY(-12px);
}

.item-tech:hover .status-tech {
  opacity: 1;
}
</style>