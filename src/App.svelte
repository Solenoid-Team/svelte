<script>

import { link, Router, Route } from 'svelte-routing';

import Head from './head.svelte';

import PageDefault from './pages/default/page.svelte';
import PageHome from './pages/home/page.svelte';

export let version;

</script>

<Head />

<div class="page-root">
	<div class="page-header">
		<a use:link href="/Home">	
			SVELTE APP (v {version})
		</a>
	</div>
	<div class="page-content">
		<div class="page-content-center">
			<Router>
				<Route path="/"     component={PageDefault} />
				<Route path="/Home" component={PageHome}    />

				<Route path="/**">Page Not Found</Route>
			</Router>
		</div>
	</div>
</div>

<style lang="scss">

@import './styles/colors.scss';

.page-root {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: column;
	justify-content: center;
	align-items: center;
	position: absolute;
	left: 0;
	right: 0;
	top: 0;
	bottom: 0;
}

.page-header {
	width: 100%;
	display: block;
	color: #ffffff;
	background-color: $header;
	font-size: 32px;
	font-weight: bolder;
	text-align: center;
}

a {
	width: 100%;
	height: 100%;
	padding: 40px;
	display: block;
	font-family: 'Source Code Pro';
	color: #ffffff;
	text-decoration: none;
}

.page-content {
	width: 100%;
	display: block;
	flex-grow: 1;
	font-size: 32px;
	text-align: center;
	overflow-y: auto;
}

.page-content-center {
	width: 100%;
	height: 100%;
	display: flex;
	flex-direction: row;
	justify-content: center;
	align-items: center;
	color: #515151;
}

</style>
