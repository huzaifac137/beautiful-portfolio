<script>
	import { intro } from '../InfoData/intro';

</script>

<div class="intro">
	<div class="name">
		<h3>Hey, Its <span> {intro.name}</span></h3>
		<h2>{intro.role}</h2>
		<p>{intro.description}</p>
		<a href="./Huzaifa_CV.pdf" download="Huzaifa's CV"   >Download CV</a>
	</div>

	<div class="imageContainer">
		<img src={intro.user_dp} alt="display profile pic" />
	</div>
</div>

<style>
	.intro {
		display: flex;
		align-items: center;
		justify-content: space-around;
		color: var(--secondary-color);
		margin-top: 100px;
		
	}

	.name {
		display: flex;
		flex-direction: column;
		align-items: flex-start;
		gap: 20px;
		animation: scale 1s ease-out 0s;
		width: 40%;
	}

	.name h3 span {
		margin-left: 5px;
		color: var(--tertiary-color);
		font-size: 27px;
	}

	.imageContainer {
		display: flex;
		align-items: center;
		justify-content: center;

		animation: scale 1s ease-out 0s;
	}

	.imageContainer img {
		width: 260px;
		height: 260px;
		border-radius: 50%;
	}

	a {
		background-color: var(--secondary-color);
		color: #fff;
		padding-left: 10px;
		padding-right: 10px;
		padding-top: 5px;
		padding-bottom: 5px;
		border: none;
		border-radius: 7px;
		text-decoration: none;
	}


	@media (max-width: 650px) {
		.intro {
			flex-direction: column;
		}

		.name {
			width: 80%;
		}

		.imageContainer {
			margin-top: 50px;
		}
	}

	@keyframes scale {
		from {
			transform: scale(0);
		}

		to {
			transform: scale(1);
		}
	}
</style>
