# deveshgoyal.github.io
Express.js flash notifications that can work with any template engine

<code>
var flash = require('flash-express'); \n
app.use(flash());
</code>

<code>
	res.flash("success"); \n
	res.flash("info", "info"); \n
	res.flash("error", "error", option); \n
	res.flash("warn", "warn", option); \n
</code>
