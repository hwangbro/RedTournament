# Restream guide
- Make sure you are able to access the restream PC

## Overview
- Racers will be using racetime.gg as the racing platform for the tournament. As the restreamer, you will join the race. Once all the racers ready-up, you will quit the room and that will kick off the timer.
- You will provide each racer their own stream key to one of our Youtube channels. The restream will be capturing each of these feeds, cropping them appropriately, then formatting them in one of our race touranment layouts.
- Layout management (including the on-stream timer) is handled through NodeCG. See the NodeCG section below for more details.
- During the race, all racers will be in the same Discord voice channel, server deafened and muted. This is to ensure that if you or the commentators need to communicate directly with the racers, we can unmute/undeafen them and do so.
- During the race, the restream PC discord account and the commentators will be in a separate discord channel, and the restream PC will be screen sharing its OBS preview. This will be the commentators' feed for them to view and commentate off of.
- When the racers finish, if they want to hop on the stream for post-race comments, unmute/undefaen them and drag them into the commnetators channel.
- As the restreamer, most of the work is done in the setup and start of the race. During the race, it's mainly monitoring for issues that come up, changing layouts and layout details if runners forfeit, adjusting audio, etc.


## Pre race setup

### NodeCG
- NodeCG is how we list information on the layouts and control the timer on the layout.
- On the restream pc, go to "nodecg.hwangbro.com" to access the control panel
- "Edit currently active run" to add/adjust commentator and runner info (names/pronouns)
- When a race begins, make sure you click the Play button the Timer widget in "Main Workspace" as the racetime.gg race starts
- When each runner finishes, do your best to click the "Stop" button next to each runner to record their finished time into the layout.


### Youtube Feeds

<details><summary>Old method</summary>

#### Steps for each runner
- From the restream PC, go to Youtube. The PC should be logged in as the racebotxd account.
- If you click the profile picture in the top right and click "switch account", there should be at least 3 accounts there for us to stream from including racebotxd. Pick one of the channels for a runner.
- Click "+Create", then "Go Live"
- Make sure the "Privacy" of the stream is "Unlisted"
- Make sure "Stream Latency" is set to "Ultra low latency" is enabled
- Make sure "Unlist live replay once stream ends" is enabled
- Copy the stream key and provide it to one of the runners, ask them to start streaming. Their feed should appear in the preview in the top left
- Once the preview appears, right click it, click "Copy video URL" and paste it into the OBS scene browser source for that racer, e.g. `RACER #1 -> Racer 1 Browser Source`
- Interact with the browser source and full screen the video. Make sure the volume is maxed out.
- Adust the volume if needed (gain filter or reducing their volume)
- Repeat steps for next runner.

</details>

#### Steps for each runner
- On the `Red 2025 Tech Sheet`, there is a list of stream keys and corresponding youtube links.
- For now, the restream PC should already have Racer #1 -> youtube link for racer 1, 2 -> 2, etc.
- Provide the stream key to the racer and have them go live. You should see their feed captured in OBS.
- "Interact" with the browser source to make the video full screen, make sure the video feed is as up to date as possible by changing the playback speed to 2x until it "catches up"

#### Verify stream feeds
- On the `3 Racers` scene, ensure that all the feeds are appearing properly.
- Make sure that only one of the audio sources are unmuted at any given time.
- Do your best to sync the timers (using the livesplit.clock) by "Interacting" with the browser sources and pausing the feeds that are ahead until they are roughly in sync, using the Setup screen to see all 3 timers at once.


### Racetime.gg
- Create the racetime.gg race, join it yourself. This can be done from your own PC.
- Once the runners are ready to start and the stream is live, you will quit the race room and the racetime.gg timer should begin counting from -15 -> 0.
- The runners should be given a palette, whether it's from you or the commentators.
- Try to sync starting the NodeCG timer with racetime.gg's timer hitting 0.

## Racebot
- Once the racetime.gg room is open, you can enter the command in #race-bot to have it start watching
- !watch <race_id> spoiler delay=5 watcher=<twitch_ch> -> `!watch bonus-gymgym-6876 spoiler delay=4 watcher=redracetv`
- Delay can be adjusted during the race, but it mainly serves to avoid spoiling the chat if racebot messages are ahead of the feeds.
- `!add_delay bonus-gymgym-6876 10` will update the new delay to 10 seconds.

### Discord commentary channel setup
- The restream PC's discord account should join the commentatary voice channel
- On the restream OBS, right click the `Program` -> `Open Program Projector` -> `New Window`
- Maximize this window and have it in the background **without** minimizing it. This can be done by clicking any of the programs in the start bar, like OBS or discord.
- In discord, screen share the Program preview window you've just opened. This will be the commentary feed.
    - If you have issues exiting the screen, you can press `Alt-Tab` on your keyboard and you should be able to move your cursor outside of Parsec.
- As the restreamer, if you wish to be in the call with the commentators and talk to them without the stream hearing you, have the restream discord account local mute your own discord account.

### Runner discord setup
- Once the runners are setup, have them remain in the voice chat and server deafen/mute them.
- If you need to reach out for any reason, undeafen/unmute them, switch to their channel on **your** discord independently of the restream and talk to them.

## Race Start

### Final checklist
- The stream should be Live and on the Intro scene, with music playing.
- The stream PC should be recording in OBS.
- The stream pc should be sharing the OBS "Program" to the discord call for the commentators to watch and commentate over.
- The runners should all be "Ready" in racetime.gg, with whatever palette is decided.
- The runners should be in their own voice call, all server deafened/muted in case emergency communication is needed


### Starting the race
- To start the race, you can cue the commentators in and transition to one of the OBS scenes `3 Racers` or `2 Racers` depending on the number of runners.
- You shouldn't have to worry about the music; it shouldn't be playing on any of the tournament runner scenes.
- Quit the racetime.gg race so the timer will automatically start counting from -15

## Race In Progress
- Adjust audio levels if the people are complaining in stream.
- There may be periods where the runners or commentators are robot-y. This is unavoidable and should go away within a minute.
- Do your best to keep audio unmuted for the runner that is in the lead. Do this by muting the current runner and unmuting the runner whose audio you want playing on stream.
- If a runner forfeits, switch scenes to one of the 1/2, 1/3, or 2/3 scenes depending on which runner is the one that forfeited.

## Race Finish
- As the runner finishes a run, do your best to time the NodeCG runner "Stop" button with their actual finish time so it updates properly in the feed.
- If the runner wants to join for comments, unmute/undeafen them and have them move into the commentary channel. Adjust their audio levels as needed.
- Make sure their feed is muted and unmute the next runner still in the race.
- Once everyone is finished and the commentators/runners are done talking, have them close out and click "stop streaming" and "stop recording"

