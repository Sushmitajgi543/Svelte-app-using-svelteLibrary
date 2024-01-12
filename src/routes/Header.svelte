<script>
	import { page } from '$app/stores';
</script>

<header>
	<nav>
		<div class="header__logo">
			<a href="/" aria-label="home"
				><svg id="logo" xmlns="http://www.w3.org/2000/svg" role="img" viewBox="0 0 84 96"
					><title>Logo</title><g transform="translate(-8.000000, -2.000000)"
						><g transform="translate(11.000000, 5.000000)"
							><polygon
								id="Shape"
								stroke="currentColor"
								stroke-width="5"
								stroke-linecap="round"
								stroke-linejoin="round"
								points="39 0 0 22 0 67 39 90 78 68 78 23"
							></polygon></g
						></g
					><text x="10" y="65" fill="currentColor" font-size="50px" font-family="Consolas">Sk</text
					></svg
				></a
			>
		</div>
		<div class="header__menu">
			<svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L1,2 C1.5,3 1.5,3 2,3 L2,0 Z" />
			</svg>
			<ul>
				<li aria-current={$page.url.pathname === '/' ? 'page' : undefined}>
					<a href="/">Home</a>
				</li>
				<li aria-current={$page.url.pathname === '/about' ? 'page' : undefined}>
					<a href="/about">About</a>
				</li>
				<li aria-current={$page.url.pathname === '/experience' ? 'page' : undefined}>
					<a href="/experience">Experience</a>
				</li>
				<li aria-current={$page.url.pathname === '/qualification' ? 'page' : undefined}>
					<a href="/qualification">Qualifications</a>
				</li>
				<li aria-current={$page.url.pathname === '/contact' ? 'page' : undefined}>
					<a href="/contact">contact</a>
				</li>
				<li aria-current={$page.url.pathname === '/resume' ? 'page' : undefined}>
					<a class="resume" href="/resume">resume</a>
				</li>
			</ul>
			<!-- <svg viewBox="0 0 2 3" aria-hidden="true">
				<path d="M0,0 L0,3 C0.5,3 0.5,3 1,2 L2,0 Z" />
			</svg> -->
		</div>
	</nav>
</header>

<style>
	header {
		display: flex;
		justify-content: center;
	}

	nav,
	div {
		display: flex;
		width: 100%;
		justify-content: space-between;
		--background: rgba(255, 255, 255, 0.21);
	}
	.header__menu {
		justify-content: flex-end;
	}

	.header__logo a {
		padding-left: 20px;
		color: var(--color-theme-1);
	}
	svg {
		width: 2em;
		height: 3em;
		display: block;
	}

	path {
		fill: var(--background);
	}

	ul {
		position: relative;
		padding: 0;
		margin: 0;
		height: 3em;
		display: flex;
		justify-content: center;
		align-items: center;
		list-style: none;
		background: var(--background);
		background-size: contain;
		padding-right: 20px;
	}

	li {
		position: relative;
		height: 100%;
	}

	li[aria-current='page']::before {
		--size: 6px;
		content: '';
		width: 0;
		height: 0;
		position: absolute;
		top: 0;
		left: calc(50% - var(--size));
		border: var(--size) solid transparent;
		border-top: var(--size) solid var(--color-theme-1);
	}

	nav a {
		display: flex;
		height: 100%;
		align-items: center;
		padding: 0 1rem;
		color: var(--color-heading);
		font-weight: 500;
		font-size: 1rem;
		text-transform: capitalize;
		letter-spacing: 0.1em;
		text-decoration: none;
		transition: color 0.2s linear;
	}

	a:hover {
		color: var(--color-theme-1);
	}

	.resume{
		border: 1px solid var(--color-theme-1);
		/* height: 70%; */
	}
</style>
