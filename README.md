# deveshgoyal.github.io
Express.js flash notifications that can work with any template engine

<code>
var flash = require('flash-express');
</code><br>
<code>
app.use(flash());
</code>

<code>
	res.flash("success");
</code><br>
<code>
	res.flash("info", "info"); \n
</code><br>
<code>
	res.flash("error", "error", option); \n
</code><br>
<code>
	res.flash("warn", "warn", option); \n
</code>
