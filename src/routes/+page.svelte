<script>
	import headImage from '$lib/assets/HeadZZ.svg';

	const currentYear = new Date().getFullYear();
	const techMatrix = [
		{ cat: 'Languages', tech: 'Elixir, Erlang' },
		{ cat: 'Frameworks', tech: 'Phoenix, LiveView' },
		{ cat: 'Data/Queues', tech: 'GraphQL, PostgreSQL, Riak' },
		{ cat: 'Infra/Security', tech: 'Docker, Rancher, K9s' }
	];
</script>

<div class="page">
	<!-- Subtle Grain Overlay Effect -->
	<div class="grain-overlay"></div>
	<!-- Main Container -->
	<div class="container">
		<!-- Header Section -->
		<header class="site-header">
			<div class="header-row">
				<div>
					<p class="eyebrow">// Distributed Systems Engineer</p>
					<h1 class="site-title">Zoltán Madarász</h1>
				</div>
				<div class="header-meta">
					<p>LOC: Budapest, HU</p>
					<p>AVAILABILITY: Q3 2026</p>
					<p class="font-bold text-paper-ink">✓ DATA INTEGRITY FIRST</p>
				</div>
			</div>
			<div class="header-body">
				<div class="site-intro">
					<p class="m-0 text-black">
						Distributed Systems Engineer specializing in fault-tolerant, high-throughput services
						and correct, dependable financial data.<br />
					</p>
					<p class=" mt-5 mb-0 text-black">
						Building <span class="text-paper-accent">invisible </span> systems that never fail.
					</p>
				</div>
				<div class="portrait-frame">
					<img src={headImage} alt="Zoltán" class="portrait" />
				</div>
			</div>
		</header>

		<!-- Tech Stack Matrix (Grid Ledger) -->
		<section class="matrix-section">
			<h2 class="section-title">// Core Architecture Matrix</h2>
			<div class="matrix-grid">
				{#each techMatrix as item (item.cat)}
					<div class="matrix-item">
						<span class="matrix-item-label">{item.cat}</span>
						<p class="matrix-item-value">{item.tech}</p>
					</div>
				{/each}
			</div>
		</section>
		<!-- Project Section (Ledger Item) -->
		<section class="projects">
			<h2 class="section-title">// Production Implementations</h2>
			<div class="card">
				<!-- Project Header -->
				<div
					class="flex items-baseline justify-between border-b border-dashed border-paper-border pb-4"
				>
					<div>
						<h3 class="font-serif text-2xl font-normal">
							High-Throughput Market Data Message Queue
						</h3>
						<p class="mt-1 text-xs text-paper-accent">
							Real-time data ingestion and processing for financial market information
						</p>
					</div>
					<span class="font-serif text-xs text-paper-muted italic">01 // Fully Owned Project</span>
				</div>
				<p class="description">
					Designed and implemented a zero-downtime message queue for market data consumed by a financial
					ranking service. The system distributes load with a HashRing, buffers traffic to protect downstream
					services, and recovers from network partitions without losing messages.
				</p>
				<div class="metrics-grid project-facts">
					<div class="metric">
						<span class="metric-label">Scale</span>
						<span class="metric-value">10,000 messages/sec</span>
					</div>
					<div class="metric">
						<span class="metric-label">Architecture</span>
						<span class="metric-value">HashRing distribution</span>
					</div>
					<div class="metric">
						<span class="metric-label">Reliability</span>
						<span class="metric-value">Recovery without data loss</span>
					</div>
				</div>
				<!-- Technical Metadata Footer -->
				<div class="meta-tags">
					<span>[Elixir]</span> <span>[Phoenix]</span> <span>[Riak]</span>
					<span>[Kubernetes]</span>
				</div>
			</div>
			<div>
				<div class="card">
					<!-- Project Header -->
					<div
						class="flex items-baseline justify-between border-b border-dashed border-paper-border pb-4"
					>
						<div>
							<h3 class="font-serif text-2xl font-normal">
								GraphQL Subscription Service for Real-Time Market Data
							</h3>
							<p class="mt-1 text-xs text-paper-accent">
								High Demand Real-Time Data Delivery for End Users via WebSocket Subscriptions
							</p>
						</div>
						<span class="font-serif text-xs text-paper-muted italic"
							>02 // Scalability Case Study</span
						>
					</div>
					<p class="description">
						Built a fault-tolerant OTP/BEAM service that delivers live prices and charts through GraphQL
						subscriptions. Implemented entitlement logic for real-time and five-minute delayed data, then
						added Prometheus, Grafana, and Thanos to support production observability and on-call diagnosis.
					</p>
					<div class="metrics-grid project-facts">
						<div class="metric">
							<span class="metric-label">Traffic</span>
							<span class="metric-value">60,000+ subscriptions</span>
						</div>
						<div class="metric">
							<span class="metric-label">Latency</span>
							<span class="metric-value">&lt; 2 ms processing</span>
						</div>
						<div class="metric">
							<span class="metric-label">Operations</span>
							<span class="metric-value">Prometheus, Grafana, Thanos</span>
						</div>
					</div>
					<!-- Technical Metadata Footer -->
					<div class="meta-tags">
						<span>[Elixir]</span> <span>[Phoenix]</span> <span>[GraphQL]</span>
						<span>[Prometheus]</span> <span>[Grafana]</span> <span>[Thanos]</span>
					</div>
				</div>
			</div>
			<div>
				<div class="card">
					<!-- Project Header -->
					<div
						class="flex items-baseline justify-between border-b border-dashed border-paper-border pb-4"
					>
						<div>
							<h3 class="font-serif text-2xl font-normal">Internal Operations Platform</h3>
							<p class="mt-1 text-xs text-paper-accent">
								Operational Tools for L3 Support Engineers to Manage and Monitor System Health
							</p>
						</div>
						<span class="font-serif text-xs text-paper-muted italic"
							>03 // Merging Frontend and Backend</span
						>
					</div>
					<p class="description">
						Built two internal Phoenix LiveView tools for L3 support engineers to manage system health and
						operational workflows. Worked across the stack, connecting GraphQL queries and mutations to
						reusable UI components while integrating the applications with OIDC, OAuth 2.0, and role-based
						access controls.
					</p>
					<div class="metrics-grid project-facts">
						<div class="metric">
							<span class="metric-label">Stack</span>
							<span class="metric-value">Phoenix LiveView, GraphQL, Tailwind</span>
						</div>
						<div class="metric">
							<span class="metric-label">Access</span>
							<span class="metric-value">OIDC, OAuth 2.0, RBAC</span>
						</div>
						<div class="metric">
							<span class="metric-label">Ownership</span>
							<span class="metric-value">Full-stack implementation</span>
						</div>
					</div>
					<!-- Technical Metadata Footer -->
					<div class="meta-tags">
						<span>[Elixir]</span> <span>[Phoenix LiveView]</span> <span>[GraphQL]</span>
						<span>[Ecto]</span>
						<span>[Tailwind CSS]</span> <span>[DaisyUI]</span>
					</div>
				</div>
			</div>
			<div>
				<div class="card">
					<!-- Project Header -->
					<div
						class="flex items-baseline justify-between border-b border-dashed border-paper-border pb-4"
					>
						<div>
							<h3 class="font-serif text-2xl font-normal">Federated GraphQL Schema Maintenance</h3>
							<p class="mt-1 text-xs text-paper-accent">
								Managing and evolving a large-scale federated GraphQL schema across multiple
								services
							</p>
						</div>
						<span class="font-serif text-xs text-paper-muted italic"
							>04 // Cross-Team Collaboration</span
						>
					</div>
					<p class="description">
						Maintained and evolved a federated GraphQL schema spanning 32 subservices and more than 20,000
						lines of schema definitions. Reviewed API changes, coordinated cross-team dependencies, and
						helped produce compatible release packages on a structured three-week cycle.
					</p>
					<div class="metrics-grid project-facts">
						<div class="metric">
							<span class="metric-label">Scope</span>
							<span class="metric-value">32 subservices</span>
						</div>
						<div class="metric">
							<span class="metric-label">Governance</span>
							<span class="metric-value">20,000+ lines of schema</span>
						</div>
						<div class="metric">
							<span class="metric-label">Delivery</span>
							<span class="metric-value">Three-week release cycle</span>
						</div>
					</div>
					<!-- Technical Metadata Footer -->
					<div class="meta-tags">
						<span>[Code Review]</span> <span>[Release Management]</span> <span>[GraphQL]</span>
					</div>
				</div>
			</div>
		</section>
		<!-- Minimal Footer -->
		<footer class="site-footer">
			<p>© {currentYear} Zoltán Madarász — Built with SvelteKit and Tailwind CSS.</p>
			<div class="footer-links">
				<a href="https://github.com/ZolTown" class="link">[GitHub]</a>
				<a href="https://linkedin.com/in/zoltán-madarász-79513b180" class="link">[LinkedIn]</a>
				<a
					href="https://mail.google.com/mail/?view=cm&fs=1&to=zoltan.madarasz1@gmail.com"
					class="link"
					target="_blank"
					rel="noreferrer"
					>[Email]</a
				>
			</div>
		</footer>
	</div>
</div>

<style>
	@reference "./layout.css";

	:global(.page) {
		@apply relative min-h-screen overflow-hidden bg-paper-bg p-6 font-[Roboto_Mono] text-paper-ink selection:bg-paper-border md:p-16;
	}
	:global(.grain-overlay) {
		@apply pointer-events-none absolute inset-0 bg-[url('data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSI0IiBoZWlnaHQ9IjQiPgo8cmVjdCB3aWR0aD0iMSIgaGVpZHRoPSIxIiBmaWxsPSIjMDAwIi8+Cjwvc3ZnPg==')] bg-repeat opacity-[0.015];
	}
	:global(.container) {
		@apply relative z-10 mx-auto max-w-4xl space-y-8;
	}
	:global(.site-header) {
		@apply border-b border-paper-border pb-0;
	}
	:global(.header-row) {
		@apply flex flex-col items-start justify-between gap-4 md:flex-row md:items-end;
	}
	:global(.header-body) {
		@apply mt-2 grid grid-cols-1 gap-5 pb-4 md:grid-cols-[minmax(0,1fr)_14rem] md:gap-8;
	}
	:global(.eyebrow) {
		@apply text-xs tracking-widest text-paper-accent uppercase;
	}
	:global(.site-title) {
		@apply line-clamp-1 pt-4 font-[EB_Garamond] text-5xl font-normal tracking-tight md:text-6xl;
		line-height: 48px;
	}
	:global(.header-meta) {
		@apply space-y-1 text-left text-xs text-paper-muted md:text-right;
	}
	:global(.site-intro) {
		@apply mt-0 max-w-2xl self-center font-serif text-lg text-paper-muted md:text-xl;
	}

	:global(.portrait-frame) {
		@apply my-0 flex h-56 items-center justify-center overflow-hidden border-l border-dashed border-paper-border pl-5 md:h-64;
	}
	:global(.portrait) {
		@apply h-full w-full object-contain object-center;
		transform: scaleX(-1) scale(1.06);
	}
	:global(.section-title) {
		@apply text-xs font-bold tracking-widest text-paper-accent uppercase;
	}
	:global(.matrix-grid) {
		@apply mt-4 grid grid-cols-2 border-t border-l border-paper-border md:grid-cols-4;
	}
	:global(.matrix-item) {
		@apply space-y-1 border-r border-b border-paper-border p-4;
	}
	:global(.matrix-item-label) {
		@apply text-[10px] text-paper-accent uppercase;
	}
	:global(.matrix-item-value) {
		@apply text-sm font-medium;
	}
	:global(.projects) {
		@apply space-y-6;
	}
	:global(.card) {
		@apply space-y-6 border border-paper-border bg-white/40 p-6 pb-8 backdrop-blur-[1px];
	}
	:global(.card-header) {
		@apply flex items-baseline justify-between border-b border-dashed border-paper-border pb-4;
	}
	:global(.card-title) {
		@apply font-serif text-xl leading-tight font-normal md:text-2xl;
	}
	:global(.card-subtitle) {
		@apply mt-2 text-[11px] leading-relaxed text-paper-accent;
	}
	:global(.card-desc) {
		@apply max-w-3xl font-[Roboto] text-sm leading-7 text-paper-muted;
	}
	:global(.description) {
		@apply max-w-3xl font-[Roboto] text-sm leading-7 text-paper-muted;
	}
	:global(.metrics-grid) {
		@apply grid grid-cols-1 gap-3 pt-1 sm:grid-cols-3;
	}
	:global(.project-facts) {
		@apply gap-4 border-t border-dashed border-paper-border pt-4;
	}
	:global(.metric) {
		@apply border-l border-paper-border pl-3 font-[Roboto];
	}
	:global(.metric-label) {
		@apply block text-[9px] tracking-widest text-paper-accent uppercase;
	}
	:global(.metric-value) {
		@apply mt-0.5 block text-xs leading-4 font-medium text-paper-ink;
	}
	:global(.meta-tags) {
		@apply flex flex-wrap gap-2 pt-2 text-[11px] text-paper-muted;
	}
	:global(.site-footer) {
		@apply flex flex-col justify-between gap-4 border-t border-paper-border pt-8 text-xs text-paper-accent sm:flex-row;
	}
	:global(.footer-links) {
		@apply flex gap-4;
	}
	:global(.link) {
		@apply underline underline-offset-4 transition-colors hover:text-paper-ink;
	}
</style>
