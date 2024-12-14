HTML provide the `<time>` element for marking up times and dates in a machine-readable format.
<br>
There are many different ways in which humans write dates, but these variety of formats cannot be understood by computers.
- For example:
	- 20th January 2016
	- Jan 20 2024
- What if we want to grab the dates of all events in a page?
- The `<time>` elements allows you to attach an unambiguous, machine-readable time/date for this purpose.

```html
<!-- Standard simple date -->
<time datetime="2016-01-20">20 January 2016</time>
<!-- Just year and month -->
<time datetime="2016-01">January 2016</time>
<!-- Just month and day -->
<time datetime="01-20">20 January</time>
<!-- Just time, hours and minutes -->
<time datetime="19:30">19:30</time>
<!-- You can do seconds and milliseconds too! -->
<time datetime="19:30:01.856">19:30:01.856</time>
<!-- Date and time -->
<time datetime="2016-01-20T19:30">7.30pm, 20 January 2016</time>
<!-- Date and time with timezone offset -->
<time datetime="2016-01-20T19:30+01:00">
  7.30pm, 20 January 2016 is 8.30pm in France
</time>
<!-- Calling out a specific week number -->
<time datetime="2016-W04">The fourth week of 2016</time>
```