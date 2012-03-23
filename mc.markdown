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
    Loading ``/mcstats/users.html``, hold on.
</div>


Last 50 chat lines:
-------------------

The last 50 lines of the chat log.

<div class="mc-chatmsgs">
    Loading ``/mcstats/chatmsgs.html``, hold on.
</div>

<script type="text/javascript">
    $(function() {
        $.ajax({
            url: "mcstats/users.html",
            success: function(data) {
                if (data == "") {
                    $("div.mc-users").html("File is empty!");
                } else {
                    $("div.mc-users").html(data);
                }
            },
            statusCode: {
                404: function(data) {
                $("div.mcstats").html("No file to parse!");
                }
            },
        });

        $.ajax({
            url: "mcstats/chatmsgs.html",
            success: function(data) {
                if (data == "") {
                    $("div.mc-chatmsgs").html("File is empty!");
                } else {
                    $("div.mc-chatmsgs").html(data);
                }
            },
            statusCode: {
                404: function(data) {
                $("div.chatmsgs").html("No file to parse!");
                }
            },
        });

    });
</script>
