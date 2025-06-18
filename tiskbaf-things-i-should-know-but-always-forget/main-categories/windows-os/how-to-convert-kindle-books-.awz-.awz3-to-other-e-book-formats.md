# How to Convert Kindle Books (.awz/.awz3) to Other E-book Formats

Amazon’s Kindle is a huge business. Both the hardware and the digital service changed how books, magazines, comics, and more are read each day. Unfortunately, customers can’t simply download Kindle books and read them through any app.

For Digital Rights Management (DRM) reasons, all Kindle e-books are locked to Kindle hardware. These digital books use Amazon’s proprietary AZW file format, even though Kindle tablets also support MOBI files. That makes reading these e-books outside the Kindle bubble nearly impossible. The good news is that DRM protection can be removed using free tools, but it’s important you don’t share your e-books with anybody else, as you could find yourself in breach of copyright laws.

Once you’ve removed DRM protection, it’s easy to convert Kindle books into PDFs. It can be a little tricky to do, but this guide shows you how to convert a Kindle book to PDF so you can read your purchased favorites on any e-book reader, not just on a Kindle.

### Download the AZW file(s)

✎ **NOTE:** Due to Digital Right Management, the e-book can’t simply download to any PC. Readers must have a hardware Kindle linked to their Amazon account. Otherwise, they will see an error stating, “You have selected content that is not compatible with any of your registered devices.” That being said, even if the e-book is read via the Kindle app on Windows 10, Android, or iOS, without an actual Kindle device linked to an Amazon account, Kindle e-books will not download.

1. With Amazon’s website loaded, click on your name, and then select Account on the drop-down menu.
2. Select Manage Content and Devices listed under Digital Content and Devices.
3. Click the Three-Dot Actions button next to the target e-book, as shown above.
4. Click Download & Transfer Via USB on the pop-up menu
5. A pop-up window appears with the registered Kindle selected. Click the yellow Download button.

The AWZ file will download to the default location on your PC, not to the listed Kindle device.

✎ **NOTE:** Calibre now offers a plugin called the KFX Input plugin, which allows you to import KFX files as well. Skip to the Calibre section to find out how to use it.

### Convert using Calibre (Windows/MacOS/Linux)

Calibre is software specifically designed to transfer and alter digital text into various formats. Fortunately, it will not eat up much of your device’s memory either. This software can support countless input formats, including MOBI, HTML, PRC, and AZW. Calibre is an effective e-book manager that gives its users the creative freedom and plentiful options they need to customize their graphics and visual images. The app’s display is user-friendly and easy to navigate, making for an exceptional and incredibly informative changeover experience. Furthermore, Calibre can operate with or without a continual or running network connection.

### Download DRM Removal Tool

✎ **NOTE:** In order to remove the DRM from your Kindle e-books, you’ll need to download an older version of Calibre, version 4.23.0.

Once you have downloaded and installed the correct version of Calibre, you’ll also need to download _**Apprentice Alf’s DRM Removal Tool**_. Just as Calibre, don’t download the latest version. You want to download and install v6.8.1, which will work with version 4 of Calibre. Just click on the DeDRM\_tools zipped folder to download it to your computer, then unzip the folder by right-clicking it and selecting Extract All (or however you would normally unzip folders on your computer).

#### Install the DRM Removal Tool Plug-in for Calibre

1. Launch Calibre and select Preferences from the top menu on the right-hand side.
2. Scroll down, and under Advanced, click Plug-Ins.
3. At the bottom right, click Load Plug-In From File, then select the DeDRM\_Plugin zipped folder on your computer in the pop-up window.
4. Click Open. Calibre will now install the plug-in.
5. Restart Calibre.

### Adding your Kindle serial number to Calibre

This is where things get a little complicated, but we’ll guide you through the next steps. You need to insert your Kindle serial number into Calibre.

1. Select Preferences again from the top menu.
2. Click Advanced, then select Plug-Ins.
3. Double-click the line that says File Type.
4. Double click on the DeDRM plug-in.
5. Select the first option that says eInk Kindle ebooks and click OK.
6. Now, you need to find and enter your Kindle serial number.
7. On most Kindles, you can find this by going to Settings > All Settings > Device Options > Device Info on your Kindle. You should see information about your Kindle, including the serial number.
8. If you’re unsure where to find your Kindle’s serial number, a quick Google of “serial location” plus your Kindle model, e.g. “10th-gen Paperwhite,” should help.
9. Enter the serial number without any spaces into Calibre.
10. Click Close, then OK, then click Apply.

### Adding your books to Calibre

Just click on Add Books on the top left in the menu, then select the books from your downloads folder or wherever you stored them after downloading them from Amazon earlier.

### Converting your e-books to PDF

Now that you’ve installed the DRM Removal plug-in, the actual conversion of an e-book to PDF is easy, as Calibre takes care of everything. Here’s how to convert your book:

1. Click on the book in your list that you’d like to convert to ensure it is highlighted.
2. Click Convert Books from the top menu in Calibre. You can also right-click on a book and select Convert Books, then choose Convert Individually or Bulk Convert.
3. In the pop-up window, ensure “AZW3” is showing as the Input Format at the top left. At the top right, where it says, Output Format, select PDF from the drop-down menu.
4. It’s also possible to adjust output settings like line height, font size, and so on, but we recommend converting the book first to see how it looks — you can always re-convert it later if you need to adjust any settings. Most books are fine with the default settings.
5. Check that the title and author on the right side of your screen are correct.
6. Click OK at the bottom of the screen and the conversion will begin.
7. Once it’s finished, the job counter at the bottom right will return to zero.
8. When you highlight the book in your list, at the right of your screen under Formats, you should now see a blue link that says “PDF.”
9. Click this to open your book in PDF format.
10. By default, Calibre stores e-books to the Calibre Library folder on your hard drive.
11. If you want to send the book to yourself (via email, for example) to read on other devices, you can select Click to Open on the right-hand side of your screen in Calibre, under Formats. This will bring up all the files associated with that book, including the cover, on your hard drive.
