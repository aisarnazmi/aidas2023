<template>
	<nav class="header-nav navbar fixed-top navbar-expand-lg position-absolute w-100">
		<div class="container header-nav-menu">
			<a class="navbar-brand" href="/">
				<img src="../assets/images/logo/logo.png" width="120" alt="Header Logo" />
			</a>
			<div class="collapse navbar-collapse d-none d-lg-block">
				<ul class="navbar-nav m-auto">
					<li class="">
						<a href="/" class="py-3">
							Homepages
						</a>
					</li>
					<li class="">
						<a href="#about" class="py-3">
							About
						</a>
					</li>
					<li class="">
						<a href="#important-dates" class="py-3">
							Important Dates
						</a>
					</li>
					<li class="">
						<a href="#call-for-paper" class="py-3">
							Call For Paper
						</a>
					</li>
					<li class="">
						<a href="#speakers" class="py-3">
							Speakers
						</a>
					</li>
					<li class="">
						<a href="#fees" class="py-3">
							Fees
						</a>
					</li>
				</ul>
			</div>
			<!-- mobile menu -->
			<div class="mobile-view-header d-block d-lg-none d-flex gap-3 align-items-center">
				<a class="border rounded-1 py-1 px-2 bg-light" data-bs-toggle="offcanvas" href="#offcanvasExample"
					role="button" aria-controls="offcanvasExample">
					<span class="navbar-toggler-icon nav-toggler-icon">
					</span>
				</a>
				<div class="offcanvas offcanvas-start" tabindex="-1" id="offcanvasExample">
					<div class="offcanvas-header">
						<a class="navbar-brand" href="/">
							<img src="../assets/images/logo/logo.png" width="120" alt="Header Logo" />
						</a>
						<button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close">
						</button>
					</div>
					<div class="offcanvas-body">
						<div class="dropdown mt-3">
							<ul class="navbar-nav m-auto">
								<li class="">
									<a href="/" class="py-3">
										Homepages
									</a>
									<div class="drop-down">
										<div class="row drop-down-wrap g-0">
											<div class="col-7">
												<ul class="drop-down-menu">
													<li class="dropdown-item d-flex align-items-center">
														<div class="item-icon">
															<img src="../assets/images/icon/icon.svg" alt="icon Images" />
														</div>
														<a href="#" class="item-content">
															<h5 class="item-title">
																Homepage Conference
															</h5>
															<span class="item-sub">
																Sessions Overview
															</span>
														</a>
													</li>
													<li class="dropdown-item d-flex align-items-center">
														<div class="item-icon">
															<img src="../assets/images/icon/icon2.svg" alt="icon Images" />
														</div>
														<a href="#" class="item-content">
															<h5 class="item-title">
																Homepage Conference
															</h5>
															<span class="item-sub">
																Sessions Overview
															</span>
														</a>
													</li>
													<li class="dropdown-item d-flex align-items-center">
														<div class="item-icon">
															<img src="../assets/images/icon/icon3.svg" alt="icon Images" />
														</div>
														<a href="#" class="item-content">
															<h5 class="item-title">
																Homepage Conference
															</h5>
															<span class="item-sub">
																Sessions Overview
															</span>
														</a>
													</li>
													<li class="dropdown-item d-flex align-items-center">
														<div class="item-icon">
															<img src="../assets/images/icon/icon4.svg" alt="icon Images" />
														</div>
														<a href="#" class="item-content">
															<h5 class="item-title">
																Homepage Conference
															</h5>
															<span class="item-sub">
																Sessions Overview
															</span>
														</a>
													</li>
												</ul>
											</div>
											<div class="col-5">
												<div class="dropdown-thumb position-relative"
													style="background-image: url(src/assets/images/banner/home-conference-dropdown-bg.jpg);">
													<span class="dropdown-sub position-absolute">
														Register Now
													</span>
												</div>
											</div>
										</div>
									</div>
								</li>
								<li class="">
									<a href="#about" class="py-3">
										About
									</a>
								</li>
								<li class="">
									<a href="#important-dates" class="py-3">
										Important Dates
									</a>
								</li>
								<li class="">
									<a href="#call-for-paper" class="py-3">
										Call For Paper
									</a>
								</li>
								<li class="">
									<a href="#speakers" class="py-3">
										Speakers
									</a>
								</li>
								<li class="">
									<a href="#fees" class="py-3">
										Fees
									</a>
								</li>
							</ul>
						</div>
					</div>
				</div>
			</div>
			<!-- end mobile menu -->
		</div>
	</nav>
</template>