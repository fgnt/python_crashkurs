server:
	python3 -m http.server 3000

dependencies:
	mkdir -p _docsify/themes

	curl -L https://unpkg.com/docsify/themes/vue.css > _docsify/themes/vue.css
	sed -i '1d' _docsify/themes/vue.css  # Delete the first line, e.g. external font. https://stackoverflow.com/a/27099557/5766934
	# curl -L https://unpkg.com/docsify/themes/dark.css > _docsify/themes/dark.css
	# curl -L https://unpkg.com/docsify/themes/pure.css > _docsify/themes/pure.css
	# curl -L https://unpkg.com/docsify/themes/buble.css > _docsify/themes/buble.css

	curl -L https://unpkg.com/docsify/lib/docsify.js > _docsify/docsify.js
	curl -L https://unpkg.com/docsify/lib/plugins/search.js > _docsify/search.js
	curl -L https://unpkg.com/prismjs/components/prism-bash.js > _docsify/prism-bash.js
	curl -L https://unpkg.com/prismjs/components/prism-python.js > _docsify/prism-python.js
	curl -L https://unpkg.com/docsify-copy-code@2 > _docsify/docsify-copy-code
	# curl -L https://cdn.jsdelivr.net/npm/docsify-katex@latest/dist/docsify-katex.js > _docsify/docsify-katex.js
	# curl -L https://cdn.jsdelivr.net/npm/katex@latest/dist/katex.min.css > _docsify/katex.min.css

