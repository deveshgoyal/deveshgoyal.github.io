# deveshgoyal.github.io
Express.js flash notifications that can work with any template engine

<code>
var flash = require('flash-express');
app.use(flash());
</code>

<code>
	res.flash("success");
	res.flash("info", "info");
	res.flash("error", "error", option);
	res.flash("warn", "warn", option);
</code>
