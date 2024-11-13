# ShoDam: Shodan IP Snatcher Bookmarklet

**ShoDam** is a simple and effective bookmarklet designed to extract IP addresses from Shodan search results with a single click. It’s a lightweight tool that enables users to collect a list of IPs quickly and easily, making it ideal for research and security testing purposes.

## **Features**

- **IP Extraction**: Collects IPs from Shodan search results by scanning the page and extracting relevant data.
- **One-Click Download**: Downloads the extracted IPs as a `.txt` file for easy saving and use.
- **No Installation Needed**: Drag and drop the bookmarklet into your bookmarks bar and click to use.
- **Simple & Lightweight**: Fast and efficient without requiring complex setup or dependencies.

## **Prerequisites**

- **Browser with JavaScript support** (Chrome, Firefox, etc.)

## **Installation**

1. **Import the Bookmarklet:**

   - Open your **Bookmark Manager** in your browser.
   - Choose **Import** and select the [ShoDam_Import.html](https://github.com/AnonKryptiQuz/ShoDam/blob/main/ShoDam__Import.html) file from your system.
   - This will add the **ShoDam** bookmarklet to your bookmarks bar.

2. **Manual Setup (if needed):**

   If you prefer to add the bookmarklet manually:
   - Open the [ShoDam_Bookmarklet.txt](https://github.com/AnonKryptiQuz/ShoDam/blob/main/ShoDam_Bookmarklet.txt) file and copy the following code inside it:

     ```javascript
     javascript:(function(){var ipElements=document.querySelectorAll('strong');var ips=[];ipElements.forEach(function(e){ips.push(e.innerHTML.replace(/[&quot;']/g,'').trim())});var ipsString=ips.join('\n');var a=document.createElement('a');a.href='data:text/plain;charset=utf-8,'+encodeURIComponent(ipsString);a.download='ShoDam.txt';document.body.appendChild(a);a.click();document.body.removeChild(a);URL.revokeObjectURL(a.href);})();
     ```

   - Open your **Bookmark Manager** in the browser.
   - Create a new bookmark and paste the copied code into the **URL** field.
   - Set the bookmark name to **ShoDam**.

## **Usage**

1. **Navigate to a Shodan search page** containing the IP addresses you want to extract.
2. **Click on the ShoDam bookmarklet** in your bookmarks bar.
3. The bookmarklet will automatically extract the IPs and download them as a `.txt` file, named `ShoDam.txt`.

## **Disclaimer**

- **Educational Purposes Only**: ShoDam is intended for educational and research use. The tool should not be used for illegal or malicious activities. Users should ensure compliance with local laws and regulations when using this tool.

## **Author**

**Created by:**
- [AnonKryptiQuz](https://AnonKryptiQuz.github.io/)
- [1hehaq](https://github.com/1hehaq)
- [HexShad0w](https://github.com/HexShad0w)
- [coffinxp](https://github.com/coffinxp)
- [Naho666](https://github.com/Naho666)

