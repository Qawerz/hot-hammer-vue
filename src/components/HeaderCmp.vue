<template>
	<header class="header">
		<!-- <img
			src="../../public/img/Zj8_PniLP1ZNMNJYGlvtv0MjFF28VtyQ5F-1gr6Rk29GSepmOlgxbveVgmwaqIjmeM1p4ba3.jpg"
		/> -->
		<div class="container">
			<h1>Идеи обретают форму</h1>
			<hr />
			<h2>Мастерская художественной ковки "Живая Сталь".</h2>
			<h2>Поможет вам воплотить вашу мечту в метал		ле</h2>

			<a href="#contact">Получить изделие</a>
		</div>
	</header>
</template>

<style lang="scss" scoped>
img {
	filter: brightness(50%);
	height: 100%;
	width: 100%;
}

header {
	div {
		margin: 0;
		display: flex;
		flex-direction: column;
		align-items: center;
		position: absolute;
		border-radius: 2rem;
		top: 50%;
		left: 50%;
		transform: translate(-50%, -50%);
		// background-color: #00000077;
		padding: 2rem;
		h1,
		h2 {
			text-align: center;
			color: #fff;
			padding: 0;
			margin: 0;
		}

		h1{
			font-family: 'Playfair Display';
			font-style: normal;
			font-weight: 700;
			font-size: 64px;
			line-height: 85px;
			text-align: center;
		}

		h2{
			font-family: 'Verdana';
			font-style: normal;
			font-weight: 400;
			font-size: 24px;
			line-height: 2;
			display: flex;
			align-items: center;
			text-align: center;
		}

		hr {
			width: 100%;
			margin-top: 1rem;
			margin-bottom: 3rem;
		}

		a{
			color:#fff;
			margin: 3.5rem;
			border: 1px solid #fff;
			padding: 1rem;
			border-radius: 20px 0px;

			text-decoration: none;

			font-family: 'Playfair Display SC';
			font-style: normal;
			font-weight: 400;
			font-size: 28px;
			line-height: 37px;
			text-transform: uppercase;
		}
	}
}

@media screen and (max-width: 799px) {
	img {
		height: 100%;
		width: 200%;
		transform: translate(-35%, 0%);
		filter: brightness(30%);
	}

	header div {
		font-size: 0.55rem;
		top: 40%;
		left: 50%;
		transform: translate(-50%, -50%);

		
	}
}
</style>
