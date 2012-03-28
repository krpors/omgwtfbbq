---
layout: base
header-title: Minecraft! 
---

Minecraft stuff
===============

Since I'm running a server on ``omgwtfbbq.nl:25565`` ... All of these
statistics and information are gathered from the server.log file.

'All time' logged in users:
---------------------------

These are the unique users who've logged in at least once in the server.
<div class="mc-users">
    Loading <code>/mcstats/users.html</code>, hold on.
</div>

Last 20 logins:
---------------

This is a list with the last 20 logins:

<div class="mc-logins">
    Loading <code>/mcstats/logins.html</code>, hold on.
</div>


Last 50 chat lines:
-------------------

The last 50 lines of the chat log.

<div class="mc-chatmsgs">
    Loading ``/mcstats/chatmsgs.html``, hold on.
</div>

<script type="text/javascript">
    function crud(thediv, theurl) {
        $.ajax({
            url: theurl,
            success: function(data) {
                if (data == "") {
                    $(thediv).html("File is empty!");
                } else {
                    $(thediv).html(data);
                }
            },
            statusCode: {
                404: function(data) {
                $(thediv).html("No file to parse!");
                }
            },
        });
    }

    $(function() {
        crud("div.mc-users", "mcstats/users.html");
        crud("div.mc-chatmsgs", "mcstats/chatmsgs.html");
        crud("div.mc-logins", "mcstats/logins.html");
    });
</script>
