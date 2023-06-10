<script setup>
import NavBar from '@/components/NavBarComponent.vue'
</script>

<script>
export default {
    mounted() {

        (function ($) {
            $(window).on('scroll', function () {
                if ($(this).scrollTop() > 120) {
                    $('.header-nav').addClass("sticky")
                } else {
                    $('.header-nav').removeClass("sticky")
                }
            });

            $('[data-parallax]').parallax({
                speed: .6,
            });

        })(window.jQuery)
    }
}
</script>

<template>
    <div class="body-wrap">
        <!-- header area start -->
        <header class="header-area">
            <NavBar />
        </header>
        <!-- header area end -->
        <div class="container">
            <hr>
        </div>



        <!-- fees sec start -->
        <section id="about-us" class="content-sec">
            <div class="container">
                <div class="section-head col-xl-8 m-auto text-center px-5">
                    <span class="label">Get to Know Us</span>
                    <h2 class="title mb-5">
                        About Us
                    </h2>
                </div>
                <div class="auto-container">
                    <div class="outer-box">
                        <div class="row justify-content-center">
                            <div class="col-lg-10">
                                <div class="about-content">
                                    <div style="margin-top: 10px; margin-bottom: 20px">
                                        <p align="justify">The International Conference on Artificial Intelligence and Data
                                            Sciences (AiDAS) is an annual conference organized by College of Computing,
                                            Informatics and Media, Universiti Teknologi MARA, Perak Branch. For the fourth
                                            edition of AiDAS (AiDAS2023), it will be co-organized by Universiti Tunku Abdul
                                            Rahman (UTAR), Malaysia and Universitas Al-Azhar, Indonesia (UAI). This
                                            conference will be technically co-sponsored by IEEE Computer Society, Malaysia
                                            Chapter. AiDAS2023 is also one of the programs organized under Ipoh
                                            International Summit On Professionalism, Research & Education (INSPIREd2023).
                                        </p>
                                    </div>

                                    <div style="margin-top: 10px; margin-bottom: 20px">
                                        <p align="justify">We are delighted to welcome you to this research conference with
                                            proceeding publication in IEEE Xplore (indexed by SCOPUS), where we bring
                                            together scholars, researchers, and professionals internationally to present and
                                            discuss the latest advancements in the field of artificial intelligence and data
                                            science. This conference serves as a platform for the exchange of knowledge,
                                            fostering collaboration, and igniting new ideas to drive future progress in
                                            these rapidly evolving disciplines. By featuring high-quality research papers,
                                            the conference aims to enhance the scientific community's understanding of AI
                                            and data science applications and contribute to the growing body of knowledge in
                                            these areas. Join us in this intellectually stimulating environment as we
                                            collectively work towards shaping the future of technology and transforming the
                                            world through the power of AI and data sciences.</p>
                                    </div>
                                    <br>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <div class="shape">
                <img src="../assets/images/shape/5.svg" alt="Shape">
            </div>
        </section>
        <!-- pricing sec end -->

        <!-- footer area start -->
        <footer class="footer-area">
            <div class="container">
                <div class="footer-top">
                    <div class="row">
                        <div class="col-lg-6 mb-3 mb-lg-0">
                            <div class="row">
                                <div class="col-sm-6 col-lg-8">
                                    <div class="footer-info">
                                        <a href="/" class="footer-logo">
                                            <img src="../assets/images/logo/logo.png"
                                                style="filter: brightness(0) invert(1);" width="250" alt="Footer Logo">
                                        </a>
                                        <div class="footer-desc mb-2">
                                            Follow our social page:
                                        </div>
                                        <ul class="footer-social social">
                                            <li>
                                                <a href="#"><i class="fa-brands fa-facebook-f"></i></a>
                                            </li>
                                            <li>
                                                <a href="#"><i class="fa-brands fa-linkedin-in"></i></a>
                                            </li>
                                            <li>
                                                <a href="#"><i class="fa-brands fa-twitter"></i></a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                        <div class="col-lg-6">
                            <div class="row">
                                <div class="d-flex justify-content-lg-center">
                                    <div class="footer-contact custom-item">
                                        <h5 class="title mb-3">About</h5>
                                        <ul class="contact-item">
                                            <li class="d-flex align-items-center gap-3">
                                                <div class="icon"><img src="../assets/images/icon/calendar2.svg"
                                                        alt="Calendar"></div>
                                                <a href="#" class="calendar-link">6 & 7 September 2023</a>
                                            </li>
                                            <li class="d-flex align-items-center gap-3">
                                                <div class="icon"><img src="../assets/images/icon/map-pin2.svg" alt="Map">
                                                </div>
                                                <a href="#" class="location-link">Virtual Conference</a>
                                            </li>
                                            <li class="d-flex align-items-center gap-3">
                                                <div class="icon"><img src="../assets/images/icon/mail2.svg" alt="Mail">
                                                </div>
                                                <a href="mailto:aidas@uitm.edu.my" class="mail-link">aidas@uitm.edu.my</a>
                                            </li>
                                        </ul>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
                <hr>
                <div class="footer-copyright-area text-center pb-3">
                    <span>Copyright © 2023 All Rights Reserved by <a href="#">UiTM Perak</a></span>
                </div>
            </div>
        </footer>
        <!-- footer area end -->
    </div>
</template>

<style scoped>#particle-wave {
    width: 100%;
    height: 100%;
    bottom: 0;
    position: absolute;
    z-index: -999;
    background-color: transparent;
}</style>