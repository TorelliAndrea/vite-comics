<script>
export default {
   name: "TheFooter",
   data() {
      return {
         footerLinks: [
            {
               title: "DC COMICS",
               links: ["Characters", "Comics", "Movies", "TV", "Games", "Videos", "News"]
            },
            {
               title: "SHOP",
               links: ["Shop DC", "Shop DC Collectables"]
            },
            {
               title: "DC",
               links: ["Terms Of Use", "Provacy Policy (New)", "Ad Choices", "Advertising", "Jobs", "Subscriptions", "Talent Workshops", "CPSC Certificates", "Ratings", "Shop Help", "Contast Us"]
            },
            {
               title: "SITES",
               links: ["DC", "MAD Magazine", "DC Kids", "DC Universe", "DC Power Visa"]
            },
         ]
      };
   },
}
</script>

<template>
   <div class="sfondo overflow-hidden">
      <div class="container py-5 d-flex justify-content-between position-relative">
         <div class="liste d-flex flex-column flex-wrap">
            <div v-for="(gruppo, i) in footerLinks" class="px-3">
               <h4 class="text-white fw-bold">{{ gruppo.title }}</h4>
               <ul class="list-unstyled">
                  <li v-for="link in gruppo.links">
                     <a :href="link">{{ link }}</a>
                  </li>
               </ul>
            </div>
         </div>
         <img src="img/dc-logo-bg.png" alt="logo DC">
      </div>
   </div>
</template>

<style lang="scss" scoped>
.sfondo {
   background-image: url(../../public/img/footer-bg.jpg);
}

.container {
   height: 50vh;
}

a {
   color: gray;
   text-decoration: none;
   transition: all 0.4s ease;

   &:hover{
      color: #0282F9;
      font-weight: bold;
      text-decoration: underline;
   }
}

img {
   position: absolute;
   right: 0;
   top: -45px;
}
</style>

