<html><head><meta http-equiv="Content-Type" content="text/html; charset=utf-8"/><title>Python Interview Notes</title><style>
/* cspell:disable-file */
/* webkit printing magic: print all background colors */
html {
	-webkit-print-color-adjust: exact;
}
* {
	box-sizing: border-box;
	-webkit-print-color-adjust: exact;
}

html,
body {
	margin: 0;
	padding: 0;
}
@media only screen {
	body {
		margin: 2em auto;
		max-width: 900px;
		color: rgb(55, 53, 47);
	}
}

body {
	line-height: 1.5;
	white-space: pre-wrap;
}

a,
a.visited {
	color: inherit;
	text-decoration: underline;
}

.pdf-relative-link-path {
	font-size: 80%;
	color: #444;
}

h1,
h2,
h3 {
	letter-spacing: -0.01em;
	line-height: 1.2;
	font-weight: 600;
	margin-bottom: 0;
}

.page-title {
	font-size: 2.5rem;
	font-weight: 700;
	margin-top: 0;
	margin-bottom: 0.75em;
}

h1 {
	font-size: 1.875rem;
	margin-top: 1.875rem;
}

h2 {
	font-size: 1.5rem;
	margin-top: 1.5rem;
}

h3 {
	font-size: 1.25rem;
	margin-top: 1.25rem;
}

.source {
	border: 1px solid #ddd;
	border-radius: 3px;
	padding: 1.5em;
	word-break: break-all;
}

.callout {
	border-radius: 3px;
	padding: 1rem;
}

figure {
	margin: 1.25em 0;
	page-break-inside: avoid;
}

figcaption {
	opacity: 0.5;
	font-size: 85%;
	margin-top: 0.5em;
}

mark {
	background-color: transparent;
}

.indented {
	padding-left: 1.5em;
}

hr {
	background: transparent;
	display: block;
	width: 100%;
	height: 1px;
	visibility: visible;
	border: none;
	border-bottom: 1px solid rgba(55, 53, 47, 0.09);
}

img {
	max-width: 100%;
}

@media only print {
	img {
		max-height: 100vh;
		object-fit: contain;
	}
}

@page {
	margin: 1in;
}

.collection-content {
	font-size: 0.875rem;
}

.column-list {
	display: flex;
	justify-content: space-between;
}

.column {
	padding: 0 1em;
}

.column:first-child {
	padding-left: 0;
}

.column:last-child {
	padding-right: 0;
}

.table_of_contents-item {
	display: block;
	font-size: 0.875rem;
	line-height: 1.3;
	padding: 0.125rem;
}

.table_of_contents-indent-1 {
	margin-left: 1.5rem;
}

.table_of_contents-indent-2 {
	margin-left: 3rem;
}

.table_of_contents-indent-3 {
	margin-left: 4.5rem;
}

.table_of_contents-link {
	text-decoration: none;
	opacity: 0.7;
	border-bottom: 1px solid rgba(55, 53, 47, 0.18);
}

table,
th,
td {
	border: 1px solid rgba(55, 53, 47, 0.09);
	border-collapse: collapse;
}

table {
	border-left: none;
	border-right: none;
}

th,
td {
	font-weight: normal;
	padding: 0.25em 0.5em;
	line-height: 1.5;
	min-height: 1.5em;
	text-align: left;
}

th {
	color: rgba(55, 53, 47, 0.6);
}

ol,
ul {
	margin: 0;
	margin-block-start: 0.6em;
	margin-block-end: 0.6em;
}

li > ol:first-child,
li > ul:first-child {
	margin-block-start: 0.6em;
}

ul > li {
	list-style: disc;
}

ul.to-do-list {
	text-indent: -1.7em;
}

ul.to-do-list > li {
	list-style: none;
}

.to-do-children-checked {
	text-decoration: line-through;
	opacity: 0.375;
}

ul.toggle > li {
	list-style: none;
}

ul {
	padding-inline-start: 1.7em;
}

ul > li {
	padding-left: 0.1em;
}

ol {
	padding-inline-start: 1.6em;
}

ol > li {
	padding-left: 0.2em;
}

.mono ol {
	padding-inline-start: 2em;
}

.mono ol > li {
	text-indent: -0.4em;
}

.toggle {
	padding-inline-start: 0em;
	list-style-type: none;
}

/* Indent toggle children */
.toggle > li > details {
	padding-left: 1.7em;
}

.toggle > li > details > summary {
	margin-left: -1.1em;
}

.selected-value {
	display: inline-block;
	padding: 0 0.5em;
	background: rgba(206, 205, 202, 0.5);
	border-radius: 3px;
	margin-right: 0.5em;
	margin-top: 0.3em;
	margin-bottom: 0.3em;
	white-space: nowrap;
}

.collection-title {
	display: inline-block;
	margin-right: 1em;
}

.simple-table {
	margin-top: 1em;
	font-size: 0.875rem;
}

.simple-table-header {
	background: rgb(247, 246, 243);
	color: black;
	font-weight: 500;
}

time {
	opacity: 0.5;
}

.icon {
	display: inline-block;
	max-width: 1.2em;
	max-height: 1.2em;
	text-decoration: none;
	vertical-align: text-bottom;
	margin-right: 0.5em;
}

img.icon {
	border-radius: 3px;
}

.user-icon {
	width: 1.5em;
	height: 1.5em;
	border-radius: 100%;
	margin-right: 0.5rem;
}

.user-icon-inner {
	font-size: 0.8em;
}

.text-icon {
	border: 1px solid #000;
	text-align: center;
}

.page-cover-image {
	display: block;
	object-fit: cover;
	width: 100%;
	height: 30vh;
}

.page-header-icon {
	font-size: 3rem;
	margin-bottom: 1rem;
}

.page-header-icon-with-cover {
	margin-top: -0.72em;
	margin-left: 0.07em;
}

.page-header-icon img {
	border-radius: 3px;
}

.link-to-page {
	margin: 1em 0;
	padding: 0;
	border: none;
	font-weight: 500;
}

p > .user {
	opacity: 0.5;
}

td > .user,
td > time {
	white-space: nowrap;
}

input[type="checkbox"] {
	transform: scale(1.5);
	margin-right: 0.6em;
	vertical-align: middle;
}

p {
	margin-top: 0.5em;
	margin-bottom: 0.5em;
}

.image {
	border: none;
	margin: 1.5em 0;
	padding: 0;
	border-radius: 0;
	text-align: center;
}

.code,
code {
	background: rgba(135, 131, 120, 0.15);
	border-radius: 3px;
	padding: 0.2em 0.4em;
	border-radius: 3px;
	font-size: 85%;
	tab-size: 2;
}

code {
	color: #eb5757;
}

.code {
	padding: 1.5em 1em;
}

.code-wrap {
	white-space: pre-wrap;
	word-break: break-all;
}

.code > code {
	background: none;
	padding: 0;
	font-size: 100%;
	color: inherit;
}

blockquote {
	font-size: 1.25em;
	margin: 1em 0;
	padding-left: 1em;
	border-left: 3px solid rgb(55, 53, 47);
}

.bookmark {
	text-decoration: none;
	max-height: 8em;
	padding: 0;
	display: flex;
	width: 100%;
	align-items: stretch;
}

.bookmark-title {
	font-size: 0.85em;
	overflow: hidden;
	text-overflow: ellipsis;
	height: 1.75em;
	white-space: nowrap;
}

.bookmark-text {
	display: flex;
	flex-direction: column;
}

.bookmark-info {
	flex: 4 1 180px;
	padding: 12px 14px 14px;
	display: flex;
	flex-direction: column;
	justify-content: space-between;
}

.bookmark-image {
	width: 33%;
	flex: 1 1 180px;
	display: block;
	position: relative;
	object-fit: cover;
	border-radius: 1px;
}

.bookmark-description {
	color: rgba(55, 53, 47, 0.6);
	font-size: 0.75em;
	overflow: hidden;
	max-height: 4.5em;
	word-break: break-word;
}

.bookmark-href {
	font-size: 0.75em;
	margin-top: 0.25em;
}

.sans { font-family: ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol"; }
.code { font-family: "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace; }
.serif { font-family: Lyon-Text, Georgia, ui-serif, serif; }
.mono { font-family: iawriter-mono, Nitti, Menlo, Courier, monospace; }
.pdf .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK JP'; }
.pdf:lang(zh-CN) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK SC'; }
.pdf:lang(zh-TW) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK TC'; }
.pdf:lang(ko-KR) .sans { font-family: Inter, ui-sans-serif, -apple-system, BlinkMacSystemFont, "Segoe UI", Helvetica, "Apple Color Emoji", Arial, sans-serif, "Segoe UI Emoji", "Segoe UI Symbol", 'Twemoji', 'Noto Color Emoji', 'Noto Sans CJK KR'; }
.pdf .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .code { font-family: Source Code Pro, "SFMono-Regular", Menlo, Consolas, "PT Mono", "Liberation Mono", Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.pdf .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK JP'; }
.pdf:lang(zh-CN) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK SC'; }
.pdf:lang(zh-TW) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK TC'; }
.pdf:lang(ko-KR) .serif { font-family: PT Serif, Lyon-Text, Georgia, ui-serif, serif, 'Twemoji', 'Noto Color Emoji', 'Noto Serif CJK KR'; }
.pdf .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK JP'; }
.pdf:lang(zh-CN) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK SC'; }
.pdf:lang(zh-TW) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK TC'; }
.pdf:lang(ko-KR) .mono { font-family: PT Mono, iawriter-mono, Nitti, Menlo, Courier, monospace, 'Twemoji', 'Noto Color Emoji', 'Noto Sans Mono CJK KR'; }
.highlight-default {
	color: rgba(55, 53, 47, 1);
}
.highlight-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(145, 145, 142, 1);
}
.highlight-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(187, 132, 108, 1);
}
.highlight-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(215, 129, 58, 1);
}
.highlight-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 148, 51, 1);
}
.highlight-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(108, 155, 125, 1);
}
.highlight-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(91, 151, 189, 1);
}
.highlight-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(167, 130, 195, 1);
}
.highlight-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(205, 116, 159, 1);
}
.highlight-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(225, 111, 100, 1);
}
.highlight-gray_background {
	background: rgba(241, 241, 239, 1);
}
.highlight-brown_background {
	background: rgba(244, 238, 238, 1);
}
.highlight-orange_background {
	background: rgba(251, 236, 221, 1);
}
.highlight-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.highlight-teal_background {
	background: rgba(237, 243, 236, 1);
}
.highlight-blue_background {
	background: rgba(231, 243, 248, 1);
}
.highlight-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.highlight-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.highlight-red_background {
	background: rgba(253, 235, 236, 1);
}
.block-color-default {
	color: inherit;
	fill: inherit;
}
.block-color-gray {
	color: rgba(120, 119, 116, 1);
	fill: rgba(145, 145, 142, 1);
}
.block-color-brown {
	color: rgba(159, 107, 83, 1);
	fill: rgba(187, 132, 108, 1);
}
.block-color-orange {
	color: rgba(217, 115, 13, 1);
	fill: rgba(215, 129, 58, 1);
}
.block-color-yellow {
	color: rgba(203, 145, 47, 1);
	fill: rgba(203, 148, 51, 1);
}
.block-color-teal {
	color: rgba(68, 131, 97, 1);
	fill: rgba(108, 155, 125, 1);
}
.block-color-blue {
	color: rgba(51, 126, 169, 1);
	fill: rgba(91, 151, 189, 1);
}
.block-color-purple {
	color: rgba(144, 101, 176, 1);
	fill: rgba(167, 130, 195, 1);
}
.block-color-pink {
	color: rgba(193, 76, 138, 1);
	fill: rgba(205, 116, 159, 1);
}
.block-color-red {
	color: rgba(212, 76, 71, 1);
	fill: rgba(225, 111, 100, 1);
}
.block-color-gray_background {
	background: rgba(241, 241, 239, 1);
}
.block-color-brown_background {
	background: rgba(244, 238, 238, 1);
}
.block-color-orange_background {
	background: rgba(251, 236, 221, 1);
}
.block-color-yellow_background {
	background: rgba(251, 243, 219, 1);
}
.block-color-teal_background {
	background: rgba(237, 243, 236, 1);
}
.block-color-blue_background {
	background: rgba(231, 243, 248, 1);
}
.block-color-purple_background {
	background: rgba(244, 240, 247, 0.8);
}
.block-color-pink_background {
	background: rgba(249, 238, 243, 0.8);
}
.block-color-red_background {
	background: rgba(253, 235, 236, 1);
}
.select-value-color-pink { background-color: rgba(245, 224, 233, 1); }
.select-value-color-purple { background-color: rgba(232, 222, 238, 1); }
.select-value-color-green { background-color: rgba(219, 237, 219, 1); }
.select-value-color-gray { background-color: rgba(227, 226, 224, 1); }
.select-value-color-orange { background-color: rgba(250, 222, 201, 1); }
.select-value-color-brown { background-color: rgba(238, 224, 218, 1); }
.select-value-color-red { background-color: rgba(255, 226, 221, 1); }
.select-value-color-yellow { background-color: rgba(253, 236, 200, 1); }
.select-value-color-blue { background-color: rgba(211, 229, 239, 1); }

.checkbox {
	display: inline-flex;
	vertical-align: text-bottom;
	width: 16;
	height: 16;
	background-size: 16px;
	margin-left: 2px;
	margin-right: 5px;
}

.checkbox-on {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20width%3D%2216%22%20height%3D%2216%22%20fill%3D%22%2358A9D7%22%2F%3E%0A%3Cpath%20d%3D%22M6.71429%2012.2852L14%204.9995L12.7143%203.71436L6.71429%209.71378L3.28571%206.2831L2%207.57092L6.71429%2012.2852Z%22%20fill%3D%22white%22%2F%3E%0A%3C%2Fsvg%3E");
}

.checkbox-off {
	background-image: url("data:image/svg+xml;charset=UTF-8,%3Csvg%20width%3D%2216%22%20height%3D%2216%22%20viewBox%3D%220%200%2016%2016%22%20fill%3D%22none%22%20xmlns%3D%22http%3A%2F%2Fwww.w3.org%2F2000%2Fsvg%22%3E%0A%3Crect%20x%3D%220.75%22%20y%3D%220.75%22%20width%3D%2214.5%22%20height%3D%2214.5%22%20fill%3D%22white%22%20stroke%3D%22%2336352F%22%20stroke-width%3D%221.5%22%2F%3E%0A%3C%2Fsvg%3E");
}
	
</style></head><body><article id="c24cefb0-f612-4fbd-8455-93d64d0d8df8" class="page serif"><header><h1 class="page-title">Python Interview Notes</h1></header><div class="page-body"><ol type="1" id="530d48cf-fe53-4c1a-b049-6d8c368656b6" class="numbered-list" start="1"><li><strong>Key features of Python ?</strong><ul id="30c7fb6d-8aa6-4c17-89ac-c10170ac0ee8" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>intrepreted language</strong> means the source code written in .py need not to be compiled before it runs. It checks each line of your program and converts to bytecode during the execution phase.</li></ul><ul id="7aa28440-0a77-44b6-85aa-49e0f33f7537" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>dynamically typed </strong>that means no need of declaring variable datatypes and automatically detects the type when you assign the value to variable.</li></ul><ul id="2653353a-9eeb-4b2d-abeb-a442217740d9" class="bulleted-list"><li style="list-style-type:disc">Python support <strong>object-oriented programming. </strong>Allows to create the classes along with composition and inheritance. Python does not support access modifiers like <strong>Java</strong>.</li></ul><ul id="ae367fe9-9737-4497-a701-f6179305e108" class="bulleted-list"><li style="list-style-type:disc">In Python, functions are <strong>first class objects </strong>means they can be assigned to variables, returned from other functions and passed into functions.</li></ul><ul id="345eaa2e-8903-4ee7-8a3c-7dfb3483a05a" class="bulleted-list"><li style="list-style-type:disc">Python syntax is simpler like plain english language but the running of code is slower whereas the code will not be compiled. Python allows C-based extension which make our code optimized . Best example is <strong>Numpy</strong></li></ul><ul id="91eaf66e-ca3b-4026-9844-ee02cb8a3e05" class="bulleted-list"><li style="list-style-type:disc">Python is used widely among industries: web applications, automation, scientific modeling, big data applications, Artifical Intelligence.</li></ul><p id="f78407de-8bb9-4902-a243-a28019301257" class="">
</p></li></ol><ol type="1" id="14f7ed68-6fcf-4cad-aea2-8bebea58210d" class="numbered-list" start="2"><li><strong>What type of programming language is python?</strong><p id="0642714a-2c92-414b-aeaa-d1392bb18858" class="">Basically Python is scripting language but now-a-days it is growing as general-purpose programming language.</p></li></ol><p id="6b2577d6-a989-4793-bd10-0618411247e1" class="">
</p><ol type="1" id="60f508ad-69a5-42ef-b3de-d50cac998be3" class="numbered-list" start="3"><li><strong>What do you mean by Intrepreted Language?</strong><p id="21e1bd37-dabf-4155-bc5c-1b915d4a1f04" class="">An Intepreted language is any programming language that the each of line of the program is converted into machine-code at the time of execution where intrepreter is responsible for scanning each line one by one and then executes and there is no compilation process in intrepreted languages.</p><p id="17f4d9d2-8c36-47ae-be22-448dfd01acdf" class="">
</p></li></ol><ol type="1" id="c31c50f9-0409-4351-bee7-084949de5b7f" class="numbered-list" start="4"><li><strong>What is PEP8 ?</strong><p id="d0ee517f-7cd1-4a97-84df-74d3087cc7e5" class="">PEP8 stands for Python Enchanment Proposal. It is a set of rules that specify how to format Python code for maximum reability.</p></li></ol><p id="b1d1a2e2-c433-407a-a996-04d89a0fdc5a" class="">
</p><ol type="1" id="667836a4-e6d4-48b6-a67e-9d9fc959b699" class="numbered-list" start="5"><li><strong>Benefits of Python ?</strong><ul id="b916abe0-1f8d-4544-8330-701341e9ab87" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>high-level programming level</strong> that means easy to read, write and learn.</li></ul><ul id="1d6b8258-67db-40a4-a083-ff302656e354" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>Intrepreted language</strong> means executes the code line by line with no compilation process involved and stops when the intrepreter raises an exception or an error at particular line.</li></ul><ul id="6d0ea64c-81f0-4846-bbb0-924a28fdeb96" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>open-source</strong>. Free to use.</li></ul><ul id="516f20a8-224f-4ff5-9ff4-29e269a5cce1" class="bulleted-list"><li style="list-style-type:disc">Python has large community of developers and support for <strong>vast libraries</strong> and allows developer to import packages using Python Package Manager(pip)</li></ul><ul id="5fc26165-a5c5-4d77-bae3-4b3288035422" class="bulleted-list"><li style="list-style-type:disc">Python is <strong>portable</strong> that means python program can run on any platform.</li></ul><p id="f239cef7-83aa-4d72-87b2-7557185f219f" class="">
</p></li></ol><ol type="1" id="3891ea67-5683-4e17-9370-d45f3aa59897" class="numbered-list" start="6"><li><strong>Python namespaces (Scopes in JS) ?</strong><figure id="24327883-0fab-4d1c-8722-1f409fa13e58"><a href="https://realpython.com/python-namespaces-scope/" class="bookmark source"><div class="bookmark-info"><div class="bookmark-text"><div class="bookmark-title">Namespaces and Scope in Python - Real Python</div><div class="bookmark-description">In this tutorial, you&#x27;ll learn about Python namespaces, the structures used to store and organize the symbolic names created during execution of a Python program. You&#x27;ll learn when namespaces are created, how they are implemented, and how they define variable scope.</div></div><div class="bookmark-href"><img src="https://cdn.realpython.com/static/favicon.68cbf4197b0c.png" class="icon bookmark-icon"/>https://realpython.com/python-namespaces-scope/</div></div><img src="https://files.realpython.com/media/Namespaces-and-Scope-in-Python_Watermarked.cb9ad9d896cb.jpg" class="bookmark-image"/></a></figure><p id="9fd2953d-18f7-4298-b927-e1cc202819a1" class="">A namespace is the name asssigned to each object in python.</p><p id="e9d22063-041c-4ff7-92d5-f824ae656c8b" class="">Think of namespace as dictonary in which the keys are the object-names and values are the objects themselves</p><p id="817adade-9956-4302-b2c9-eaa618136300" class="">Each key-value pair maps a name to its corresponding object.</p><p id="1ba073f0-8106-4a50-9e38-7f13af57a6a3" class="">There are four levels of namespaces in Python:</p><ol type="1" id="8d7cff82-42a9-4674-864b-83ea39c95468" class="numbered-list" start="1"><li><strong>Built-in namespace: </strong><p id="c957144a-de7d-424b-9464-2e29d9ec5c28" class="">contains the names of all Python built-in objects.</p><p id="1a9897a5-a1c1-4b06-8601-88304a32cfc0" class="">Available where you want in the program.</p><p id="2b8661e4-ab72-46b5-babc-2f7e29df8352" class="">Eg: built-in object types - <strong>int, str</strong><div class="indented"><p id="0af7ac77-61e2-4c28-9032-7542031e39ab" class="">built-in functions - <strong>max ( ) , len( )</strong></p></div></p></li></ol><ol type="1" id="5feaa4d6-8a40-4141-8632-0d836f15b353" class="numbered-list" start="2"><li><strong>Global namespace:</strong><p id="cc0fa049-a708-44e1-a2e7-02dc7aa471f5" class="">contains any names defined at the level of main program.</p><p id="8928dec3-ca5d-4c7a-888b-e354cdfe0726" class="">Python creates global namespace when python started running until its termination.</p></li></ol><ol type="1" id="fe3c490a-bbea-4323-858c-7c1902f164ee" class="numbered-list" start="3"><li><strong>Local and Enclosing Namespace:</strong><p id="9118ba93-f492-400e-9cfb-416210b3b0c4" class="">creates a new namespace whenever a function executes.</p><p id="e3cec05e-d68f-418a-ac9d-6fe21bbee190" class="">Enclosing namespaces are at the higher level or outer function whereas local namespace is inner function wrapped inside the enclosing namespace.</p><p id="e51ca140-0fa4-4db7-a9b1-7dcc4dee0758" class="">The namespace is local to that function and remains in existence until that function terminates.</p><p id="acf85656-acd8-4ea3-9324-1da6c712e5ce" class="">
</p></li></ol></li></ol><ol type="1" id="4a7eb80d-8486-45cb-b9e1-a32486220ce6" class="numbered-list" start="7"><li><strong>Decorators</strong><pre id="4144eb55-1d93-42b7-b5b2-992f8ed07858" class="code code-wrap"><code>@decorator
def div(a, b):
    print(a/b)

@decorator_fun
def smart_div(func):
    def inner(a, b):
        if a &lt; b:
            a,b = b,a
        return func(a, b)
    return inner

div1 = smart_div(div)
div1(2, 4)</code></pre><p id="b9b86a2b-6305-4bf0-b606-b1443f1f0d5d" class="">A decorator is a function that takes  another function as its argument, and returns yet another function.</p><p id="5731c3b0-9830-4d90-885d-181d7df87f0a" class="">
</p></li></ol><ol type="1" id="5c45d489-433d-4b50-80fe-1689ac316130" class="numbered-list" start="8"><li><strong>Dictionary and List Comphrension ?</strong><p id="4338650b-9254-4aa7-a6df-a87b1529c739" class="">List comphrension:</p><pre id="fe63d1f5-e967-4796-bbbe-ed3b08dba327" class="code code-wrap"><code>numbers = [1, 2, 3, 4, 5, 6]
squares = []

for num in numbers:
		squares.append(number ** 2)
print(squares) # [1, 4, 9, 16, 25, 36]

#using list comphrension
squares = [num ** 2 for num in numbers]
print(squares) # [1, 4, 9, 16, 25, 36]</code></pre><p id="715863cf-77b6-4367-bceb-cf3432777f35" class="">Dictionary comphrension:</p><pre id="3a889f15-3b15-4976-9803-7144019db81d" class="code code-wrap"><code>stocks = {
		&#x27;AAPL&#x27;: 256,
		&#x27;AMZN&#x27;: 332,
		&#x27;NFLX&#x27;: 151,
		&#x27;MCSF&#x27;: 225
}

new_stocks = {}
for symbol, price in stocks.items():
        new_stocks[symbol] = price * 1.02

print(new_stocks)

# refactoring the line 8 - 10 using dictionary comphrension
new_stocks = { symbol: price * 1.02 for (symbol, price) in stocks.items()}
print(new_stocks)
					</code></pre><p id="88366f43-359b-4334-a230-cb41b14b0bde" class="">
</p></li></ol><ol type="1" id="fca8578a-130c-44e5-a8bf-37e818a643b1" class="numbered-list" start="9"><li><strong>Built-in datatypes in Python ?</strong><p id="70ae5008-72ca-4483-80fc-68775406b0d4" class="">There are 7 built-in datatypes in Python:</p><ol type="1" id="db0ae718-a026-463a-8d86-2a566a38e7fd" class="numbered-list" start="1"><li><strong>Numbers: </strong>integer, floating point and complex numbers(3 + 4j)</li></ol><ol type="1" id="63943c48-17e7-4d9a-9d85-143f19ab49e3" class="numbered-list" start="2"><li><strong>List: </strong>A collection of ordered values and can be declared using square brackets.</li></ol><ol type="1" id="54b9a117-8258-4b23-9d92-78882469f4e4" class="numbered-list" start="3"><li><strong>Tuple: </strong>A collection of ordered values which are immutable(cannot be modified) and can declared using parentheses.</li></ol><ol type="1" id="0ade6c92-265d-47f1-8173-4a66776f81e5" class="numbered-list" start="4"><li><strong>String: </strong>A sequence of characters is called String. Declared inside single or double quotes.</li></ol><ol type="1" id="887c7912-24bd-433c-a770-b8818c0118b3" class="numbered-list" start="5"><li><strong>Set: </strong>A collection of unordered values and can be declared inside curly braces.</li></ol><ol type="1" id="1e13f396-6a1a-4ca3-8665-22db79904f29" class="numbered-list" start="6"><li><strong>Dictionary: </strong>A collection of key-value pairs where each key is associated to value. Declared inside the curly braces.</li></ol><ol type="1" id="e7fa8f27-ec7a-4a27-8651-c62bd68b0595" class="numbered-list" start="7"><li><strong>Boolean:  </strong>Bool Datatype with two values - True and False.</li></ol><p id="e8ff97c2-0fa2-4a16-b59b-c489692f760d" class="">
</p></li></ol><ol type="1" id="181ac9d5-caab-4abf-b471-06afaa7da06d" class="numbered-list" start="10"><li><strong>Difference between .py and .pyc ?</strong><p id="ecc3a122-50de-4963-ab41-4e16601b7332" class="">.py contains source code and .pyc contains the byte code of the python files.</p><p id="eb9858b4-4434-4512-9f1c-7cadfaed1076" class="">.pyc files are created when you import it from some other source to save time.</p><p id="8dc94006-f624-4fd0-91ae-4c9b871b1fd3" class="">
</p></li></ol><ol type="1" id="1ff5743b-437c-4e57-a954-95296285248b" class="numbered-list" start="11"><li><strong>Slicing in python ?</strong><p id="bcc8a325-8e3d-4683-9a97-4fc76e393aae" class="">Slicing is like accessing the part of a list, tuples and strings.</p><p id="8b2aedb8-7c57-4f62-9cd6-bdea511d6de5" class="">It is like taking out slice from pizza.</p><p id="b77ac244-6930-4710-8efd-286975655fad" class=""><strong>Syntax: [start: end: step]</strong></p><p id="829838ef-cb7a-49db-a1d4-2e12c4010b76" class=""><strong>start</strong> - position to start from</p><p id="7b0b5ddb-d1a7-4c6a-922e-afc1a443a244" class=""><strong>end</strong> - position where to end</p><p id="b8b8de1b-558d-42a2-b2f0-13454b7c7048" class=""><strong>step</strong> - for skipping the no. of items when declared</p><p id="e382fe46-418d-4d59-babd-c87264c37498" class="">
</p></li></ol><ol type="1" id="f7720547-a156-49c7-886d-4a8bdebb8586" class="numbered-list" start="12"><li><strong>What are keywords in Python?</strong><p id="e58c3703-0e85-44c7-8627-f9adefb58870" class="">Keywords are reserved words to a language which has special meaning. They cannot be used as variable or function names.</p></li></ol><p id="65e177bc-96f4-4d35-9521-fffa316096dd" class="">
</p><ol type="1" id="ef7a4961-2598-4f64-875d-b7cf9730a7e7" class="numbered-list" start="13"><li><strong>How memory is managed in Python?</strong><p id="6b6391d4-96d8-456f-b8fb-425f1cc5190b" class="">All python object and data structures are stored in <strong>private heap space.</strong> User doesn&#x27;t have access to private heap but the intrepreter takes care of it.</p><p id="ffe55e2b-0600-418e-a118-08866b40009a" class="">Allocation of heap space to python objects is done by <strong>Python memory manager.</strong></p><p id="52c7ae72-b0f4-49d9-8ba5-2030778a426a" class="">Python has in-built garabe collector which is responsible for collecting and recycling the unused memory so that it can be made available to heap.</p><p id="e6574208-c64c-4cd6-a77f-01e38a44805e" class="">
</p></li></ol><ol type="1" id="27c7dc46-2591-47b5-ae85-50e6da4d972e" class="numbered-list" start="14"><li><strong>PYTHON PATH ?</strong><p id="1bdefdb2-5811-4d6e-a8dd-2cb5b57679b4" class=""> It is an environment variable which is used when a module is imported.</p><p id="86f5010a-ccdd-442f-97ab-4162094b3744" class="">PYTHON PATH also checks for the presence of imported modules in various directories.</p><p id="138e57c1-2d7e-48a1-9b56-6f1a6f5eacb9" class="">Intrepreter uses it to determine which module to load.</p></li></ol><p id="7fff49ad-bcf0-414a-98b1-df00b5200269" class="">
</p><ol type="1" id="01b03643-88b5-43cd-bedb-1d59a572f67c" class="numbered-list" start="15"><li><strong>What are modules?</strong><p id="e68b3e51-7fc6-441f-a92a-e0abff6239a7" class="">Modules are files contain python code and nothing but the python code by written other programmers that we import them in our project and use them.</p><p id="96a56014-0cb8-447b-9ad2-a0d3365ecf82" class=""><strong>Commonly used modules in Python:</strong></p><p id="9e350c2d-f0d4-4b41-8a1d-eeed90e9738d" class="">os, sys, math, random, data time, JSON</p></li></ol><p id="5bd90e65-671a-4a64-9463-e61c13f918c1" class="">
</p><ol type="1" id="d180d092-0a1c-487b-8b95-e987aee5b839" class="numbered-list" start="16"><li><strong>Local variables and Global variables ?</strong><p id="1e4613d7-1a0a-4296-874a-a4fde5db54c0" class="">A variable which is declared outside a function or in global space is called <strong>Global variable.</strong></p><p id="c440c395-a31d-437c-ac44-ab92e01e317e" class="">These variables can be accessed anywhere in the program.</p><p id="71ba2265-708c-4ea8-8b73-f3f85cde841c" class="">A variable which is declared inside a function or bound inside block code(conditional statements) is called <strong>Local variable.</strong></p><p id="300f5bf9-d76b-4a9b-bb78-cc0257b7d930" class="">These variables only available inside and to that function.</p></li></ol><p id="c4b0d6d6-7274-4a42-bacb-7faabdec8880" class="">
</p><ol type="1" id="c87e8c99-bc22-460f-865b-a0265c7d665a" class="numbered-list" start="17"><li><strong>Type conversion in Python?</strong><p id="9a7ba30b-0c46-4489-b359-1a24d2c131d0" class="">The process of converting one datatype to another datatype is known as <strong>Type conversion.</strong></p><ul id="ac21e496-066e-4666-8b7a-9c3919014a52" class="bulleted-list"><li style="list-style-type:disc">int( ) - converts any to integer</li></ul><ul id="3781ddae-727d-4153-b009-a93b470a9366" class="bulleted-list"><li style="list-style-type:disc">float( ) - converts any to float</li></ul><ul id="0a5d93ed-ecd8-4478-b374-218bc91e8fe2" class="bulleted-list"><li style="list-style-type:disc">ord( ) - converts char to integers</li></ul><ul id="99a79427-91ec-45eb-9bec-04ba40d72faa" class="bulleted-list"><li style="list-style-type:disc">hex( ) - converts integer to hexadecimal</li></ul><ul id="a052a5f7-7f44-4a1e-a825-bb6583321983" class="bulleted-list"><li style="list-style-type:disc">oct( ) - converts integer to octal</li></ul><ul id="833cff12-1994-4437-ad67-bc86bdeaeed3" class="bulleted-list"><li style="list-style-type:disc">tuple( ) - converts to tuple</li></ul><ul id="c7402d7a-4e7b-410d-820d-dd95976894cd" class="bulleted-list"><li style="list-style-type:disc">list( ) - converts any to  list</li></ul><ul id="80f4f8de-2b48-4fbe-b3ee-4c4ef9c48dc9" class="bulleted-list"><li style="list-style-type:disc">dict( ) - converts any to dictionary</li></ul><ul id="88d76e95-7425-407f-89e0-c100cb605b15" class="bulleted-list"><li style="list-style-type:disc">str( ) - converts any. to string</li></ul></li></ol><p id="d142356b-988f-4351-ab98-f0d0a4f5bcfe" class="">
</p><ol type="1" id="545d67e8-cbf0-466f-94e0-a8f3d57e9da0" class="numbered-list" start="18"><li><strong>Is indentation mandatory in Python ?</strong><p id="42be80c8-0cae-4b85-9930-1386f3201359" class="">Indenation is required to segregate one block from another block. Other languages like Java, Javascript uses to curly braces whereas Python uses Indenation for loops, classes, functions.</p><p id="f1e03370-5a03-486c-b2df-f5068d746838" class="">Indenation defines the scope of a block. </p></li></ol><p id="c5058cbe-9c32-4ae7-8707-c84685d825d7" class="">
</p><ol type="1" id="3550266f-6047-4258-86d8-82822ec20fdf" class="numbered-list" start="19"><li><strong>Difference between Arrays and Lists?</strong><p id="1d0f006e-836b-449c-bb27-0e6193b527b0" class="">Arrays and Lists are similar in nature when reading, writing ans storing the data.</p><p id="761042ae-2181-44ce-9fbf-9c5889c2273d" class=""> Arrays restricts to define the values of single datatype whereas lists allows you to define values of different datatypes.</p><p id="c77f72a8-aa4b-4908-a5d4-c213abba1382" class="">In Python, Arrays are built-in data types. Need to import them as module and Lists are built-in data types.</p></li></ol><p id="9703b56e-45bb-4d43-96c6-1279e47986aa" class=""> </p><ol type="1" id="9eba8b93-06b7-4900-b1bb-531baff489fb" class="numbered-list" start="20"><li><strong>__init__ in Python?</strong><p id="a81a045e-3230-46ef-9d84-eb1593b380d9" class="">__init__ is a constructor method which is method takes parameters and has no return statement.</p><p id="808b09d7-7807-44e7-bc0b-114fc13a7cc5" class=""><strong> </strong>Automatically called when a new object instance of a class is created and allocates memory to that instance object.</p><pre id="4e8ea3a5-802a-4e26-9b42-c6caa02a3db1" class="code code-wrap"><code>def Car:
	def __init__(self, make, model, capacity):
			self.make = make
			self.model = model
			self.capacity = capacity

new_car = Car(&#x27;Porsche&#x27;, &#x27;911 GT3&#x27;, &#x27;3.5 L&#x27;)
print(new_car)</code></pre></li></ol><p id="cccf26e8-cbb7-42fd-9d51-1e34b5035811" class="">
</p><ol type="1" id="82576735-527b-4a4f-ab86-13372cf75c59" class="numbered-list" start="21"><li><strong>Lambda function in Python?</strong><p id="37b0dab5-7730-43cb-bec7-211583faec06" class="">A lambda function is anonymous function in Python.</p><p id="a47adfe5-0e8b-4922-8631-99f854a97eb4" class="">Anyonomous function is a function with no function name.</p><p id="ea88085b-1b3f-491a-a736-79a5d2a4f305" class="">Lambda function can have any number of parameters but have only one conditional statement.</p><pre id="262c679e-4bb0-471f-822c-117856a0181d" class="code code-wrap"><code># Syntax: lambda parameters: expression

def full_name(first_name, last_name, formatter):
    return formatter(first_name, last_name)

new_name = full_name(&#x27;Naveen&#x27;, &#x27;Kollu&#x27;, lambda first_name, last_name: f&quot;{first_name} {last_name}&quot;)
print(new_name)</code></pre></li></ol><p id="cac73d71-479b-4acc-a564-dc381fd68436" class="">
</p><ol type="1" id="e5b0535d-8ebf-4f98-8589-650a7c5f40ee" class="numbered-list" start="22"><li><strong>Self in Python ?</strong><p id="9fe4d1ef-f5f5-48c1-a991-7d7d27e65e62" class="">Self is an instance or object of a class in Python. By the convention we name it as <strong>self </strong>but we can name it anything we want. It is the first parameter of any function inside a class. </p><p id="dc0665f1-afa9-4bd5-ac46-4b098baf719c" class="">self in <strong>init</strong> refers to instance of new object.</p><p id="60631b10-1ef2-448c-ac29-41490c9ce0f0" class="">self in <strong>methods </strong>refers to object whose method is called.</p><p id="9e138aca-479b-4fad-a2d9-13db97833916" class="">
</p></li></ol><ol type="1" id="6aac3ed5-befe-4293-93df-a721416feae4" class="numbered-list" start="23"><li><strong>{:: -1} does in Python?</strong><p id="851d7b9d-da67-4b66-8050-9f902a724394" class="">Reverse the order of sequenced values.</p><pre id="86d10f68-ea2a-4239-810c-cc72c78646a6" class="code code-wrap"><code>lists = [1, 2, 3]
print(lists[::-1])</code></pre><p id="dd7e1de2-8c6f-47d3-a918-b078e866aa30" class="">
</p></li></ol><ol type="1" id="e8c9c4f6-54b1-4c3b-a767-bb02190d7719" class="numbered-list" start="24"><li><strong>Iterators in Python?</strong><p id="67ddde88-988d-4714-92b6-4116d865e5cf" class="">Iterators are the objects which can be traversed through or iterated upon.</p><p id="0451302b-2f88-498b-a423-537259311bbc" class="">
</p></li></ol><ol type="1" id="fa0e04e2-f675-4890-a5ac-fc9dc2dd9d45" class="numbered-list" start="25"><li><strong>Comments in Python?</strong><p id="2cfa1039-5eef-494b-8f51-d3cb9f1c705c" class="">For writing single line comments we use <strong>#(hash)</strong></p><p id="8e5785e4-5813-41b7-8a6c-fb6f062cfdc1" class="">For multiple-line comments, we use docstrings which are triple quotes <strong>&quot;&quot;&quot; &quot;&quot;&quot;</strong>.</p><p id="1fc70ef6-3cb1-420e-b8b3-0e035f70326f" class="">
</p></li></ol><ol type="1" id="648dda8a-7fb4-44b7-9823-ba44b02d57f7" class="numbered-list" start="26"><li><strong>Pickling and unpickling in Python?</strong><p id="31aea8f4-b9cc-4955-a8b9-bbe01a96d84f" class="">Pickle module accepts any object and converts it into a string representation and dumps it into a file using dump function is called <strong>Picking.</strong></p><p id="b31ebd6f-6512-4629-b797-fa718d639d87" class="">Retreiving Python objects from converted string representation is called <strong>unpickling.</strong></p><p id="5fb10432-2524-49da-bf41-70934c29ec72" class="">
</p></li></ol><ol type="1" id="0c46b8be-7a0f-45b0-a338-519385a5134f" class="numbered-list" start="27"><li><strong>Generators in Python?</strong><p id="fbb290d4-36dd-41fe-8d70-552508bba708" class="">Functions that return iterable set of items are called Generators.</p><p id="4c6164b8-c741-4302-9dee-7012c76492ed" class="">
</p></li></ol><ol type="1" id="e8c45df0-bd38-42d5-b542-479136132051" class="numbered-list" start="28"><li><strong>help( ) and dir( ) function in Python ?</strong><p id="2fdb334e-21b8-452d-a056-49d8fd295b9b" class=""><strong>help( )</strong> function is used to access the documentation of functions, classes, modules.</p><p id="77e94ba9-14fb-4fd7-927f-8091b9992b48" class=""><strong>dir( ) </strong>returns a list of attributes of the object and takes an object as argument.</p><p id="ae55c193-3fab-4d26-935a-c2d059aef670" class="">
</p></li></ol><ol type="1" id="d4f7d705-fadd-4768-9cf5-5789d7ddb8e8" class="numbered-list" start="29"><li><strong>Ternary operator in Python ?</strong> <pre id="280230d9-47af-42f7-ae30-eb9130cf4402" class="code code-wrap"><code>age = int(input(&#x27;Enter the age: &#x27;))

result = &quot;You&#x27;re welcome!&quot; if age &gt;= 18 else &quot;You&#x27;re not welcome&quot;
print(result)</code></pre><p id="7993d095-3ef7-4b17-b8b0-de013d920d3c" class="">
</p></li></ol><ol type="1" id="14537c27-cc01-44a6-afef-6d41848610ab" class="numbered-list" start="30"><li><strong>*args , **kwargs in Python ?</strong><p id="b06655fc-8d5a-4922-83ab-594e3a3c24ed" class=""><strong>*args</strong> are used when we don&#x27;t how manys arguments are passed to a function when it is called or to pass the list or tuple of items. Used to unpack the list and tuple.</p><pre id="7e13aa88-5a18-48a2-9d1e-08be40a1816c" class="code code-wrap"><code>def add(x, y, *args):
    return x + y + sum(args)


print(add(10, 20, 30, 40))</code></pre><p id="ed37e7a7-9e46-4623-808c-70b3e0a55775" class=""><strong>**kwargs </strong>are used when we don&#x27;t how many argument key-value pairs are passed to a function when it is called or to pass the dictionary as keyword arguments. Used to unpack dictionaries.</p><pre id="c77f8188-56d0-421d-82ce-60fe3fa9a790" class="code code-wrap"><code>def connect(**kwargs):
    print(kwargs)


config = {&#x27;server&#x27;: &#x27;localhost&#x27;,
        &#x27;port&#x27;: 3306,
        &#x27;user&#x27;: &#x27;root&#x27;,
        &#x27;password&#x27;: &#x27;Py1thon!Xt12&#x27;}

connect(**config)</code></pre><p id="727bdd85-e0c8-480e-a8e6-5aedb79f3d7f" class="">
</p></li></ol><h3 id="70308f49-c79b-477c-8d3f-389aaf55c693" class="">Object Oriented Programming in Python</h3><p id="bee396ee-dca8-4a7d-b9e6-575573f99cf7" class="">
</p><ol type="1" id="a9b66003-545c-4c7e-a73d-caee5bf7689d" class="numbered-list" start="31"><li><strong>Difference between Class variables and Instance variables?</strong><p id="7119e6af-53e0-442e-a7db-88cee16ac5f2" class="">A variable is said to class variable when it is <strong>bound to a class</strong> whereas instance variable is bound to <strong>specific instance of a class.</strong> </p><pre id="6a377a0d-2501-41e0-85f5-8a402b537f3e" class="code code-wrap"><code>class HtmlDocument:

    # Class variables
    version = 5
    extension = &#x27;html&#x27;

    def __init__(self, name, contents):
        # Instance variables
        self.name = name
        self.contents = contents

# Accessing the class variables: className.variableName
print(HtmlDocument.extension)

# Initializing and accessing the instance variables: objName = className(params) ---&gt; objName.variableName
version_check = HtmlDocument(&#x27;HTML&#x27;, &#x27;metaprogramming&#x27;)
print(version_check.contents)</code></pre></li></ol><p id="b5993cdb-7846-475e-b6e4-0bd8514e9e2a" class="">
</p><ol type="1" id="8654af15-a666-429a-9c78-619ca5c705b6" class="numbered-list" start="32"><li><strong>What are Private attributes ?</strong><p id="c0ec60d5-d9b4-4976-8d6c-5b24a9a4acf5" class="">Privates attributes are the attributes that are accessible to methods inside the class and cannot be accessed outside the class.</p><pre id="d047c366-189b-47cc-bbc9-815eb8ffcbc6" class="code code-wrap"><code>class Counter:

    def __init__(self):
        # private attribute: _class__attribute
        self.__current = 0
    
    def increment(self):
        self.__current += 1

    def decrement(self):
        self.__current -= 1
    
    def current_value(self):
        return self.__current</code></pre><pre id="40357ca9-da26-4be8-977c-ffc410c24c05" class="code code-wrap"><code>counter = Counter()
print(counter._Counter__current)</code></pre><pre id="f0c22cb0-91b3-4f74-89d0-f9188a4014c1" class="code code-wrap"><code>class Counter:

    def __init__(self):
        # private attribute: _attribute
        self._current = 0
    
    def increment(self):
        self._current += 1

    def decrement(self):
        self._current -= 1
    
    def current_value(self):
        return self._current</code></pre><pre id="c08e831a-95f0-4cda-bc4b-7513c310e90c" class="code code-wrap"><code>counter = Counter()
print(counter._current)</code></pre><p id="0f66e366-3772-46f6-a4e7-9048d35fd32f" class="">
</p></li></ol><ol type="1" id="1a6e400a-3b9c-47e6-83af-9e7d030e3cc0" class="numbered-list" start="33"><li><strong>What is Encapsulation ?</strong><p id="a3157031-3905-4874-82f0-177982775031" class="">Encapsulation is the process of packing of data and methods in a class so that you can hide the information and restrict access from outside the class.</p><p id="a9e17b3e-e97c-434b-beb0-68e3e551511e" class=""> </p></li></ol><ol type="1" id="752ac0bc-b5a8-49fc-86c0-f08559032838" class="numbered-list" start="34"><li><strong>What is static method ?</strong><p id="f2903243-33bc-4e18-8935-33fffb0cbc53" class="">A static methods are the methods aren&#x27;t bound to a class. cannot modify or access an object state.</p><p id="4c7aedda-9202-4948-90f2-4b9bcf7aa6c1" class="">To define static method we can use <strong>@staticmethod</strong></p><p id="9c3f3e3d-02b6-4c4b-91c7-a64811d8f5bb" class="">Static methods are used to define utility methods or group a logically related functions into a class.</p><pre id="5e6914b0-db84-4d5d-94f9-322622615951" class="code code-wrap"><code>class TemperatureConverter:

    KELVIN = &#x27;K&#x27;
    FAHRENHEIT = &#x27;F&#x27;
    CELSIUS = &#x27;C&#x27;

    @staticmethod
    def celsius_to_fahrenheit(c):
        return 9*c/5 + 32

f = TemperatureConverter.celsius_to_fahrenheit(55)
print(f)</code></pre></li></ol><p id="1141053d-7924-4b4a-a9dd-0e6cd212a4f9" class="">
</p><ol type="1" id="800a5b6b-be9e-498c-86da-63a3ac972bdb" class="numbered-list" start="35"><li><strong>Inheritance in Python ?</strong><p id="bcd4636c-03c0-47da-8bce-e97a47c0886d" class="">Inheritance allows one class to use attributes and methods of another class by just inheriting.</p><p id="e9f08041-a054-4f59-b087-60bb1c841ebf" class="">Code reusability and maintainability can be acheived using Inheritance.</p></li></ol><p id="257aaf80-03e4-4c29-9718-76e60b1a20d5" class="">
</p><ol type="1" id="e1a7b255-4be3-443f-98ef-a1159c5e51d3" class="numbered-list" start="36"><li><strong>Multiple Inheritance in Python ?</strong><p id="e3b928ba-27f8-4f68-95db-3deb9fb0f060" class="">Multiple Inheritance allows child class to inherit attributes and methods from more than one parent class.</p><pre id="3c68520e-01a4-417d-9162-28fdfe3c1ceb" class="code code-wrap"><code>class Car:
		def go(self):
				print(&#x27;Going&#x27;)</code></pre><pre id="01474f9f-d192-4a15-9f9b-db83722cab9f" class="code code-wrap"><code>class Flyable:
		def fly(self):
				print(&#x27;Flying&#x27;)</code></pre><pre id="cb87b443-b34b-46ab-bf2f-6ae20cc1c08e" class="code code-wrap"><code>class FlyingCar(Car, Flyable):
		pass</code></pre><pre id="bed61660-b71d-4e3a-8fd0-7d65f8086463" class="code code-wrap"><code>if __name__ = &#x27;__main___&#x27;
fc = FlyingCar()
fc.go()
fc.fly()</code></pre></li></ol></div></article></body></html>
