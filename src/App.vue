<template>
	<div id="app">
		<header>
			<nav class="nav-extended hide-on-small-only">
				<div class="nav-wrapper">
					<router-link to='/' class="brand-logo" title="Setup">Setup</router-link>
					<ul class="right user-login">
						<li><router-link to="/">Olá, Augusto <i class="material-icons right">arrow_drop_down</i></router-link></li>
					</ul>
					<div class="nav-content">
						<ul class="tabs">
							<li class="tab">
								<router-link to="/members" title="My Team">My Team </router-link>
							</li>
							<li class="tab">
								<router-link to="/offices" title="Offices">Offices</router-link>
							</li>
						</ul>
					</div>
				</div>
			</nav>
		</header>
		<aside>
			<ul id="slide-out" class="side-nav fixed">
				<span class="logo-icon">
					<i class="material-icons">person_pin</i>
				</span>
				<li>
					<i class="material-icons">toc</i>
					<span>Tasks</span>
				</li>
				<li>
					<i class="material-icons">view_carousel</i>
					<span>Contents</span>
				</li>
				<li>
					<i class="material-icons">settings</i>
					<span>Setup</span>
				</li>
			</ul>
		</aside>
		<main class="content">
			<div class="actions-mobile center-align hide-on-med-and-up">
				<router-link to="/members" class="btn btn-home-mobile" title="My Team">My Team </router-link>
				<router-link to="/offices" class="btn btn-offices-mobile" title="Offices">Offices</router-link>
			</div>
			<router-view></router-view>
		</main>
	</div>
</template>

<script>
import Members from './components/Members.vue'

export default {
	name: 'app',
	components: {
		Members
	},
	data () {
		return {

		}
	}
}
</script>

<style>
/* Geral style */
body {
	background-color: rgba(242, 246, 247, 0.80);
}

header, main, footer {
	padding-left: 100px;
}

.back-btn {
	color: #8a8a8a;
}

/* Header style */
nav {
	background-color: #eef2f3;
	box-shadow: none;
}

nav .brand-logo {
	font-weight: 300;
	font-size: 1.6em;
	margin-left: 50px;
	color: #659db8;
}

nav ul a {
	color: #a8a8a8 !important;
}
.nav-content {
	margin-left: 50px;
}

.tabs {
	background-color: #eef2f3;
}

.tabs .tab a:hover {
	background-color: #E6EAEB;
}

.tabs .tab a.active {
	background-color: rgba(242, 246, 247, 0.80);
	color: #86c06e !important;
}

.tabs .indicator {
	bottom: 46px;
	background-color: #86c06e;
}

/* Aside style */
.side-nav {
	width: 100px;
	background-color: #feffff;
}

.side-nav .logo-icon .material-icons {
	display: block;
	margin: 23px 0 45px 0;
	font-size: 3.2em;
	text-align: center;
	color: #a8a8a8;
}

.side-nav li {
	margin-bottom: 25px;
	padding-top: 10px;
	text-align: center;
	text-transform: uppercase;
	color: #a8a8a8;
	font-weight: 400;
    font-size: 0.8em;
	cursor: pointer;
}

.side-nav li:hover {
	background-color: #f4f4f4;
}

.side-nav li i {
	text-align: center;
	display: block;
	color: #a8a8a8;
}

.content {
	margin: 0 30px 0 30px;
}

.actions-mobile .btn {
	margin: 10px 0 20px 0;
	background-color: #659db8;
}

.actions-mobile .btn:hover {
    background-color: #5989a0;
}

/* Media Query */
@media only screen and (max-width: 990px) {
	header, main, footer {
		padding-left: 0px;
	}
}

@media only screen and (max-width: 1083px) {
	.change-view span {
		display: none;
	}
}
</style>
