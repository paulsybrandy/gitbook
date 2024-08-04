# 12 Firefox Hidden Settings You Should Check Out

Firefox received an overhaul late in 2017, and is now fondly known as [Firefox Quantum](https://beebom.com/used-firefox-quantum-never-going-back-chrome/) for the re-engineering and fine-tuning that went into [improving its speed and reliability](https://beebom.com/firefox-quantum-beats-chrome/).

Firefox, just like Chrome, also lets you tweak some hidden settings to fiddle with the experimental features that are available in the browser. By tweaking these settings, you can enjoy a better browsing experience. It’s easy to get lost in the sea of experimental settings in Firefox and not all are meant to be played by anyone other than the developers. This is why we’ve listed out 12 Cool Firefox Hidden Settings for users to try out.

Before we get into our list, it would be prudent to first see the steps that we will use to access hidden Firefox settings. The below steps will show you how you can access Firefox hidden settings to unlock all the features that we are going to show you.

### Access Hidden Settings in Firefox

To access the Firefox hidden settings, type “**about:config**” in the address bar and hit enter. A warning will show up and you be required to click on “**I accept the risk!**” button to access all the hidden options.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-about-config-warning.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-about-config-warning.jpg)

Firefox Hidden Settings

In the advanced settings page, you will find a search bar at the top that you can use to quickly search for settings that we have listed below:

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-about-config.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-about-config.jpg)

Firefox Hidden Settings

Now that you have all the advanced options of Firefox at your disposal, here are the 12 Firefox hidden settings you should know.

### List of Firefox Hidden Settings

### 1. Change what Backspace Does

Inside Mozilla Firefox, the Backspace (on Windows; Delete on Mac) button has been assigned with the function of going back, by default. This was initially designed with inspiration from Internet Explorer. But if that’s not what you want it to do, you can change the key’s function and either set it to be used for scrolling a page or can be unmapped, so that the backspace/delete function can be exclusively used for text-related fields.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-backspace.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-backspace.jpg)

Firefox Hidden Settings backspace

To change the action of the backspace button, type “**browser.backspace\_action**” inside the search bar of the settings page. On the matching option that appears on the list, either right-click and select “Modify” or just double-click to modify the settings.

The numeric value will be ‘0’ by default and you can **set it to ‘1’** to use the backspace key as Page Up (and Shift+Backspace for Page Down). You can set to any other numeral to unmap the backspace key.

### 2. Block Auto Refresh

Some websites auto refresh web pages whenever they are updated or just to get more ad impressions. However, this is a really annoying from the user perspective, as the refresh takes 2-3 seconds. Additionally, refreshing web pages also eat up your precious bandwidth, definitely a concern if you have a limited data package. Thankfully, Firefox makes it easier to halt auto refresh.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-autorefresh.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-autorefresh.jpg)

Firefox Hidden Settings autorefresh

Type **accessibility.blockautorefresh** in the search bar and double-click on it to set it to “**true**”. Now all auto refreshing websites won’t refresh and you can browse with ease.

### 3. Paste Content with Middle Mouse Click

Right-clicking in a text field and selecting “Paste” isn’t the fastest option, and reaching for the keyboard to press Ctrl+V is a chore as well. In Firefox, you can set the middle mouse button to work as the paste command to quickly paste anything from the clipboard. Best of all, it will not override the current function of the middle mouse button, i.e. you can still automatically scroll pages.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-mouse.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-mouse.jpg)

Firefox Hidden Settings mouse

Type **middlemouse.paste** and double-click on the setting that shows up to set it to “**true**”. Now you can simply press the middle mouse button to paste content copied to the clipboard. Although, it will only work inside the Firefox browser.

### 4. Disable Firefox Animations

Firefox comes with animations to make transitions look cooler. However, these smooth transitions can also result in a little lag. Well, you can disable Firefox animations to make things snappier. Of course, it will remove all the cool animations but it will make navigation much faster. It’s a tweak worth making if your Firefox browser seems slower.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-animate\_.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-animate\_.jpg)

Firefox Hidden Settings animation

You need to type “**animate**” in the search bar to see all the options to disable animations. There will be **multiple settings** to tweak, just set all the options to “**False**” by double-clicking on each one. This will disable all the animations during closing/opening tabs, main menu, notifications and other areas where animations are prominent.

### 5. Open Links at the End of the Bar

By default, Firefox opens links in a new tab next to the current one, which is fine. However, what if you prefer to open new links at the end of the bar? Although it completely depends on your preference, but opening links at the end of bar could be a better option if you don’t like new tabs getting between tabs you are currently working on.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-aftercurrent.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-aftercurrent.jpg)

Firefox Hidden Settings

To open new links at the end of the bar, type **browser.tabs.insertRelatedAfterCurrent** in the search bar and set its value to “**false**”. Once done, whenever you click on a link to open in a new tab, it will be opened at the end of the bar.

### 6. Prevent Videos from Auto-playing

Often websites play audio and video content without seeking your permission first and while this can be annoying, it can also have damaging repercussion at times. To avoid this from foiling your mood or even your rapport, you can disable the feature by default from within the hidden settings inside Firefox.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-autoplay.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-autoplay.jpg)

Firefox Hidden Settings

To access the setting, type “**media.autoplay.default**” in the search bar and then **set the value of the integer to ‘1’** in order to enable the feature, If you choose any other numeral in place of 1, websites will be able to play videos by default as soon as the page is opened. But when the value is set to 1, media will only play when you click on the Play button.

### 7. Prevent Caching Encrypted Content

This is a security measure against a security hole that isn’t too dangerous, but it is still a step worth taking if you are very concerned about your security. By default, Firefox caches all types of content from all sources in your computer’s hard drive, to make it easier to load the same page, next time you visit it. This includes data from encrypted websites (SSL) as well. However, encrypted websites usually have confidential data and keeping that data locally on your system can be harmful.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-disk-cache.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-disk-cache.jpg)

Firefox Hidden Settings

Enter **browser.cache.disk\_cache\_ssl** in the search bar and double-click on the value to set it to “**false**”. Now all the data on encrypted websites will not be downloaded as cache in Firefox but this will increase the load times, as encrypted pages will need to be downloaded every time you open them.

### 8. Disable Firefox Prefetch

By default, Firefox will prefetch data from links on a page that you are more likely to click on. This helps speed things up for you, as data is already being downloaded while you are thinking about clicking on a link, however, it has some downsides. Firefox will use more bandwidth to download data that you may not even access, and the connection to the website is made even if you don’t click on it, which is bad for privacy reasons.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-prefetch.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-prefetch.jpg)

Firefox Hidden Settings

To disable Firefox Prefetch, type **network.prefetch-next** and double-click on it to set its value to “**false**”. This may slow down page loading a bit but it will stop Firefox from downloading unnecessary data and maintaining your privacy.

### 9. Move To New Tab From Link

Usually when you open a link in a new tab, the focus stays on the current page and you need to click on the newly opened tab to see its content. If you are are not comfortable with this approach and would like to immediately move to the new tab, this setting can be enabled from the Firefox hidden settings.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-load-in-background.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-load-in-background.jpg)

Firefox Hidden Settings

Look for the option **browser.tabs.loadInBackground** and set its value to “**false**”. Now, whenever you open a link in new tab, you will be immediately moved to it. Keep in mind though that this feature might not be great if you need to open multiple links from the same page, at a time.

### 10. Quickly Install Firefox Add-ons

While installing Firefox add-ons, you may have noticed that after downloading the extension, Firefox waits for a second saying “Verifying” and then allows you to click on “Install” button. Well, that 1 second wait is completely unnecessary and it is only there so that you can double-check what you are installing. Thankfully, you can disable this wait time and save yourself a second while installing new extensions.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-addon-delay.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-addon-delay.jpg)

Firefox Hidden Settings addon add-on

Search for option **security.dialog\_enable\_delay** and double-click on it to change its value. By default it is set to “1000”, change it to “**0**” to make the installation instant.

### 11. Improve Visibility When Finding Words or Phrases

Firefox, like all other browsers, lets you find specific words or phrases using the Ctrl+F (Cmd+F on Mac). While the feature in itself is pretty useful, Firefox has a nifty addition to the feature which can be enabled using the hidden settings in the browser. Aside from highlighting the matching term, you can also dim the rest of the webpage so that what you’re looking for does not evade your eyes.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight.jpg)

Firefox Hidden Settings

To toggle the feature, enter **findbar.modalHighlight** in the search bar on about:config page. To activate the setting, either double-click on the option or right-click and select Toggle and the value will change to “**true**“. This is how the page looks when the highlight feature is turned on.

\[Firefox Hidden Settings highlight]\([https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight-2.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight-2.jpg)

### 12. Highlight All Search Result

When you use the ‘Find’ feature in Firefox, it shows one result at a time – unlike Chrome, which highlights all relevant results in yellow and the one you’re currently viewing in orange. However, Firefox does let you activate the feature from within the hidden settings, thereby letting you read better and search relevant information on a webpage more easily.

![https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight-all.jpg](https://beebom.com/wp-content/uploads/2019/01/mozilla-firefox-highlight-all.jpg)

Firefox Hidden Settings

You can start by typing “**findbar.highlightAll**” in the search bar and set its value to “**true**“. Just like the previous options, you can double-click the option to activate it or right-click and then click on ‘Toggle’. As you can see in the image below, all the matching results are highlighted in a fuchsia color while the selected result is highlighted in green, elaborating how search can be improved by using this setting.
