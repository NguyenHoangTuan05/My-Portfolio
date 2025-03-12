<template>
 <div class="bg-[#111827] min-h-screen">
<!-- Wrap components in Suspense to handle loading -->
   <Suspense>
     <template #default>
<!--   Wrap all Components inside a single root element   -->
       <div>
         <Navbar />
         <HeroSection />
         <ServiceSection />
         <AboutSection />
         <ExperienceAndSkills />
         <LatestProjSection/>
         <ContactSection />
         <TestimonialsSection />
         <Footer />
         <BacktoTop />
       </div>
     </template>
     <template #fallback>
       <div class="flex justify-center items-center min-h-screen">
         <loadingSpinner />
       </div>
     </template>
   </Suspense>
 </div>
</template>

<script setup>
import { defineAsyncComponent } from 'vue';
import BackToTop from "@/components/BackToTop.vue";
//import HeroSection from "@/components/HeroSection.vue";
//import Components Asynchronously
//import Navbar from "./components/NavBar.vue";
const Navbar = defineAsyncComponent(()=> import('@/components/NavBar.vue'));
const HeroSection = defineAsyncComponent(()=> import('@/components/HeroSection.vue'));
const ServiceSection = defineAsyncComponent(()=> import('@/components/ServicesSection.vue'));
const AboutSection = defineAsyncComponent(()=> import('@/components/AboutSection.vue'));
const ExperienceAndSkills = defineAsyncComponent(()=> import('@/components/ExperienceAndSkills.vue'));
const LatestProjSection = defineAsyncComponent(()=> import('@/components/LatestProjSection.vue'));
const ContactSection = defineAsyncComponent(()=> import('@/components/ContactSection.vue'));
const TestimonialsSection = defineAsyncComponent(()=> import('@/components/TestimonialsSection.vue'));
const Footer = defineAsyncComponent(()=> import('@/components/Footer.vue'));
const BacktoTop = defineAsyncComponent(()=> import('@/components/BackToTop.vue'));
const loadingSpinner = defineAsyncComponent(()=> import('@/components/loadingSpinner.vue'));
</script>
<style>
*{
  scrollbar-width: thin;
  scrollbar-color: #111827 #f1f1f1;
}
</style>
