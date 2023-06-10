<template>
	<nav class="header-nav navbar fixed-top navbar-expand-lg position-absolute w-100">
		<div class="container header-nav-menu">
			<a class="navbar-brand d-flex gap-3" href="/">
				<img src="../assets/images/logo/logo.png" width="120" alt="Header Logo" />
				<img src="../assets/images/logo/inpired-logo.png" width="120" alt="Header Logo" />
			</a>
			<div class="collapse navbar-collapse d-none d-lg-block">
				<ul class="navbar-nav m-auto">
					<li class="">
						<a href="/" class="py-3">
							Home
						</a>
					</li>
					<li class="">
						<a href="/#about" class="py-3">
							About
						</a>
					</li>
					<li class="">
						<a href="/#important-dates" class="py-3">
							Important Dates
						</a>
					</li>
					<li class="dropdown">
						<a class="py-3">Call For Paper</a>
						<ul class="dropdown-menu">
							<li><a href="/#call-for-paper">Call For Paper + Tracks</a></li>
							<li><a href="paper-submission">Paper Submission</a></li>
						</ul>
					</li>
					<li class="">
						<a href="/#speakers" class="py-3">
							Speakers
						</a>
					</li>
					<li class="">
						<a href="/#fees" class="py-3">
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
						<a class="navbar-brand d-flex gap-3" href="/">
							<img src="../assets/images/logo/logo.png" width="120" alt="Header Logo" />
							<img src="../assets/images/logo/inpired-logo.png" width="120" alt="Header Logo" />
						</a>
						<button type="button" class="btn-close text-reset" data-bs-dismiss="offcanvas" aria-label="Close">
						</button>
					</div>
					<div class="offcanvas-body">
						<div class="dropdown mt-3">
							<ul class="navbar-nav m-auto">
								<li class="">
									<a href="/" class="py-3">
										Home
									</a>
								</li>
								<li class="">
									<a href="/#about" class="py-3">
										About
									</a>
								</li>
								<li class="">
									<a href="/#important-dates" class="py-3">
										Important Dates
									</a>
								</li>
								<li class="dropdown">
									<a class="py-3">Call For Paper</a>
									<ul class="dropdown-menu">
										<li><a href="/#call-for-paper">Call For Paper + Tracks</a></li>
										<li><a href="paper-submission">Paper Submission</a></li>
									</ul>
								</li>
								<li class="">
									<a href="/#speakers" class="py-3">
										Speakers
									</a>
								</li>
								<li class="">
									<a href="/#fees" class="py-3">
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