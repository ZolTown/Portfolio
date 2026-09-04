<script>
	import headImage from '$lib/assets/HeadZZ.svg';

	const currentYear = new Date().getFullYear();
	const techMatrix = [
		{ cat: 'Languages', tech: 'Elixir, Erlang' },
		{ cat: 'Frameworks', tech: 'Phoenix, LiveView' },
		{ cat: 'Data/Queues', tech: 'GraphQL, PostgreSQL, SQLite3, Riak' },
		{ cat: 'Infra/Security', tech: 'Docker, Rancher, ArgoCD, K9s' }
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
					<p class="eyebrow">// Banking Infrastructure</p>
					<h1 class="site-title">Zoltán Madarász</h1>
				</div>
				<div class="header-meta">
					<p>LOC: Budapest, HU</p>
					<p>AVAILABILITY: Q3 2026</p>
					<p class="font-bold text-paper-ink">✓ SECURE CONNECTION ESTABLISHED</p>
				</div>
			</div>
			<div class="site-intro">
				<p class="m-0">
					Backend engineer specializing in fault-tolerant, high-throughput microservices, and
					airtight financial data security.<br />
				</p>
				<p class=" mt-5 mb-0 text-black">
					Building <span class="text-paper-accent">invisible </span> systems that never fail.
				</p>
			</div>
		<img src={headImage} alt="Zoltán" class="inline-block mr-1 h-60 w-90" />
		<!--TODO: line width, fill-color, stroke color-->

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
				<!-- Description -->
				<p class="description">
					Architected and executed a zero-downtime message queue that ingresses 10k messages per
					second of market data servicing a financial ranking service.<br />
					The system is designed to be horizontally scalable (using a HashRing to distribute load), fault-tolerant,
					and resilient to network partitions, ensuring uninterrupted service even under high load conditions.<br
					/>
					The main challenge was determining the acceptable delay time for buffering messages not to overload
					the downstream services, while also ensuring that the system could recover gracefully from any
					failures without data loss.<br />
					It leverages a combination of Elixir, Phoenix, and Riak to ensure high availability and low
					latency, while maintaining strict data integrity and security protocols.
				</p>
				<!-- System Metrics Panel -->
				<div class="metrics-grid">
					<div class="metric">
						<span class="block text-[10px] text-paper-accent uppercase">Throughput</span>
						<span class="text-lg font-bold">10,000 txn/sec;</span>
					</div>
					<div class="metric">
						<span class="block text-[10px] text-paper-accent uppercase">API's</span>
						<span class="text-lg font-bold"> REST, GraphQL;</span>
					</div>
					<div class="metric">
						<span class="block text-[10px] text-paper-accent uppercase">Lines of Code</span>
						<span class="text-lg font-bold">3604;</span>
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
					<!-- Description -->
					<p class="description">
						Developed a fault-tolerant real-time market data distribution service on the OTP/BEAM
						platform, delivering live prices and charts to 60,000+ concurrent GraphQL subscriptions
						with &lt; 2 ms processing latency and sustained throughput of ~40,000 messages/sec.<br
						/>
						Designed and implemented entitlement logic to seamlessly provide either real-time or 5-minute
						delayed market data based on user permissions.<br />
						Despite handling high message volumes and supporting publish rates of up to 66,000 messages/sec,
						the service maintained an efficient runtime footprint of approximately 0.5 GB RAM per node,
						enabling cost-effective horizontal scaling without compromising latency—an essential requirement
						in financial market data delivery.<br />
						Implemented a comprehensive observability stack using Prometheus, Grafana, and Thanos, significantly
						improving production visibility and reducing debugging and incident resolution time.<br
						/>
						Regularly participated in the on-call rotation, troubleshooting production incidents and ensuring
						the reliability of latency-sensitive services.
					</p>
					<!-- System Metrics Panel -->
					<div class="metrics-grid">
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Latency</span>
							<span class="text-lg font-bold">&lt; 2 ms;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Traffic</span>
							<span class="text-lg font-bold">60k+ Subscriptions;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Runtime Efficiency</span>
							<span class="text-lg font-bold">0.5 GB RAM / Node;</span>
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
					<!-- Description -->
					<p class="description">
						Developed two internal operational tools using Phoenix LiveView, delivering responsive,
						user-friendly interfaces that improved the efficiency of L3 support engineers.<br />
						Worked across the full application stack, translating operational workflows and user requirements
						into integrated backend and frontend solutions without relying on a separate SPA architecture.<br
						/>
						Integrated the applications into the company's existing authentication infrastructure using
						OpenID Connect (OIDC) with OAuth 2.0 endpoints, collaborating with DevOps to configure role-based
						access control and user permissions.<br />
						Built the UI with Tailwind CSS, DaisyUI, and custom reusable components, while wiring GraphQL
						queries and mutations to user interactions to provide a seamless, real-time user experience.
					</p>
					<!-- System Metrics Panel -->
					<div class="metrics-grid">
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Platform</span>
							<span class="text-lg font-bold">Internal Operations Platform;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Full-Stack Phoenix</span>
							<span class="text-lg font-bold">Custom UI Components and State Management;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Role-Based Access</span>
							<span class="text-lg font-bold">OIDC / OAuth2;</span>
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
					<!-- Description -->
					<p class="description">
						Responsible for maintaining and evolving a large-scale federated GraphQL schema spanning
						32 subservices and over 20,000 lines of schema definitions.<br />
						Ensured long-term maintainability and consistency of API contracts across multiple teams by
						reviewing changes, discussing design decisions, and promoting sustainable schema evolution
						practices.<br />
						Coordinated with development teams to align changes across services and ensure a coherent,
						stable release package within a structured 3-week release cycle.<br />
						Helped prevent integration issues by maintaining clear communication between teams and ensuring
						that API changes remained compatible, understandable, and maintainable over time.
					</p>
					<!-- System Metrics Panel -->
					<div class="metrics-grid">
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase"
								>Cross-Team Coordination</span
							>
							<span class="font-italic text-lg font-bold">20k+ LOC Schema;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">API Governance</span>
							<span class="font-italic text-lg font-bold">Federated GraphQL;</span>
						</div>
						<div class="metric">
							<span class="block text-[10px] text-paper-accent uppercase">Release Integration</span>
							<span class="font-italic text-lg font-bold">32 Services;</span>
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
			<p>© {currentYear} — Encrypted & Published via Clean Code Principles.</p>
			<div class="footer-links">
				<a href="https://github.com/ZolTown" class="link">[GitHub]</a>
				<a href="https://linkedin.com/in/zoltán-madarász-79513b180" class="link">[LinkedIn]</a>
				<a href="mailto:zoltan.madarasz1@gmail.com" class="link">[Email]</a>
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
		@apply mt-8 max-w-2xl font-serif text-lg text-paper-muted md:text-xl;
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
		@apply font-serif text-2xl font-normal;
	}
	:global(.card-subtitle) {
		@apply mt-1 text-xs text-paper-accent;
	}
	:global(.card-desc) {
		@apply max-w-3xl font-[Roboto] text-sm leading-relaxed text-paper-muted;
	}
	:global(.description) {
		@apply max-w-3xl font-[Roboto] text-sm leading-relaxed text-paper-muted;
	}
	:global(.metrics-grid) {
		@apply grid grid-cols-1 gap-4 pt-2 sm:grid-cols-3;
	}
	:global(.metric) {
		@apply border-l-2 border-paper-ink pl-3 font-[Roboto];
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
