<script setup>
import NavBar from '@/components/NavBar.vue'
</script>

<script>
export default {
	mounted() {
		const $ = window.jQuery;

		/* sticky header - start*/
		$(window).on('scroll', function () {
			if ($(this).scrollTop() > 120) {
				$('.header-nav').addClass("sticky")
			} else {
				$('.header-nav').removeClass("sticky")
			}
		});
		/* sticky header - end */

		/* bg parallax - start */
		$('[data-parallax]').parallax({
			speed: .6,
		});
		/* bg parallax - end */

		/* counter */
		$('.counter-box[data-countdown]').each(function () {
			var $this = $(this), finalDate = $(this).data('countdown');
			$this.countdown(finalDate, function (event) {
				$(this).html(event.strftime(''
					+ '<li class="days"><strong class="day2">%D</strong><span class="d-block">Days</span></li>'
					+ '<li class="hours"><strong class="hours2">%H</strong><span class="d-block">Hours</span></li>'
					+ '<li class="minutes"><strong class="min2">%M</strong><span class="d-block">Minutes</span></li>'
					+ '<li class="seconds"><strong class="sec2">%S</strong><span class="d-block">Seconds</span></li>'));
			});
		});
		/* counter */

		/* magnific popup */
		$('.zoom-gallery').magnificPopup({
			delegate: '.item-thumb',
			type: 'image',
			closeOnContentClick: false,
			closeBtnInside: false,
			mainClass: 'mfp-with-zoom mfp-img-mobile',
			gallery: {
				enabled: true
			},
			zoom: {
				enabled: true,
				duration: 300,
				opener: function (element) {
					return element.find('img');
				}
			}
		});
	}

}
</script>

<template>
	<div class="body-wrap">
		<!-- header area start -->
		<header class="header-area">
			<NavBar />

			<!-- hero sec start -->
			<section class="hero-sec">
				<div class="hero-slider-wrap">
					<div class="hero-slider-item overflow-hidden">
						<div class="container position-relative">
							<div class="row align-items-center slide-2">
								<div class="text-center">
									<div class="slider-item-content-wrap">
										<div class="item-content2">
											<h3 class="item-title2">
												4th International Conference on Artificial Intelligence & Data Sciences
											</h3>
											<h4 class="item-subtitle2">Theme: "Discovering Technological Advancement in
												Artificial<br>Intelligence and Data Science"</h4>
											<div class="highlight-text2 img-moving-anim4">
												<strong class="big-title"><span class="text">AiDAS&nbsp;2023</span></strong>
											</div>
										</div>
									</div>
								</div>
							</div>
							<div class="dots">
								<img src="../assets/images/dots/dots2.png" alt="Shadow Image"
									class="dots-4 img-moving-anim2">
							</div>
						</div>
						<img src="../assets/images/dots/dots5.png" alt="Shadow Image" class="dots-3 img-moving-anim3">
					</div>
				</div>
			</section>
			<!-- hero sec start -->
		</header>
		<!-- header area end -->


		<!-- info sec start -->
		<div class="info-sec" id="about">
			<div class="container">
				<div class="info-countdown">
					<ul class="counter-box d-flex justify-content-around" data-countdown="2023/9/6">
					</ul>
					<div class="dots img-moving-anim2">
						<img src="../assets/images/dots/dots3.png" alt="Shadow Image">
					</div>
				</div>
				<div class="information-area">
					<div class="row g-4">
						<div class="col-md-6 col-lg-4" data-aos="fade-up" data-aos-duration="1000">
							<div class="calendar">
								<div class="icon"><img src="../assets/images/icon/calendar.svg" alt="Calendar"></div>
								<a href="#" class="calendar-link">6 & 7 September 2023</a>
							</div>
						</div>
						<div class="col-md-6 col-lg-4" data-aos="fade-up" data-aos-duration="800">
							<div class="location">
								<div class="icon"><img src="../assets/images/icon/map-pin.svg" alt="Map"></div>
								<a href="#" class="location-link">Virtual Conference</a>
							</div>
						</div>
						<div class="col-md-6 col-lg-4" data-aos="fade-up" data-aos-duration="600">
							<div class="mail">
								<div class="icon"><img src="../assets/images/icon/mail.svg" alt="Mail"></div>
								<a href="mailto:aidas@uitm.edu.my" class="mail-link">aidas@uitm.edu.my</a>
							</div>
						</div>
					</div>
				</div>
			</div>
		</div>
		<!-- info sec end -->

		<!-- video sec start -->
		<section class="video-sec" data-parallax>
			<div class="container">
				<div class="row align-items-center">
					<div class="col-lg-6">
						<div class="video-wrap">
							<div class="video-image img-moving-anim1">
								<img src="../assets/images/video/video1.jpg" alt="Video Image 1">
							</div>
							<div class="video-play">
								<img src="../assets/images/video/video2.jpg" alt="Video Image 2" data-bs-backdrop="static">
							</div>
							<div class="dots img-moving-anim2">
								<img src="../assets/images/dots/dots6.png" alt="Shadow Image">
							</div>
						</div>
					</div>
					<div class="col-lg-6">
						<div class="video-content-wrap">
							<h2 class="title">
								About Us
							</h2>
							<p class="desc" align="justify"> The 4th International Conference on Artificial Intelligence and
								Data Sciences
								(AiDAS2022) is organized by the Faculty of Computer and Mathematical Sciences, Universiti
								Teknologi MARA, Perak Branch. The co-organizers for AiDAS2022 are Universiti Tunku Abdul
								Rahman
								(UTAR) and Universitas Al-Azhar, Indonesia (UAI).
								AiDAS2022 also is part of the INSPIRED2022 event organized by UiTM Perak.
								This conference is technically co-sponsored by IEEE Computer Society, Malaysia Chapter.
								<br><br>
								The conference aims to form an inclusive meeting place for researchers,
								academics, and practitioners to discuss fundamental and innovative issues related to
								Artificial
								Intelligence and Data Sciences.
								The theme of AiDAS2022 is Artificial Intelligence and Data Sciences: Championing Innovations
								in
								Artificial Intelligence and Data Sciences
								for Sustainable Future ...
							</p>
							<div class="dots img-moving-anim3">
								<img src="../assets/images/dots/dots7.png" alt="Shadow Image">
							</div>
							<button class="custom-btn2 video-btn">Read More&nbsp;&nbsp;></button>
						</div>
					</div>
				</div>
			</div>
		</section>
		<!-- video sec end -->

		<!-- schedule sec start -->
		<section id="important-dates" class="schedule-sec">
			<div class="container mb-4">
				<div class="section-head text-center col-xl-8 m-auto mb-5">
					<span class="label mb-4">Schedules Plan</span>
					<h2 class="title">
						Important Dates
					</h2>
				</div>
				<div class="schedule-content-wrap">
					<div class="d-flex justify-content-center m-auto">
						<ul class="timeline timeline-split">
							<li class="timeline-item">
								<div class="timeline-info">
									<span>March 31, 2023</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Call for paper & reviewer</h5>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
									<span>June 16, 2023</span>
									<!-- <strike></strike>&nbsp;&nbsp;June 19, 2022 -->
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Final deadline for full paper submission</h5>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
									<span>July 16, 2023</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Reviewer deadline</h5>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
									<span>July 19, 2022</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Notification of acceptance</h5>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
									<span>August 20, 2023</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Camera ready</h5>
									<h5>&nbsp;</h5>
									<h5 class="timeline-title">Payment deadline</h5>
								</div>
							</li>
							<li class="timeline-item">
								<div class="timeline-info">
									<span>September 6 &amp; 7, 2023</span>
								</div>
								<div class="timeline-marker"></div>
								<div class="timeline-content">
									<h5 class="timeline-title">Conference date</h5>
								</div>
							</li>
						</ul>
					</div>
					<div class="dots img-moving-anim1">
						<img src="../assets/images/dots/dots2.png" alt="Shadow Image">
					</div>
				</div>
			</div>
			<div class="shape">
				<img src="../assets/images/shape/2.svg" alt="Shape">
			</div>
		</section>
		<!-- schedule sec end -->
		<div class="container">
			<hr>
		</div>

		<!-- cfp sec start -->
		<section id="call-for-paper" class="cfp-sec">
			<div class="container">
				<div class="row align-items-center">
					<div class="col-lg-6 mb-5 mb-lg-0" data-aos="fade-right" data-aos-duration="800">
						<div class="title-area">
							<h2 class="title mb-3">
								Call For Papers<br>Tracks & Reviewer
							</h2>
							<p class="desc mb-5">
								Topic of interest for submission include, but are not limited to:
							</p>
						</div>
					</div>
					<div class="col-lg-6" data-aos="fade-left" data-aos-duration="1000">
						<div class="question-area">
							<div class="accordion" id="accordionExample">
								<div class="accordion-item">
									<h2 class="accordion-header" id="headingTwo">
										<button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
											data-bs-target="#collapseOne" aria-expanded="false" aria-controls="collapseOne">
											Data Science Tracks
										</button>
									</h2>
									<div id="collapseOne" class="accordion-collapse collapse"
										aria-labelledby="headingOne" data-bs-parent="#accordionExample">
										<div class="accordion-body">
											<div class="cfp-grid-container">
												<div class="cfp-grid-item"><span></span> AI and Creativity</div>
												<div class="cfp-grid-item"><span></span> Deep Learning</div>
												<div class="cfp-grid-item"><span></span> Evolutionary Computing</div>
												<div class="cfp-grid-item"><span></span> Fuzzy Systems</div>
												<div class="cfp-grid-item"><span></span> Hybrid Intelligent Systems</div>
												<div class="cfp-grid-item"><span></span> Industrial Applications of AI</div>
												<div class="cfp-grid-item"><span></span> Intelligence and Cybersecurity
												</div>
												<div class="cfp-grid-item"><span></span> Intelligent User Interfaces</div>
												<div class="cfp-grid-item"><span></span> Knowledge Representation and
													Reasoning
												</div>
												<div class="cfp-grid-item"><span></span> Knowledge-Based System</div>
												<div class="cfp-grid-item"><span></span> Ambient Intelligence</div>
												<div class="cfp-grid-item"><span></span> Machine Learning</div>
												<div class="cfp-grid-item"><span></span> Model-Based Reasoning</div>
												<div class="cfp-grid-item"><span></span> Natural Language Processing</div>
												<div class="cfp-grid-item"><span></span> Neural Networks</div>
												<div class="cfp-grid-item"><span></span> Ontologies</div>
												<div class="cfp-grid-item"><span></span> Pattern Recognition</div>
												<div class="cfp-grid-item"><span></span> Planning and Scheduling</div>
												<div class="cfp-grid-item"><span></span> Social Network Analysis</div>
												<div class="cfp-grid-item"><span></span> Soft Computing</div>
												<div class="cfp-grid-item"><span></span> State Space Search</div>
												<div class="cfp-grid-item"><span></span> Bayesian Networks</div>
												<div class="cfp-grid-item"><span></span> Uncertainty in AI</div>
												<div class="cfp-grid-item"><span></span> Vision and Perception</div>
												<div class="cfp-grid-item"><span></span> Visualization</div>
												<div class="cfp-grid-item"><span></span> Case-Based Reasoning</div>
												<div class="cfp-grid-item"><span></span> Cognitive Systems</div>
												<div class="cfp-grid-item"><span></span> Constraint Satisfaction</div>
											</div>
										</div>
									</div>
								</div>
								<div class="accordion-item">
									<h2 class="accordion-header" id="headingTwo">
										<button class="accordion-button collapsed" type="button" data-bs-toggle="collapse"
											data-bs-target="#collapseTwo" aria-expanded="false" aria-controls="collapseTwo">
											Data Science Tracks
										</button>
									</h2>
									<div id="collapseTwo" class="accordion-collapse collapse" aria-labelledby="headingTwo"
										data-bs-parent="#accordionExample">
										<div class="accordion-body">
											<div class="cfp-grid-container">
												<div class="cfp-grid-item"><span></span> Big Data</div>
												<div class="cfp-grid-item"><span></span> Big Data Modeling and Prediction
												</div>
												<div class="cfp-grid-item"><span></span> Data Analytics</div>
												<div class="cfp-grid-item"><span></span> Data Mining, Text Mining</div>
												<div class="cfp-grid-item"><span></span> Data Pre-processing and Sampling
												</div>
												<div class="cfp-grid-item"><span></span> Data Classification and Taxonomy
												</div>
												<div class="cfp-grid-item"><span></span> Data Metrics and Metrology</div>
												<div class="cfp-grid-item"><span></span> Data Representation, Dimensionality
													Reduction, Processing and Proactive Service Layers</div>
												<div class="cfp-grid-item"><span></span> Data Capturing, Management, and
													Scheduling
													Techniques</div>
												<div class="cfp-grid-item"><span></span> Feature Selection and Development
												</div>
												<div class="cfp-grid-item"><span></span> Foundational Theories and Models of
													Data
													Science</div>
												<div class="cfp-grid-item"><span></span> Governance and Big Data</div>
												<div class="cfp-grid-item"><span></span> Large Scale Optimization</div>
												<div class="cfp-grid-item"><span></span> High Performance Computing for Data
													Analytics</div>
												<div class="cfp-grid-item"><span></span> Architecture and Management for
													Data
													Science</div>
												<div class="cfp-grid-item"><span></span> Web and social text mining</div>
												<div class="cfp-grid-item"><span></span> Cloud Computing and Service Data
													Analysis
												</div>
												<div class="cfp-grid-item"><span></span> Efficient Management of Data
													Acquisition
												</div>
												<div class="cfp-grid-item"><span></span> Intelligent Analysis of Large
													Spatial
													Data
												</div>
												<div class="cfp-grid-item"><span></span> Data Science for Real World
													Applications
												</div>
												<div class="cfp-grid-item"><span></span> Challenges In Data Science and
													Advanced
													Analytics</div>
											</div>
										</div>
									</div>
								</div>
								<div class="accordion-item">
									<h2 class="accordion-header" id="headingOne">
										<button class="accordion-button" type="button" data-bs-toggle="collapse"
											data-bs-target="#collapseThree" aria-expanded="true"
											aria-controls="collapseOne">
											Call For Reviewer
										</button>
									</h2>
									<div id="collapseThree" class="accordion-collapse show"
										aria-labelledby="headingOne" data-bs-parent="#accordionExample">
										<div class="accordion-body">
											<p class="desc">We invite experts from related research areas to be part of us
												by participating
												as
												REVIEWERS!</p>
											<p class="desc">
												Those interested may fill in the form at this link: <a target="_blank"
													href="#">CLICK
													HERE</a>
											</p>
										</div>
									</div>
								</div>
							</div>
						</div>
					</div>
				</div>
			</div>
		</section>
		<!-- faq sec end -->
		<div class="container">
			<hr>
		</div>


		<!-- fees sec start -->
		<section id="fees" class="pricing-sec">
			<div class="container">
				<div class="section-head col-xl-8 m-auto text-center px-5">
					<span class="label">Come and Join US</span>
					<h2 class="title mb-5">
						Event Registration Fees
					</h2>
				</div>
				<div class="pricing-cart-wrap">
					<div class="row row-cols-1 row-cols-lg-4 g-4">
						<div class="col col-md-6 col-lg-3">
							<div class="card h-80" data-aos="fade-down" data-aos-easing="ease-out-cubic"
								data-aos-duration="2000">
								<div class="card-body">
									<span class="card-lable"><i class="fa-sharp fa-solid fa-circle"></i>IEEE Members</span>
									<h3 class="price-pacage">RM900 <span class="regular-price">/ $240</span>
									</h3>
									<span>
										Presenter
									</span>
								</div>
							</div>
						</div>
						<div class="col col-md-6 col-lg-3">
							<div class="card h-80" data-aos="fade-up" data-aos-easing="ease-out-cubic"
								data-aos-duration="2000">
								<div class="card-body">
									<span class="card-lable"><i class="fa-sharp fa-solid fa-circle"></i>Non-IEEE
										Members</span>
									<h3 class="price-pacage">RM1050 <span class="regular-price">/ $280</span>
									</h3>
									<span>
										Presenter
									</span>
								</div>
							</div>
						</div>
						<div class="col col-md-6 col-lg-3">
							<div class="card h-80" data-aos="fade-down" data-aos-easing="ease-out-cubic"
								data-aos-duration="2000">
								<div class="card-body">
									<span class="card-lable"><i class="fa-sharp fa-solid fa-circle"></i>IEEE Members</span>
									<h3 class="price-pacage">RM700 <span class="regular-price">/ $200</span>
									</h3>
									<span>
										Student
									</span>
								</div>
							</div>
						</div>
						<div class="col col-md-6 col-lg-3">
							<div class="card h-80" data-aos="fade-up" data-aos-easing="ease-out-cubic"
								data-aos-duration="2000">
								<div class="card-body">
									<span class="card-lable"><i class="fa-sharp fa-solid fa-circle"></i>Non-IEEE
										Members</span>
									<h3 class="price-pacage">RM750 <span class="regular-price">/ $220</span>
									</h3>
									<span>
										Student
									</span>
								</div>
							</div>
						</div>
					</div>
					<div class="dots img-moving-anim1">
						<img src="../assets/images/dots/dots12.png" alt="Shadow Image">
					</div>
				</div>
			</div>
			<div class="shape">
				<img src="../assets/images/shape/5.svg" alt="Shape">
			</div>
		</section>
		<!-- pricing sec end -->
		<div class="container">
			<hr>
		</div>

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
					<span>Copyright © 2022 All Rights Reserved by <a href="#">UiTM Perak</a></span>
				</div>
			</div>
		</footer>
		<!-- footer area end -->

		<!-- Modal -->
		<div class="modal fade popup-modal" id="staticBackdrop" data-bs-backdrop="static" data-bs-keyboard="false"
			tabindex="-1" aria-hidden="true">
			<div class="modal-dialog modal-lg popup-dialogue modal-dialog-centered">
				<div class="modal-content popup-content p-4 bg-white">
					<button type="button" class="btn btn-secondary  ms-auto" data-bs-dismiss="modal"><i
							class="fa-solid fa-xmark"></i></button>

					<div class="modal-body popup-body">
						<iframe width="100%" height="400" src="https://www.youtube.com/embed/1dtzSRlfBDk"
							allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
							allowfullscreen></iframe>
					</div>

				</div>
			</div>
		</div>

		<!-- Button trigger modal -->

		<!-- Modal 2 -->
		<div class="modal  popup-box fade" id="exampleModal" tabindex="-1" aria-hidden="true">
			<div class="modal-dialog popup-box-dialog modal-dialog-centered">
				<div class="modal-content popup-box-content">
					<div class="popup-card" style="width:100%">
						<button type="button" class="btn popup2-btn  ms-auto" data-bs-dismiss="modal"><i
								class="fa-solid fa-xmark"></i></button>
						<img src="../assets/images/popup.png" class="card-img-top" alt="popup-bg">
						<div class="card-body popup-card-body">
							<div class="popup-title-area">
								<p class="popup-sub">October 2, 2023</p>
								<h5 class="card-title popup-title">Virtual sessions. Eventor Live@MAX</h5>
							</div>
							<a href="#" class="btn popup-play" data-bs-toggle="modal" data-bs-target="#staticBackdrop"><i
									class="fa-solid fa-play"></i></a>
						</div>
						<form action="#" class="popup-form">
							<div class="row gy-3 mb-3">
								<div class="col-lg-6">
									<label for="exampleFormControlInput5" class="form-label">Full Name</label>
									<input type="text" class="form-control" id="exampleFormControlInput5"
										placeholder="Your Full Name" required>
								</div>
								<div class="col-lg-6">
									<label for="exampleFormControlInput6" class="form-label">Email</label>
									<input type="email" class="form-control" id="exampleFormControlInput6"
										placeholder="Enter Email" required>
								</div>
								<div class="col-lg-6">
									<label for="exampleFormControlInput7" class="form-label">Phone</label>
									<input type="text" class="form-control" id="exampleFormControlInput7"
										placeholder="Enter Phone" required>
								</div>
								<div class="col-lg-6">
									<label for="exampleFormControlInput8" class="form-label">Conference</label>
									<select class="form-control bg-black-50" name="" id="">
										<option value="">Early Bird ($10)</option>
										<option value="">Regular ($20)</option>
										<option value="">VIP ($50)</option>
									</select>
								</div>
							</div>
							<button class="custom-btn2">Buy Now</button>
						</form>
					</div>
				</div>
			</div>
		</div>
	</div>
</template>
