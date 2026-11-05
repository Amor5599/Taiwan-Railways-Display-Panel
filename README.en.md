# Taiwan Rail Passenger Information System

[繁體中文](README.md) | **English**

A Windows application for passenger information displays and station announcements, with modes for Taiwan Railways (TRA), Taiwan High Speed Rail (THSR), and supported metro operators. It can use Taiwan's [TDX transport data platform](https://tdx.transportdata.tw/) to display train information and support announcement scheduling.

> **Important:** This is an independent project, not an official operational information system. Timetables, estimated arrival times, announcements, platform assignments, and other information may be delayed, incomplete, estimated, or unavailable. Always follow the operator's official information and staff instructions.

Features depend on the installed version, transport mode, station, available data, permissions, license and configuration. Beta releases may contain unfinished features or defects. Consult the release notes for the version you install.

## Contents

- [Download and installation](#download-and-installation)
- [Getting started](#getting-started)
- [Transport modes](#transport-modes)
- [Displays and passenger information](#displays-and-passenger-information)
- [Announcement management](#announcement-management)
- [Audio and speakers](#audio-and-speakers)
- [Settings and data](#settings-and-data)
- [Keyboard shortcuts](#keyboard-shortcuts)
- [Updates and backups](#updates-and-backups)
- [Troubleshooting](#troubleshooting)
- [Data, privacy and materials](#data-privacy-and-materials)
- [Feedback](#feedback)

## Download and installation

Download a package from [GitHub Releases](https://github.com/Amor5599/Taiwan-Railways-Display-Panel/releases). Check the release notes and asset names before downloading.

| Asset | Purpose |
| --- | --- |
| `TR_sche-Setup.exe` | Windows installer. Follow the installation wizard. |
| `TR_sche-Portable.exe` | Portable installation or update package. Follow its prompts and select the appropriate folder. |
| `TR_sche-Portable.zip` | Extract the archive and run `TR_sche.exe` from the extracted folder. |

Assets vary by release. Versions marked **Beta** or **Pre-release** are test builds. Back up important data before installing or updating.

### Installed and portable editions

The installed edition uses an installation directory selected through its setup workflow. Portable can be run from an extracted folder without registering a normal Windows installation. Do not run the executable directly inside the ZIP archive. Keep the extracted program files together.

Before replacing an existing portable installation, back up its settings and data and follow the release instructions. The program may need permission to write to its installation or portable folder.

## Getting started

1. Install the application or extract the portable package.
2. Launch it and complete the initial setup. Where supported, existing settings may be imported.
3. Choose the transport mode and station. Review station name and other station-specific values.
4. In **Preferences → Station → API**, configure the TDX credentials required by your data source.
5. Choose a suitable display and review its layout, directions and text settings.
6. Configure announcement languages, audio folders, output devices and speaker zones as applicable.
7. Save your changes. Follow any prompts to restart after switching modes.
8. Check data and test audio at a safe volume before relying on automatic playback.

A network connection and valid TDX account/API credentials may be required. Missing data, expired credentials, API limits, offline operation, and unsupported station/operator combinations can affect the result.

## Transport modes

Modes have different station data, display choices and announcement capabilities. Some settings may be hidden when they do not apply. Use **Preferences → Station → Transport mode** to select an existing station profile or manage supported profiles. Save pending changes first.

### Taiwan Railways (TRA)

The TRA mode provides multiple display styles for train services. Depending on the display and available data, it can show train number and type, origin, destination, route, arrival/departure time, platform and service status.

The broadcast manager supports manual and scheduled announcements, train-specific operations, preview and relevant station settings. Unreserved seating and intermediate-stop information can be displayed or announced when configured and available.

### Taiwan High Speed Rail (THSR)

THSR uses separate station and display settings. The board can show train numbers, destinations, scheduled times, platforms, route stops and status information, subject to the data available.

Supported announcements include approaching and currently stopped trains. Chinese, English, Taiwanese and Hakka audio can be configured. Applicable pages support manual daily status adjustments and unreserved-seat carriage configurations, including JSON import/export. Timetable-based estimates are not a guarantee of real-time train position.

### Metro

Supported profiles include Taipei Metro, New Taipei Metro and Taoyuan Airport MRT, with availability depending on the application version and operator data. Metro layouts can show destinations, station codes, countdowns, announcement tickers and media. The Taoyuan Airport MRT display is separate from the Taipei/New Taipei layout.

Depending on the station and data source, arrival information may be real-time or estimated from a timetable. Direction filtering and announcement availability depend on station, line and destination information.

Some layouts include an occupancy area. When occupancy information is unavailable, an unavailable or neutral indicator does **not** mean a train is empty. Video and image playback requires compatible local media and playback support.

## Displays and passenger information

Available settings differ by board. Depending on the selected display, you can adjust the display style, station, number of rows, text size, route/direction, ticker settings and other layout options.

Information may include service identifiers, destination, scheduled time, platform, running status, stop patterns, alerts or unreserved-seat information. A platform fallback is not necessarily a confirmed real-world platform. Screen content should be verified against official sources.

### Tickers and media

Supported tickers can display train information, station announcements, public information, advertising or emergency messages. The transition mode and speed may be configurable for a particular display.

Some metro boards can cycle through local advertising images and video. Configure the applicable media folder in Preferences. If media is absent, the board can show a default visual; codec support and playback performance depend on the machine.

Applicable ticker and advertising settings may provide JSON import/export. Check the page and back up existing data before importing.

## Announcement management

Press **F2** to open the broadcast manager. Depending on the current mode and version, you can:

- View, search and filter available train or announcement plans.
- Create individual or batch custom announcements.
- Play, stop or remove applicable entries and refresh the list.
- Review text previews and announcement timelines.
- Manage supported train-specific settings, including delay/cancellation and related configurations.
- Use available context-menu or quick-command actions.

A preview is not proof that an announcement has been queued or played. Automatic items depend on mode, enabled settings, train data, trigger conditions, sound files and output routing.

### Audio files and languages

Set the correct audio folder for the active transport mode. Available announcements may use recorded sound clips in supported formats and naming conventions. Language and audio availability differ by announcement type and version.

Enable the desired language and announcement type, select an appropriate speaker, and confirm volume and output zones. Missing or incompatible sound files can prevent an announcement. Test at a low volume first.

### Outputs, routing and other announcements

Where supported, output devices can be assigned to speaker zones or directions. Station music, safety/public-information messages, weather-related reminders, notification sounds, speech speed and audio effects are configured through applicable Preferences pages.

Results vary with the selected output device and source audio. Do not assume an audio device, zone or direction is correct without testing.

## Settings and data

Press **F3** for Preferences. Available pages and controls vary by mode and release:

- **Station and transport mode:** station identity, mode-specific profiles and related configuration.
- **Display:** supported boards, layout and display options.
- **Playback:** announcement content, enabled languages, scheduling and audio.
- **API:** TDX configuration and applicable account synchronization controls.
- **Data and backup:** supported configuration import/export and backup workflows.
- **Updates:** installed version, available releases and Beta preference.

Use the page's appropriate Save button and review any status or errors. Settings imported from another machine may refer to audio or media paths that do not exist on the current device.

### TDX credentials

Create and manage credentials through TDX. Enter them only in the application's settings, not in public reports or screenshots. Account-linked synchronization, where available, depends on the installed version and service availability. Never publish API keys, passwords, tokens, license details, or personal configuration files.

## Keyboard shortcuts

| Key | Action |
| --- | --- |
| `F2` | Broadcast manager |
| `F3` | Preferences |
| `F4` | Emergency mode |
| `F8` | Broadcast/ticker text templates |

Availability depends on focus, mode, version and configuration.

## Updates and backups

Use **Preferences → Station → Check for updates** to inspect the current and available version. Enabling Beta updates includes eligible pre-releases. Follow the updater prompts and choose the correct installed or portable workflow.

Save work and back up settings and important user files before an update, reset or import. Review the release notes for the exact package and version. An update is not a substitute for a verified backup.

## Troubleshooting

### No train data

Check the active mode and station, the computer's date and time, network access, API credentials and TDX service availability. Some operators or fields may not provide real-time data. A timetable estimate can differ from actual operations.

### Display appears empty or different

Confirm that the intended station profile and display are selected. Some controls are mode-specific. Save the correct page and restart if the application requests it. Check the installed version against the release notes.

### No announcements

Check that the relevant announcement type and language are enabled, train data is available, and the trigger condition has been reached. Verify the audio folder, filenames, speaker device, volume, zone and direction. Inspect the broadcast timeline and any skipped/error messages.

### Media does not play

Check the active mode and media folder, that files are readable and compatible, and that the installed package supports the selected format. An empty or unreadable folder can cause the default image or placeholder to appear.

### Settings do not take effect

Verify the station and mode being edited, click the appropriate Save button and check for an error. Follow any restart prompt. Imported settings do not necessarily include credentials, licenses or media files; check the import workflow's description.

## Data, privacy and materials

TDX availability, data fields, quotas, permissions and refresh rates are controlled by the data provider. The application cannot guarantee service availability or data accuracy.

You are responsible for obtaining permission to use any imported recordings, images, videos, fonts or other materials. Do not post credentials or personal data in public issue reports.

## Feedback

Report problems through [GitHub Issues](https://github.com/Amor5599/Taiwan-Railways-Display-Panel/issues). Include the application version, installed or portable edition, transport mode, station, steps to reproduce and screenshots or error messages where useful. Redact sensitive information first.
