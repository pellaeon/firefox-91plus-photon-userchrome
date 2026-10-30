Use Firefox’s **Browser Toolbox** to inspect the browser interface—tabs, toolbar, address bar, menus—and the CSS applied to it. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/?utm_source=chatgpt.com)

## 1. Enable Browser Toolbox

Open `about:config` and set both preferences to `true`:

| Preference | Value |
|---|---|
| `devtools.chrome.enabled` | `true` |
| `devtools.debugger.remote-enabled` | `true` |

These enable debugging of Firefox’s own interface. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/testing/geckodriver/Flags.html?utm_source=chatgpt.com)

## 2. Open it and inspect an element

Press **Ctrl + Alt + Shift + I** on Linux/Windows, or **⌘ + Option + Shift + I** on macOS. Accept the debugging connection prompt if one appears. Browser Toolbox opens in a separate window. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/?utm_source=chatgpt.com)

Select **Inspector**, click the **element picker** at the top left, then click the element you want to inspect in the main Firefox window.

- **Markup pane:** Find the element’s ID, classes, attributes, and surrounding elements.
- **Rules:** Examine matching CSS rules, their source files, and overridden declarations. You can edit values to see the result immediately.
- **Computed:** Check the final calculated CSS values. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/?utm_source=chatgpt.com)

### Useful for `userChrome.css`

**To inspect a menu or popup:** In Browser Toolbox, select **⋯ → Disable popup auto-hide**, then open the menu in Firefox and use the element picker. Press **Esc** to dismiss the popup afterward. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/browser_toolbox/?utm_source=chatgpt.com)

**To show Firefox’s built-in CSS rules:** Press **F1** inside Browser Toolbox and enable **Inspector → Show Browser Styles**. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/settings/?utm_source=chatgpt.com)

**To keep your changes:** Copy the resulting rules into your `userChrome.css`. Edits made in the Inspector are temporary and do not automatically save to the file. [Firefox Source Docs documentation](https://firefox-source-docs.mozilla.org/devtools-user/page_inspector/how_to/examine_and_edit_css/?utm_source=chatgpt.com)
