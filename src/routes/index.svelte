<script>
	import '$lib/styles.css';
</script>

<svelte:head>
	<title>NFT Card</title>
</svelte:head>

<main>
	<section>
		<div class="nft-image">
			<img src="image-equilibrium.jpg" alt="equilibrium" />
			<div class="selection">
				<img src="/icon-view.svg" alt="view" />
			</div>
		</div>

		<div class="nft-details">
			<h1>Equilibrium #3429</h1>
			<p>Our Equilibrium collection promotes balance and calm.</p>
		</div>

		<div class="nft-info">
			<div class="nft-price-box">
				<div class="vertical-align">
					<img src="icon-ethereum.svg" alt="ethereum" />
				</div>
				<div class="price">
					<p><span>0.041 ETH</span></p>
				</div>
			</div>

			<div class="nft-time-box">
				<div class="vertical-align">
					<img src="/icon-clock.svg" alt="clock" />
				</div>
				<div class="time">
					<p>3 days left</p>
				</div>
			</div>
		</div>

		<hr />

		<div class="nft-author">
			<div class="nft-author-image">
				<img src="/image-avatar.png" alt="author" />
			</div>
			<p>Creation of <span>Jules Wyvern</span></p>
		</div>
	</section>
</main>

<style>
	/* Outer container */
	main {
		width: 20.4375rem;
		background-color: var(--cardBG);
		box-shadow: 0rem 1.5625rem 3.125rem rgba(0, 0, 0, 0.0952917);
		border-radius: 0.9375rem;
		padding-block: 1.5rem;
	}

	/* inner container */
	section {
		width: 17.375rem;
		margin-inline: auto;
	}

	/* base styles */
	h1 {
		font-family: 'Outfit';
		font-style: normal;
		font-weight: 600;
		font-size: 1.375rem;
		line-height: 1.75rem;
		color: var(--white);
	}

	p {
		font-family: 'Outfit';
		font-style: normal;
		font-weight: 300;
		font-size: 1.125rem;
		line-height: 1.625rem;
		color: var(--softBlue);
	}

	.nft-image img {
		border-radius: 0.5rem;
	}
	.nft-image {
		position: relative;
		height: 17.375rem;
	}
	.selection {
		position: absolute;
		inset: 0;
		opacity: 0;
		display: grid;
		place-content: center;
		border-radius: 0.5rem;
		transition: 0.3s all ease-in-out;
	}

	.selection:hover {
		--cyan: hsla(178, 100%, 50%, var(--opacity));
		--opacity: 0.5;
		background-color: var(--cyan);
		mix-blend-mode: normal;
		opacity: 1;
		cursor: pointer;
	}

	.nft-details h1 {
		margin-top: 1.5rem;
		margin-bottom: 0.75rem;
	}
	.nft-details h1:hover {
		color: var(--cyan);
		cursor: pointer;
	}
	.nft-details p {
		margin-bottom: 1rem;
	}

	/* pricing information box */
	.nft-info,
	.nft-price-box,
	.nft-time-box {
		display: flex;
		align-items: center;
	}

	.vertical-align {
		display: flex;
		margin-right: 0.5rem;
		align-items: center;
	}

	.nft-info {
		justify-content: space-between;
		margin-bottom: 1rem;
	}
	.nft-info p {
		font-size: 0.9375rem;
		line-height: 1.1875rem;
	}

	.price span {
		font-weight: 600;
		color: var(--cyan);
	}

	/* author section */
	hr {
		display: block;
		height: 0.0625rem;
		border: 0;
		border-top: 0.0625rem solid var(--line);
		margin: 1em 0;
		padding: 0;
		margin-bottom: 1rem;
	}

	.nft-author {
		display: flex;
		align-items: center;
	}

	.nft-author-image {
		width: 2.0625rem;
		height: 2.0625rem;
		border: 0.0625rem solid var(--white);
		border-radius: 50%;
		margin-right: 1rem;
	}
	.nft-author p {
		font-family: 'Outfit';
		font-style: normal;
		font-weight: 400;
		font-size: 0.9375rem;
		line-height: 1.1875rem;
	}
	.nft-author p span {
		color: var(--white);
	}

	.nft-author p span:hover {
		color: var(--cyan);
		cursor: pointer;
	}
	@media screen and (min-width: 48rem) {
		main {
			width: 21.875rem;
		}
		section {
			width: 18.875rem;
		}
		.nft-details h1 {
			margin-bottom: 1rem;
		}
		.nft-image {
			height: 18.875rem;
		}

		.nft-info,
		.nft-details p {
			margin-bottom: 1.5rem;
		}
		.nft-info p,
		.nft-author p {
			font-size: 1rem;
			line-height: 1.25rem;
		}
	}
</style>
