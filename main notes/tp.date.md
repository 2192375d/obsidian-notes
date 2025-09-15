Display today
<% tp.date.now("Do MMMM YYYY")%>

You can change the date from today to other days by adding a second parameter
<% tp.date.now("Do MMMM YYYY", "P-1M")%>

Adding double square brackets turn it into a link
[[<% tp.date.now("Do MMMM YYYY", "P-1M")%>]]