<p align="center">
  <a href="README.md">简体中文</a> · <strong>English</strong>
</p>

<p align="center">
  <img src="docs/assets/logo.png" width="64" height="64" alt="TabNest · a resting bird" />
</p>

<h1 align="center">栖页 · TabNest</h1>

<p align="center">Find your open pages, save what you want to read later, and see where your browsing time goes.</p>

TabNest (栖页) is a new tab extension for Chrome and Edge. Click your browser's **+** button to bring open tabs, saved pages, and browsing statistics into one workspace.

Chromium Manifest V3 · Chrome / Edge support · Local storage · No account required

**[Download the extension ZIP](https://github.com/Maxine0917/Qiye/releases/latest/download/TabNest-Chrome.zip)** · [Install in four steps](#install-from-the-extension-package) · [Ask an agent to help you install](#ask-an-agent-to-help-you-install)

The extension interface is currently in Chinese. This guide includes the Chinese labels next to their English meanings so you can find the controls.

![Open and switch: click the browser's plus button to open TabNest, then click a page title to switch back to its existing tab](docs/assets/open-and-switch.gif)

## Quick installation

### Install from the extension package

1. [Download TabNest-Chrome.zip](https://github.com/Maxine0917/Qiye/releases/latest/download/TabNest-Chrome.zip) and extract it to a folder you will keep.
2. In Chrome, open `chrome://extensions`; in Edge, open `edge://extensions`. Turn on **Developer mode**.
3. Click **Load unpacked** and select the extracted folder that directly contains `manifest.json`.
4. Click your browser's **+** button to open TabNest. If the browser asks about the new tab page change, choose **Keep it** (保持现状).

Button labels may vary slightly by browser version or language. Select the folder, rather than the ZIP archive or the `manifest.json` file itself. The extension package already contains the files to load; you do not need to find an `extension/` subfolder. Keep the installation folder in place. **Using the extension requires no Node.js, Python, or server.**

<details>
<summary>Watch the full installation: download → extract → load → open TabNest</summary>

![Full installation: download the extension package from GitHub, extract it on macOS, check manifest.json, enable Developer mode in Chrome, load the folder, and open TabNest with the browser's plus button](docs/assets/install.gif)

This recording uses macOS, the actual v2.0.2 extension package, and a separate Chrome profile. Cursor and step annotations were added, and the recording was edited for clarity. Extraction and folder selection screens may differ on other operating systems; loading the extension in Chrome works the same way.

</details>

### Ask an agent to help you install

Copy this prompt to an agent that can access the internet and work with files on your computer:

```text
Please help me install the TabNest (栖页) extension from https://github.com/Maxine0917/Qiye in Chrome or Edge on my computer, depending on which browser I use. First read the repository's README.en.md and docs/INSTALL.md. Download the latest extension package from https://github.com/Maxine0917/Qiye/releases/latest/download/TabNest-Chrome.zip, extract it to a folder I will keep, and preserve the included LICENSE. If I already have an installation, confirm its existing folder before making changes. Find and check manifest.json, then give me the absolute path of its containing folder. Guide me to chrome://extensions in Chrome or edge://extensions in Edge, turn on Developer mode, click "Load unpacked" (the label may vary by version or language), and select that folder. Finally, ask me to click the browser's "+" button and confirm that TabNest appears correctly.
```

The agent prepares the installation files; you still need to confirm loading them in your browser. Use the same installation path for future updates.

<details>
<summary>Install from source or update an existing installation</summary>

When installing from [TabNest-Source.zip](https://github.com/Maxine0917/Qiye/releases/latest/download/TabNest-Source.zip), select `qiye/extension/`. If you use **Code → Download ZIP**, select `extension/` inside the extracted repository folder. Both folders directly contain `manifest.json`. Keep the root `LICENSE` with the source files.

To update, first check the original loaded folder in the extension's details. Update the files in that same folder, click **↻ Reload** on the extension card, and open a new tab. Refreshing the page alone does not update the extension name and icon recorded by the browser. Moving the installation to another folder may change its identity; data does not migrate automatically.

</details>

For folder examples, update instructions, and troubleshooting, see [Installation and updates](docs/INSTALL.md) (Chinese). See the [latest release](https://github.com/Maxine0917/Qiye/releases/latest) for the current version notes.

## Why TabNest exists

Losing a page you opened while researching, keeping too many tabs because you want to read them later, and finishing a busy day without knowing where the time went: these everyday problems inspired TabNest. It brings together pages that are **open now, saved for later, or already viewed**.

| Everyday problem | How TabNest helps |
| --- | --- |
| Too many tabs to find the page you just opened | Groups open tabs by website; click a title to switch back to the existing page |
| Multiple copies of the same page make cleanup tedious | Close individual tabs, close duplicates, or close all tabs in the current website group |
| You want to read something later without forgetting it | Save it to “Read later” (稍后查看), then check it off to move it to “Viewed” (已查看) |
| Other websites distract you while working | Start a focus timer and allow only the websites you listed beforehand |
| You want to see where your time goes without recording all the time | Pause recording when needed and review statistics for today, this week, this month, or this year |

## See how it works

### 1. Open with “+”, then click a title to return to an existing page

Once installed, TabNest becomes your new tab page. Open pages are automatically grouped by website, so you can find them without searching through the tab strip. Clicking a title activates **the existing tab**, even if it is in another browser window. The animation above shows both actions.

### 2. Close finished pages, duplicates, or an entire website group

Click **×** on the right of an entry to close that tab, with a small confetti effect. After confirmation, **Close duplicates** (关闭重复) keeps the earliest opened tab for each duplicate URL. After confirmation, **Close all** (关闭全部) closes every tab in **the current website group**.

![Closing tabs: close one tab with a confetti effect, close duplicate URLs, then close all tabs in a website group](docs/assets/close-tabs.gif)

### 3. Save pages for later and keep viewed pages separately

Click the bookmark icon to add a page to **Read later** (稍后查看). After reading it, check it off to move it to the collapsible **Viewed** (已查看) list. Your tab strip no longer has to double as a reading list, and you can see which pages still need attention.

![Read later: save a page with the bookmark button, check it off to move it to Viewed, then expand the viewed list](docs/assets/save-and-viewed.gif)

Saving a page does not close its original tab. Opening a saved link does not remove the record or automatically mark it as viewed. Both lists support search; unchecking a viewed entry returns it to Read later. Saved states persist across refreshes and stay in sync between TabNest pages in the same browser profile. The sidebar hides automatically when both lists are empty.

### 4. Pause recording whenever you need a break

Click **Pause recording** (暂停记录) and choose a duration. TabNest stops tracking browsing time during that period. Click again to resume early, or let recording resume automatically when the pause ends. **This pauses TabNest's recording; your browser's own browsing history is still kept.**

![Pause recording: select a 15-minute pause, see the countdown, then click to resume recording](docs/assets/pause-recording.gif)

### 5. Set aside focused time for your current task

First enter domain names under **Settings → Allowed websites** (设置 → 允许访问的网站) and save them. Then click **Focus timer** (专注计时), check **Restrict website access** (限制网站访问), choose a duration, and start. Listed websites remain accessible; other regular web pages are redirected to a focus reminder.

![Focus flow: save allowed websites, start a 25-minute focus session with website restrictions, open MDN normally, and check that another website is blocked](docs/assets/focus-allowlist.gif)

The allowlist is saved for future sessions. Starting the countdown without checking the restriction option does not block websites. The reminder page lets you go back, end the session, or allow that domain for the current session only. It is designed to support personal focus habits.

### 6. Review today, this week, this month, or this year

Click **Statistics** (统计) and switch between four time ranges to see total browsing time and website rankings. Today's view also includes a 24-hour heatmap. Export browsing history as JSON or CSV for further analysis.

![Browsing statistics: views for today, this week, this month, and this year show total browsing time and website rankings using demonstration data](docs/assets/browsing-stats.gif)

*The six feature animations were recorded from actual extension interactions using example pages and data in a separate browser profile. Cursor and step annotations were added, and the recordings were edited for clarity. Statistics are demonstration values, not real usage results. Recording took place on a Monday, so the totals for today and this week are identical.*

<details>
<summary>View workspace and settings screenshots</summary>

![TabNest workspace: tabs grouped by website, with Read later and Viewed lists on the right](docs/assets/workspace.png)

![TabNest settings: browsing records, theme, retention period, and allowed websites for focus sessions](docs/assets/settings.png)

Choose a light theme, a dark theme, or follow your system setting. You can also configure idle detection, domains excluded from time tracking, and history retention.

</details>

## Bug reports and feature requests

If something goes wrong, [report a bug](https://github.com/Maxine0917/Qiye/issues/new?title=Bug%20report%3A%20). Include your browser name and version, extension version, steps to reproduce, and expected versus actual behavior. Hide personal information in screenshots.

To suggest an improvement, [submit a feature request](https://github.com/Maxine0917/Qiye/issues/new?title=Feature%20request%3A%20). Describe the problem you encounter, how you currently handle it, and the outcome you would like.

## Privacy and data

Browsing records, saved pages, and settings are stored locally in `chrome.storage.local`. Chrome and Edge use the same storage API but keep separate data; switching browsers does not automatically sync it. The extension has no account system and does not upload these records to analytics or telemetry services.

Website icons may be loaded from their original websites, and opening a link visits the corresponding website. Those requests are subject to the websites' own privacy policies. See the [Privacy policy](PRIVACY.md) (Chinese) for the purpose of each permission.

Browsing history export is currently supported. There is no complete import or migration tool for saved lists and settings yet. Keep any data you need before uninstalling.

## Development and validation

<details>
<summary>Tests, packaging, browser checks, and project structure</summary>

The project uses plain HTML, CSS, and JavaScript ES Modules and can be loaded without a build step. Run the following commands from the project root. Tests require Node.js 22 or later; packaging requires Python 3.

```bash
# Regression tests
node extension/tests/nodeRunner.mjs

# Background startup check
node extension/tests/swSmoke.mjs

# Build the extension and full source packages
python3 scripts/package.py
```

Packaging produces:

```text
dist/
├── 栖页-插件.zip   # Runtime files and license; extract to install
└── qiye-源码.zip   # Source, tests, documentation, and GitHub Actions
```

Browser checks require Playwright and an available Chrome or Edge installation:

```bash
npm install --no-save --package-lock=false playwright@1.65.0
npx playwright install chrome msedge

# Chrome
node extension/tests/browser-ui.mjs

# Edge
QIYE_BROWSER_CHANNEL=msedge node extension/tests/browser-ui.mjs
```

The checks use a separate temporary browser profile and cover new tab counts, duplicate closing, saved pages, viewed states, persistence after refresh, synchronization between TabNest pages, themes, and narrow layouts. They do not use your everyday browser profile. Chrome is the default; set `QIYE_BROWSER_CHANNEL=msedge` to use Microsoft Edge. If Playwright is installed elsewhere, set `PLAYWRIGHT_MODULE` to its module entry point. Use `QIYE_BROWSER_EXECUTABLE` to specify an executable for a separately extracted browser. Screenshots and `result.json` are saved in the system's temporary directory by default; set `QIYE_SCREENSHOT_DIR` to change the location. On Linux, `npx playwright install --with-deps chrome msedge` also installs the required system dependencies.

On every push and pull request, GitHub Actions runs regression tests, the background startup check, real Chrome and Edge browser checks, and packaging. After a successful run, download `qiye-packages` from that run's Artifacts. The `qiye-browser-check` artifact contains screenshots and results and is retained for 14 days. If browser checks fail, the runner also attempts to save `failure.png` and diagnostic results to help investigate.

### Project structure

```text
qiye/
├── extension/         # Load this folder in Chrome or Edge
│   ├── background/    # Storage, time tracking, focus, and synchronization
│   ├── shared/        # Constants, types, and message protocol
│   ├── ui/            # Interface and interactions
│   ├── icons/         # Resting bird icons in SVG and PNG
│   └── tests/         # Regression tests and browser checks
├── docs/              # Installation, architecture, decisions, and media
├── scripts/           # Packaging tools
├── .github/workflows/ # Automated checks
├── README.md          # Chinese README
├── README.en.md       # English README
├── PRIVACY.md
└── LICENSE
```

[Architecture](docs/ARCHITECTURE.md) · [Development decisions](docs/DECISIONS.md) · [Changelog](CHANGELOG.md) · [Publishing guide](docs/PUBLISH.md)

These supporting documents are currently in Chinese.

</details>

## License and acknowledgments

This project builds on existing MIT-licensed code. Thank you to Zara Zhang for the original contributions. The copyright holders, years, MIT grant, and disclaimer are preserved in [LICENSE](LICENSE).
