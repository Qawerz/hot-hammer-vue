<template>
    <nav class="sticky navbar">
        <div class="brand display__logo">
			<a href="#top" class="nav__link">
				<span class="logo">Художественная ковка</span></a
			>
		</div>
        <slot></slot>
    </nav>
</template>

<style lang="scss" scoped>
:root {
	--primary: rgba(37, 37, 37, 1);
	--secondary: rgba(252, 41, 74, 1);
	--shades: rgba(238, 238, 238, 1);
}

.navbar {
	padding-top: 0.5em;
	padding-bottom: 0.5em;
	background-color: var(--primary);
	-webkit-box-shadow: 0 14px 14px -14px rgba(0, 0, 0, 0.75);
	-moz-box-shadow: 0 14px 14px -14px rgba(0, 0, 0, 0.75);
	box-shadow: 0 14px 14px -14px rgba(0, 0, 0, 0.75);
}

.nav {
	&__items {
		margin: 0;
		padding: 0;
		list-style: none;
		margin-top: 5px;
	}

	&__link {
		color: var(--shades);
		text-decoration: none;
	}
}

.brand {
	margin: 0;
	font-size: 1.45em;

	a {
		padding: 10px 15px;
		text-align: center;
		display: block;
	}
}

.logo {
	display: inline-block;
	padding-top: 0.3125rem;
	padding-bottom: 0.3125rem;
	margin-right: 1rem;
	line-height: inherit;
}

.brand .nav__link,
.nav__items .nav__link {
	padding: 10px 15px;
	text-align: center;
	display: block;
}

.nav__items .nav__link {
	color: var(--shades);
	font-size: 0.99rem;
}

.nav__items .nav__link:hover {
	color: var(--secondary);
}

.nav__item:nth-child(1) .nav__link::before {
	content: "1. ";
}

.nav__item:nth-child(2) .nav__link::before {
	content: "2. ";
}

.nav__item:nth-child(3) .nav__link::before {
	content: "3. ";
}

.nav__item:nth-child(4) .nav__link::before {
	content: "4. ";
}

@media (min-width: 800px) {
	.navbar,
	.nav__items {
		display: flex;
	}

	.navbar {
		flex-direction: column;
		align-items: center;
	}

	.navbar {
		flex-direction: row;
		justify-content: space-between;
	}
}

@media screen and (max-width: 799px) {
	.nav {
		position: fixed;
		top: 0;
		left: 0;
		height: 100%;
		width: 100%;
		z-index: -1;
		background-color: var(--primary);
		opacity: 0;
		transition: all 0.2s ease;
	}

	.nav .nav__items {
		position: absolute;
		top: 50%;
		transform: translateY(-50%);
		width: 100%;
		padding-inline-start: 0;
	}

	.nav .nav__items .nav__item {
		display: block;
		float: none;
		width: 100%;
		text-align: right;
		margin-bottom: 10px;
	}

	.nav .nav__items .nav__item:nth-child(1) a {
		transition-delay: 0.2s;
	}

	.nav .nav__items .nav__item:nth-child(2) a {
		transition-delay: 0.3s;
	}

	.nav .nav__items .nav__item:nth-child(3) a {
		transition-delay: 0.4s;
	}

	.nav .nav__items .nav__item:nth-child(4) a {
		transition-delay: 0.5s;
	}

	.nav .nav__items .nav__item:not(:first-child) {
		margin-left: 0;
	}

	.nav .nav__items .nav__item .nav__link {
		padding: 10px 25px;
		opacity: 0;
		color: var(--shades);
		font-size: 24px;
		font-weight: 600;
		transform: translateY(-20px);
		transition: all 0.2s ease;
	}

	.nav .nav__items .nav__item .nav__link:hover {
		color: var(--secondary);
	}

	.nav__open {
		position: absolute;
		right: 10px;
		top: 16px;
		display: block;
		width: 48px;
		height: 48px;
		cursor: pointer;
		z-index: 9999;
		border-radius: 50%;
	}

	.nav__open i {
		display: block;
		width: 20px;
		height: 2px;
		background-color: var(--secondary);
		border-radius: 2px;
		margin-left: 14px;
	}

	.nav__open i:nth-child(1) {
		margin-top: 16px;
	}

	.nav__open i:nth-child(2) {
		margin-top: 4px;
		opacity: 1;
	}

	.nav__open i:nth-child(3) {
		margin-top: 4px;
	}
}

#nav:checked + .nav__open {
	transform: rotate(45deg);
}

#nav:checked + .nav__open i {
	background-color: var(--shades);
	transition: transform 0.2s ease;
}

#nav:checked + .nav__open i:nth-child(1) {
	transform: translateY(6px) rotate(180deg);
}

#nav:checked + .nav__open i:nth-child(2) {
	opacity: 0;
}

#nav:checked ~ .nav__item a {
	display: block !important;
}

#nav:checked + .nav__open i:nth-child(3) {
	transform: translateY(-6px) rotate(90deg);
}

#nav:checked ~ .nav {
	z-index: 9990;
	opacity: 1;
}

#nav:checked ~ .nav ul li a {
	opacity: 1;
	transform: translateY(0);
}

</style>