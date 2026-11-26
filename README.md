# Binxsy for Streamer.bot

Choose the Twitch tools you want to use. Each `.sb` file imports one tool into Streamer.bot on Windows. All four use the same [Binxsy.dll](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Binxsy.dll).

| Tool | What it does | Download |
| --- | --- | --- |
| Clip to Discord | Viewers type `!clip` to create a Twitch clip and post it in your Discord channel. | [Clip-to-Discord.sb](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Clip-to-Discord.sb) |
| Stream Announce Discord | Posts when you go live, updates the post when your stream changes, and removes it when you go offline. | [Stream-Announce-Discord.sb](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Stream-Announce-Discord.sb) |
| Cider | Lets viewers request songs, check the current track, and vote to skip in Cider. Download both files. | [Cider.sb](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Cider.sb) · [cider-listener.html](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/cider-listener.html) |
| Dynamic Stream Island 3.0 | Adds a current-track display, audio waveform, and Twitch alerts to an OBS scene. | [DSI-3.0.sb](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/DSI-3.0.sb) |

## Import a tool

1. Use Streamer.bot 1.0.7 on Windows with .NET Framework 4.8.1. If you have an existing setup, back up your Streamer.bot data and current DLL before replacing anything. [Streamer.bot backup guide](https://docs.streamer.bot/guide/core/backup)
2. Close Streamer.bot. Download `Binxsy.dll` and place it in the `dlls` folder beside `Streamer.bot.exe`. Create that folder if needed. One copy serves every import from the same release.
3. Reopen Streamer.bot, click **Import** on the top toolbar, and drag your `.sb` file onto **Import String**. Review the included items and any existing entries marked for overwrite, then click **Import**. Repeat for each tool you want. [Streamer.bot import guide](https://docs.streamer.bot/guide/core/import-export)
4. Connect your Twitch broadcaster account. In **Actions & Queues**, select your tool’s **Settings** action. Right-click its **Test** trigger and choose **Test Trigger** to open the editor. [Twitch account setup](https://docs.streamer.bot/guide/platforms/twitch#accounts)
5. For a tool with chat commands, open **Commands** after import. Fresh imports can leave commands disabled. Review who can use each command, then enable the ones you want. For Clip to Discord, enable **!clip** before testing it in chat.

## First use

**Clip to Discord.** Choose a Discord channel for clips, create a webhook for that channel, and paste the URL into **Delivery**. Save your settings. While live, try `!clip 15 Last lap` in Twitch chat and check for the clip in Discord. [Create a Discord webhook](https://support.discord.com/hc/en-us/articles/228383668-Intro-to-Webhooks)

**Stream Announce Discord.** Paste your announcement channel’s webhook into **Delivery**, then customize the **Go-live post**. **Send test** posts your draft to that channel with mentions muted. Save the design to use it for your next stream. The original Stream Announce actions are by rondhi and identify their license as GPLv3. [rondhi’s extensions](https://rondhi.com/) · [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html)

**Cider.** Enable Cider’s playback API, then enter its URL and your app token under **Connections**. Select **Check primary connection**. Start Streamer.bot’s WebSocket server on `127.0.0.1:8080` and keep `cider-listener.html` open on the same PC while streaming. Play a track and confirm its title in the listener. [Cider install guide](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Cider-Install.txt) · [Cider playback API](https://taproom.cider.sh/docs/api/)

**Dynamic Stream Island 3.0.** Run OBS and Streamer.bot on the same PC. Install the OBS plugins listed in the guide and start SMTC Bridge for track information. In **[DSI] Settings**, choose your OBS collection and music audio source, then select **OBS setup → Install scene & sources**. Add **[DSI] Widget** as an existing scene source in your streaming scene. [DSI install guide and plugin downloads](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/DSI-3.0-Install.txt) · [SMTC Bridge](https://github.com/nuttylmao/smtc-bridge)

**Using Cider and DSI together.** The **DSI Song** command triggers both tools’ current-song actions. Enable the command in **Commands**, then choose one reply. In **Actions & Queues**, disable its command trigger on either **[CIDER & SB] 8 - Current Song** or **[DSI] Song Information**. The other action will answer `!song` and its aliases.

For a previous version, download its DLL and imports from the same release. [Release history](https://github.com/reallybinxsy/binxsy-streamerbot/releases)
