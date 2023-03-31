<template>
  <q-page padding>
    <section class="row justify-start items-start text-left q-px-xl" style="height:85vh">
      <div class="col-xs-11 col-sm-6 col-md-6 q-mr-xl">
        <div class="text-h2 q-mb-md">
          About Me
        </div>

        <div class="col-4 items-center lt-sm">
        <q-img
          style="width:200px"
          src="../assets/faces/00_real-one.png"
          :ratio="2/3"
          spinner-color="primary"
          spinner-size="82px"
          bordered
        >
        <div class="bg-green-7 absolute-bottom-right text-subtitle2">
          Muhammad Rivandra
        </div>
      </q-img>
      </div>

        <div class="text-p q-mb-md q-py-md q-pr-sm">
          <div class="text-bold">Hello! I am a recent graduate in <strong>Industrial Engineering</strong> from <strong>Andalas University</strong> who has been passionately learning <strong>web development</strong> since late 2020. I have a strong understanding of various web development technologies and methodologies, and I am excited to apply my skills and knowledge to create exceptional web applications.</div>
          <br>
          I believe nobody should suffer, feel confused, or, even worse, feel stupid while using a product, whether it's a website, mobile app, or any physical product around.
          In my four years of study as an industrial engineer, I learned how to make a system efficient, effective, productive, and user-friendly. I apply that everywhere I go. I am always thinking of ways to make things faster, easier, and cheaper.
          <br><br>
          <div class="text-bold">If you need to improve a system or create a user-friendly web app, feel free to contact me.</div>
        </div>
        <q-btn class="q-mb-xl" outline color="positive" icon="download" label="Download CV" href="https://drive.google.com/file/d/18GVTAIuyr6hM-zmLBp8iYHtfeEBi7o_V/view?usp=drivesdk" target="_blank"/>
      </div>
      <div class="col-4 items-center gt-xs">
        <q-img
          style="width:200px"
          src="../assets/faces/00_real-one.png"
          :ratio="2/3"
          spinner-color="primary"
          spinner-size="82px"
          bordered
        >
        <div class="bg-green-7 absolute-bottom-right text-subtitle2">
          Muhammad Rivandra
        </div>
      </q-img>
      </div>
    </section>
  </q-page>
</template>

<script>
export default {
  // name: 'PageName',
}
</script>
