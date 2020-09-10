<template>
	<div>
		<h1>About page</h1>
		<p>Check the source code to see the custom meta tags added with our custom component</p>
		<twitter-head-card />
		<p>
			<nuxt-link to="/">Home page</nuxt-link>
		</p>		
	</div>
</template>

<script>
import TwitterHeadCard from '~/components/twitter-head-card.vue'
export default {
	head: {
		title: 'About Page',
		meta: [
			{
				hid: 'descrption',
				name: 'description',
				content: 'About page description'
			}
		]
	},
	components: {
		TwitterHeadCard
	}
	/**
	 * asyncData({ isStatic, isServer }) {
		return {
			name: isStatic? 'static': (isServer?'server': 'client')
		}
	   }
	 */
  	
}
</script>
