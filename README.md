# deveshgoyal.github.io
Express.js flash notifications that can work with any template engine

<code>
var flash = require('flash-express');
</code>
<code>
app.use(flash());
</code>

<code>
	res.flash("success");
</code>
<code>
	res.flash("info", "info"); \n
</code>
<code>
	res.flash("error", "error", option); \n
</code>
<code>
	res.flash("warn", "warn", option); \n
</code>
