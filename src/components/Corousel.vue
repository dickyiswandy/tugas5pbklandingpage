<template>
    <q-carousel
      animated
      v-model="slide"
      infinite
      navigation
      arrows
      :autoplay="5000"
    >
      <q-carousel-slide
        v-for="(image, index) in images"
        :name="index"
        :img-src="image.src"
        key="index"
      >
        <!-- Caption untuk setiap gambar -->
        <div class="caption">{{ image.caption }}</div>
      </q-carousel-slide>
    </q-carousel>
  </template>
  
  <script>
  export default {
    name: 'MyCarousel',
    data() {
      return {
        slide: 0,
        images: [
          {
            src: 'https://4kwallpapers.com/images/walls/thumbs_3t/13501.jpg',
            caption: 'Ferrari SF90 XX Stradale Race track'
          },
          {
            src: 'https://4kwallpapers.com/images/walls/thumbs_3t/10252.jpg',
            caption: 'Koenigsegg Jesko Supercars'
          },
          {
            src: 'https://4kwallpapers.com/images/walls/thumbs_3t/8082.jpg',
            caption: 'McLaren P1 GTR McLaren NFT Genesis Collection'
          },
          {
            src: 'https://4kwallpapers.com/images/walls/thumbs_3t/9141.jpg',
            caption: 'Hybrid Supercar Ferrari SF90 Stradale Assetto Fiorano'
          },
          {
            src: 'https://4kwallpapers.com/images/walls/thumbs_3t/2798.jpg',
            caption: 'McLaren 765LT 2021 Supercar'
          },
        ]
      }
    }
  }
  </script>
  
  <style scoped>
  .q-carousel {
    height: 600px;
    width: 1500px;
  }
  
  .q-carousel-slide {
    background-position: center;
    background-size: cover;
    display: flex;
    align-items: center;
    justify-content: center;
  }
  
  .caption {
    position: absolute;
    bottom: 20px;
    left: 50%;
    transform: translateX(-50%);
    background-color: rgba(0, 0, 0, 0.5);
    color: #fff;
    padding: 10px;
    border-radius: 10px;
    font-size: 30px;
  }
  </style>