<template>
  <div>
    <Navigation />
    <Hero />
    <Up />
    <Anatomical />
    <VideoSpain />
    <Services />
    <Team />
    <Metodologia />
    <Footer />
  </div>
</template>

<script>
import Navigation from '@/components/Navigation'
import Hero from '@/components/Hero'
import Up from '@/components/Up'
import Anatomical from '@/components/Anatomical'
import VideoSpain from '@/components/VideoSpain'
import Services from '@/components/Services'
import Team from '@/components/Team'
import Metodologia from '@/components/Metodologia'
import Footer from '@/components/Footer'
export default {
  components: {
    Navigation,
    Hero,
    Up,
    Anatomical,
    VideoSpain,
    Services,
    Team,
    Metodologia,
    Footer,
  },
}
</script>
