# Spicetify Commands

### Quick commands: (frequently used)

### When Spicetify stops working

`spicetify restore backup apply`



**Installation:**

* **Install Node.js:** Download and install the latest Node.js LTS version from [https://nodejs.org/](https://nodejs.org/)
* **Install Spicetify:**
  * Open your terminal or command prompt.
  * Run the following command: `npm install -g spicetify-cli`

**Usage:**

* **Launch Spicetify:**
  * Run `spicetify` in your terminal. This will open the Spicetify UI in your browser.
* **Check for Updates:**
  * Run `spicetify update` to update Spicetify to the latest version.
* **Apply Themes:**
  * Download a theme from a source like [https://github.com/spicetify/spicetify-themes](https://github.com/spicetify/spicetify-themes) or [https://www.reddit.com/r/spicetify/](https://www.reddit.com/r/spicetify/).
  * **Apply Theme:**
    * Copy the theme folder to your `~/.spicetify/Themes` directory.
    * Run `spicetify apply --theme [theme_name]`
* **Apply Customizations:**
  * Create a `.js` file with your customizations in `~/.spicetify/Customizations`.
  * Run `spicetify apply` to apply the customizations.
* **Customize Spicetify:**
  * Run `spicetify config` to open the configuration options for customizing your Spicetify experience.
* **Manage Extensions:**
  * **Install Extensions:**
    * Download an extension from a source like [https://github.com/spicetify/spicetify-extensions](https://github.com/spicetify/spicetify-extensions) or [https://www.reddit.com/r/spicetify/](https://www.reddit.com/r/spicetify/).
    * **Apply Extension:**
      * Copy the extension folder to your `~/.spicetify/Extensions` directory.
      * Run `spicetify apply` to apply the extension.
  * **Disable Extensions:**
    * Run `spicetify disable [extension_name]` to disable a specific extension.
* **List Available Themes and Extensions:**
  * Run `spicetify list` to see a list of available themes and extensions.

**Advanced Usage:**

* **Build custom extensions and themes:**
  * Refer to the Spicetify documentation for instructions on creating your own themes and extensions. [https://github.com/spicetify/spicetify-docs/](https://github.com/spicetify/spicetify-docs/)
* **Create Customizations:**
  * Refer to the Spicetify documentation for details on using JavaScript to create your own customizations.
* **Use Spicetify with third-party Spotify clients:**
  * Spicetify can be used with third-party clients like BetterSpotify and SpotX. Refer to their respective documentation for instructions.

**Troubleshooting:**

* If you encounter issues, refer to the Spicetify documentation or search for solutions on the official Spicetify subreddit.

**Note:**

* These commands are for Linux/macOS. For Windows, you might need to adjust the path for the `~/.spicetify` directory.
* Make sure you have administrator privileges to run certain commands.

This is a basic overview of Spicetify commands. For more detailed instructions and advanced usage, refer to the official Spicetify documentation.
