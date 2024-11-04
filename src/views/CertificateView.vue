<!-- Bagian Certificates -->
<div class="bg-[#2c2c2d] px-5 py-5 md:px-12 md:py-10 text-left border border-[#555555] rounded-3xl text-amber-50 mx-3 mb-5">
    <article data-page="certificates">
      <header>
        <div class="text-2xl font-bold text-white mb-5 fadein-bot title-section flex items-center">
          Certificates &nbsp;
          <div class="h-[1px] w-32 bg-amber-200 md:w-96 aos-init aos-animate" data-aos="zoom-in-left" data-aos-duration="600"></div>
        </div>
      </header>
      <section>
        <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-4">
          <div v-for="certificate in certificates" :key="certificate.id" class="certificate-card">
            <img :src="certificate.imageUrl" alt="Certificate Image" class="rounded-md mb-3" />
            <p class="text-lg font-semibold">{{ certificate.name }}</p>
            <p class="text-sm text-gray-400">{{ certificate.issuer }}</p>
            <p class="text-sm text-gray-400">{{ certificate.date }}</p>
          </div>
        </div>
      </section>
    </article>
  </div>
  