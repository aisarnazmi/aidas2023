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
        <section id="paper-submission" class="content-sec">
            <div class="container">
                <div class="section-head col-xl-8 m-auto text-center px-5">
                    <span class="label">Author's Guidance</span>
                    <h2 class="title mb-5">
                        Paper Submission
                    </h2>
                </div>
                <div class="auto-container">
                    <div class="outer-box">
                        <div class="row">
                            <div class="col-lg-12">
                                <div class="about-content">
                                    <strong>Step 1</strong>
                                    <div style="margin-top: 10px; margin-bottom: 20px">
                                        <p align="justify">- All manuscripts must be in English.
                                            Your paper must be prepared in A4 size according to IEEE format. Download as
                                            MS-Word DOC,
                                            Latex (Windows) or Latex (UNIX).
                                            The length of your paper should be no more than 6 pages in A4 size, including
                                            figures,
                                            tables and references.
                                        </p>
                                        <p align="justify" style="margin-top: 8px">
                                            For the purpose of review, since we are conducting a double blind review
                                            process, the
                                            author(s) is (are) required to remove their name(s) from the paper.
                                        </p>
                                        <p align="justify" style="margin-top: 8px">Papers submitted for review MUST NOT
                                            contain any author information (no
                                            authors, affiliation or address, and no explicit self-reference). However, the
                                            name(s) of
                                            author(s) need to be included in the final submission.
                                            <u><a target="_blank" title="Click to download document template."
                                                    href="/documents/Conference-Template-2023-A4.docx"
                                                    style="font-size: 15px" download>Download
                                                    template as MS-Word DOC</a></u>
                                        </p>
                                    </div>
                                    <strong>Step 2</strong>
                                    <div style="margin-top: 10px; margin-bottom: 20px">
                                        <p align="justify">- Your paper must be in PDF format.</p>
                                    </div>
                                    <strong>Step 3</strong>
                                    <div style="margin-top: 10px; margin-bottom: 20px">
                                        <p align="left">- Please register and submit your manuscript to
                                            <u><a target="_blank" href="http://submit.confbay.com/conf/aidas2023"
                                                    style="font-size: 15px">http://submit.confbay.com/conf/aidas2023</a></u>
                                        </p>
                                    </div>
                                    <br>
                                    <strong>PLEASE NOTE:</strong>
                                    <p align="justify">- All papers will be reviewed and evaluated based on originality,
                                        technical
                                        quality, and relevance to the conference. Concurrent submission to this conference
                                        and/or
                                        other conferences or journals is not allowed.</p>
                                    <p align="justify">Please note that failure to follow the above instructions may result
                                        in your
                                        paper being excluded from the conference proceedings.</p>
                                    <p align="justify">All author name(s) and contact details should not be included for
                                        first
                                        submission. This is for the blind review process.</p>
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