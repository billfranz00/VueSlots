<template>
    <div class="container">
        <div class="row">
            <div class="col-xs-12">
            	<!-- <app-quote quote="A wonderful quote!"></app-quote> -->
            	<!-- <app-quote> -->
            		<!-- <h2 slot="title">{{ quoteTitle }}</h2> -->
            		<!-- <p slot="content">A wonderful Quote</p> -->
            		<!-- <p>A wonderful Quote</p> -->
            	<!-- </app-quote> -->
                <button @click="selectedComponent = 'appQuote'">Quote</button>
                <button @click="selectedComponent = 'appAuthor'">Author</button>
                <button @click="selectedComponent = 'appNew'">New</button>
                <hr>
                <p>{{ selectedComponent }}</p>
                <keep-alive>
                    <component :is="selectedComponent">
                        <p>Default Content</p>
                    </component>
                </keep-alive>
            </div>
        </div>
    </div>
</template>

<script>
	import Quote from './components/Quote.vue';
    import Author from './components/Author.vue';
    import New from './components/New.vue';

    export default {
    	data: function() {
    		return {
    			quoteTitle: 'The Quote',
                selectedComponent: 'appQuote'
    		}
    	},
        components: {
        	appQuote: Quote,
            appAuthor: Author,
            appNew: New
        }
    }
</script>

<style>
	h2 {
		color: green;
	}
</style>
