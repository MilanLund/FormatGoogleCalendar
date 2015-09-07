# FormatGoogleCalendar
Script gets public Google calendar and displays list of events. 
## How to install
###Step 1: Link required files
<pre><code>
&lt;!-- jQuery library --&gt;<br>
&lt;script src="//code.jquery.com/jquery-1.11.3.min.js"&gt;&lt;/script&gt;<br>
&lt;!-- FormatGoogleCalendar Javascript file --&gt;<br>
&lt;script src="/js/format-google-calendar.js"&gt;&lt;/script&gt;<br>
</code></pre>
###Step 2: Create HTML markup
<pre><code>
&lt;ul id="events-upcoming"&gt;<br>
&lt;/ul&gt;<br>
&lt;ul id="events-past"&gt;<br>
&lt;/ul&gt;
</code></pre>
###Step 3: Call the FormatGoogleCalendar
<pre><code>
formatGoogleCalendar.init({});
</code></pre>
## Options
* calendarUrl (string, url of a public Google calendar)<br>
* past (boolean, determines if past events should be displayed)<br>
* upcoming (boolean, determines if upcoming events should be displayed)<br>
* pastTopN (integer, number of latest past events, -1 means display all)<br>
* upcomingTopN (integer, number of upcoming events, -1 means display all)<br>
* itemsTagName (string, tagname of each event item)<br>
* upcomingSelector (string, selector name of a parent element of upcoming events)<br>
* pastSelector (string, selector name of a parent element of past events)<br>
* upcomingHeading (string, heading of upcoming events)<br>
* pastHeading (string, heading of past events)<br>

## Example of initialization
<pre><code>
formatGoogleCalendar.init({<br>
		calendarUrl: 'https://www.googleapis.com/calendar/v3/calendars/milan.kacurak@gmail.com/events?key=AIzaSyCR3-ptjHE-_douJsn8o20oRwkxt-zHStY',<br>
		past: false,<br>
        upcoming: true,<br>
        pastTopN: -1,<br>
        upcomingTopN: 3,<br>
        itemsTagName: 'li',<br>
        upcomingSelector: '#events-upcoming',<br>
        pastSelector: '#events-past',<br>
        upcomingHeading: '&lt;h2&gt;Upcoming events&lt;/h2&gt;',<br>
        pastHeading: '&lt;h2&gt;Past events&lt;/h2&gt;'<br>
	});
	</code></pre>
