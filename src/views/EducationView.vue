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
            &nbsp; &nbsp; &nbsp; Hi everyone! My name is Naufal Danisha Amri. I'm a web developer from Sidoarjo, East Java. I have 1 year of experience in back-end web development.
            I really enjoy what I do right now, in my opinion, creating programs is not just a job, but also an art that has aesthetic value.
          </p>
          <p class="mb-3 fadein-left fadeins-2">
            &nbsp; &nbsp; &nbsp; My job is to build your website to be functional and user-friendly yet still attractive.
            In addition, I provide a personal touch to your product and ensure that the website catches attention and is easy to use.
            My goal is to convey your message and identity in the most creative way. If you are interested in hiring me, please contact the listed contact.
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
        <p class="text-sm text-gray-300">Teknik Informatika dan Jaringan</p>
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
        <!-- Bagian tab dan konten Skills Anda seperti sebelumnya -->
      </section>
    </article>
  </div>
</template>

<script>
export default {
  name: 'AboutView'
};
</script>

<style>
.fadein-bot {
  opacity: 0;
  animation: fadeInUp 0.5s ease-out forwards;
}

@keyframes fadeInUp {
  0% { opacity: 0; transform: translateY(100%); }
  100% { opacity: 1; transform: translateY(0); }
}
</style>
