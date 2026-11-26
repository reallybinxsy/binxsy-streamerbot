# Binxsy for Streamer.bot

Send Twitch clips to Discord, customize go-live announcements, and update the settings editors for your Binxsy widgets. These downloads update existing Streamer.bot setups on Windows with .NET Framework 4.8.1.

## Choose a download

| Download | Choose it if you already use… | What you get |
| --- | --- | --- |
| [Clip to Discord ZIP](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Clip-to-Discord.zip) | The Clip to Discord action group | Customize `!clip` chat replies and retry failed Discord deliveries at the end of a stream. |
| [Stream Announce Discord ZIP](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Stream-Announce-Discord.zip) | The Stream Announce Discord Webhook action group | Preview your go-live post, choose its mentions and accent color, and update the announcement as your stream changes. |
| [Binxsy.dll](https://github.com/reallybinxsy/binxsy-streamerbot/releases/latest/download/Binxsy.dll) | Any Binxsy widget that needs a shared library update | The settings editors used by Dynamic Stream Island, Minim Raid Out, Cider, Clip to Discord, and Stream Announce. |

Each ZIP includes the matching DLL, its installer, and a text guide. Download the ZIP for the action group you want to update.

## Install an update

1. Close Streamer.bot and extract the ZIP to its own folder.
2. Open the `Install-…txt` guide inside. Follow its PowerShell command using the folder that contains your `Streamer.bot.exe`.
3. Keep the backup folder the installer prints. Reopen Streamer.bot and run the updated group's **Settings** action.

For a DLL-only update, close Streamer.bot, back up its existing `dlls\Binxsy.dll`, and replace it with the downloaded file. Reopen Streamer.bot and run a widget's Settings action to see the installed version.

[Release notes and earlier versions](https://github.com/reallybinxsy/binxsy-streamerbot/releases)

The original Stream Announce Discord Webhook actions were created by [rondhi](https://twitch.tv/rondhi). The original script identifies its license as [GPLv3](https://www.gnu.org/licenses/gpl-3.0.en.html).
