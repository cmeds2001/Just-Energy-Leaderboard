Field Sales Leaderboard

Two files, no backend. The board reads data.json; you update scores by editing that file on GitHub.

Deploy (one time, ~5 minutes)
On github.com, create a new repo (e.g. sales-leaderboard, private is fine).
Add file → Create new file → name it index.html, paste the contents, commit.
Add file → Create new file → name it data.json, paste the contents, commit.
On vercel.com → Add New → Project → import the repo → Deploy. No settings to change.
Your board is live at the Vercel URL. Send it to the team or open it on the break-room TV.
Updating scores (daily, from your phone)
Open data.json in the GitHub app or github.com.
Tap the pencil, change the sales numbers, commit.
Vercel redeploys automatically — live in about 30 seconds. In TV mode the screen refreshes itself every 60 seconds, so a TV left on will pick it up without touching it.
Weekly rollover

At the end of each week, for every rep:

Copy their sales number into lastWeek.
Set sales back to 0.
Update weekLabel.

The lastWeek numbers power the ▲/▼ movement arrows.

Adding Cleveland's roster

In data.json, add reps inside Cleveland's reps array:

json
{ "name": "FirstName", "sales": 0, "lastWeek": 0 }

Separate each rep with a comma. Adding a third team works the same way, but the head-to-head battle bar only compares the first two teams in the file.
